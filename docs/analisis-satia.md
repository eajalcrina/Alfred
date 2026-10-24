# Ingeniería inversa de Satia (satia.so) y lecciones para la vertical de IA de Redesign Lab

> Fecha del análisis: 24-oct-2026. Fuentes: sitio público satia.so (home, /precios, /partners, /producto/*, /templates, /terms, /privacy, /dpa, /ai-terms), cabeceras HTTP y bundles JavaScript públicos. Todo lo marcado como **[Inferencia]** se deduce de evidencia indirecta; lo demás es observable en el sitio.

---

## 1. Resumen ejecutivo

- **Qué es:** una plataforma no-code de "sistema operativo con IA" para negocios. El usuario conversa con un meta-agente (**Sati**) y este *construye* las piezas: bases de datos (tablas), agentes conversacionales multicanal, automatizaciones, integraciones y componentes visuales (dashboards).
- **Para quién:** pymes de LatAm y EE. UU. (restaurantes, clínicas, tiendas). También agencias e implementadores que hoy usan n8n, Make, Zapier o ManyChat.
- **Cómo gana dinero:** freemium sin cobro por usuario. Cobra por **registros almacenados** y por **tokens de IA** con margen sobre el costo del modelo. Escala con un **canal de partners**: los partners cobran la implementación y Satia les comparte entre 12 % y 20 % del consumo de tokens.
- **Ventaja real (moat):** no está en la IA en sí. Está en (1) ser **Meta Business Partner**, con la API oficial de WhatsApp incluida; (2) tener todo en una sola herramienta: datos, agente, canal, automatización y UI; (3) una red de implementadores que hace las ventas y el trabajo de implementación.
- **Origen probable:** Colombia, constituida como Delaware LLC **[Inferencia]**. Las señales: integraciones con Siigo, Alegra, Wompi y PayU, moneda COP, zona horaria `America/Bogota` y teléfonos +57 en las plantillas.

---

## 2. Propuesta de valor (lo que dice el sitio)

| Elemento | Evidencia |
|---|---|
| Promesa | "Just ask Sati. It gets done." / "Describe what you need in your own words and Sati builds the whole system." |
| Velocidad | "Primer proceso implementable en menos de 3 horas"; para partners, "días, no semanas" e "implementaciones hasta 50 % más ágiles". |
| Comparación implícita | "Sin Satia": 4 o 5 herramientas (modelo de IA, canal, automatizador, base de datos y hosting). "Con Satia": una sola plataforma. |
| Gobernanza | Auditoría de cada acción, permisos por usuario y por agente, aprobación humana para acciones sensibles, escalamiento a humano y restauración de 30 días. |
| Canales | WhatsApp (API oficial), Instagram, Gmail/Outlook, Telegram, TikTok, LinkedIn, webchat y **voz** (agentes telefónicos por SIP). |
| Casos de uso tipo | Calificación de leads por WhatsApp, agendamiento con recordatorios, cotizaciones con seguimiento, enrutamiento de solicitudes y campañas con plantillas de WhatsApp. |
| Plantillas publicadas | Pizzerías (pedidos por WhatsApp), consultorio médico, restaurantes (reservas, menú, abonos y eventos) y "arth". |

---

## 3. Ingeniería inversa de la tecnología

### 3.1 Stack observado

| Capa | Tecnología | Evidencia |
|---|---|---|
| Frontend / marketing | **Next.js** (App Router, RSC, Turbopack) | `x-powered-by: Next.js`, chunks `turbopack-*.js`, cabeceras `rsc` |
| Hosting | **Vercel** (región `iad1`, Virginia) | `server: Vercel`, `x-vercel-id: iad1` |
| i18n | Cookie `NEXT_LOCALE` (es/en) | Set-Cookie |
| Base de datos, auth y storage | **Supabase** (PostgreSQL con RLS, Auth y Storage) sobre **AWS** | Tabla de subprocesadores del DPA; cookie `sb-*-auth-token` en el JS |
| LLM principal | **Google Gemini 2.5 Flash / Pro** | AI Addendum: "Gemini 2.5 Flash / Pro"; RAG y *captioning* de visión con Gemini 2.5 Flash |
| LLM secundario y embeddings | **OpenAI API** | DPA: "Language model reasoning and vector embeddings" |
| Mensajería | **Meta Cloud API** (WhatsApp e Instagram Graph) | DPA; campos `whatsapp_waba_id` y `whatsapp_phone_number_id` en plantillas; "Satia es Meta Business Partner" |
| Voz | Carriers telefónicos (síntesis de voz y enrutamiento SIP) | DPA, sección "Telephony Voice Agents" |
| Analítica y marketing | Google Tag Manager/gtag, **Meta Pixel**, Vercel Analytics | Scripts en el HTML |
| Integraciones listadas | Stripe, Mercado Pago, Wompi, PayU, Siigo, Alegra, HubSpot, Calendly, Zoom, Slack, Telegram, Twilio, Shopify, WooCommerce, Notion, Airtable, Outlook, Mailchimp, SendGrid, Resend, Trello, Dropbox y "cualquier API abierta" | Catálogo en el bundle JS |
| Cumplimiento | Términos (Delaware, arbitraje), Privacy, DPA y AI Addendum con *zero data retention for training* | Páginas legales |

### 3.2 Arquitectura funcional inferida

Las plantillas públicas se sirven como JSON serializado. Eso permite ver el **modelo de datos interno** de Satia:

```
Workspace (tenant, RLS en Postgres)
├── Entities / Tablas        → campos: key, type, label, is_required, is_unique,
│                              sort_order, config, default_value, agent_instruction
│                              ("agent_instruction" = instrucción para que el agente sepa
│                              cómo llenar/interpretar el campo)
├── Records                  → filas (la unidad que se factura)
├── Agents                   → prompt/rol, base de conocimiento (RAG), canales,
│                              permisos (access/permission/precedence), approval
├── Automations              → trigger_type + trigger_config (evento, cron, webhook),
│                              steps, scripts **Python** (`import satia_sdk`, `import db`,
│                              variables de entorno, `required_secrets`)
├── Visual components        → HTML/JS embebido que usa un SDK de cliente:
│                              satia.onReady(), getSchema(), getEntities(),
│                              createEntity(), updateEntity(), toast()
├── Integrations / Secrets   → required_secrets (p. ej. STRIPE_SECRET_KEY,
│                              token de Mercado Pago, token de Meta)
└── Audit log                → cada acción con actor; restauración de 30 a 365 días
```

**[Inferencia] Cómo funciona Sati, el "constructor":**
1. Sati es un agente con *tool calling* cuyas herramientas son operaciones sobre ese meta-modelo: `create_table`, `add_field`, `create_agent`, `create_automation(script)`, `create_component(html)` y `connect_integration`.
2. Con el LLM genera código Python para las automatizaciones y HTML/JS para los componentes. Ambos corren en *sandbox*: un runtime aislado para Python y un iframe con un SDK *postMessage* para la UI.
3. Las **plantillas** son el mismo grafo de "piezas" (`pieces`, `temp_id`) serializado. Instalar una plantilla es simplemente reproducir esas piezas en un workspace nuevo.
4. El almacenamiento de "records" es casi seguro un esquema genérico: tablas definidas por el usuario sobre Postgres, con JSONB o EAV, y cada fila cuenta como un registro.
5. El RAG ("Satia Docs") indexa Markdown, PDFs e imágenes. Las imágenes pasan antes por *captioning* con Gemini y los embeddings se hacen con OpenAI, probablemente en **pgvector** dentro de Supabase.

### 3.3 Qué tan difícil es replicarlo

| Componente | Dificultad | Comentario |
|---|---|---|
| Tablas dinámicas y CRUD con RLS | Media | Patrón conocido (Supabase + JSONB + schemas). |
| Agente conversacional con herramientas y RAG | Media | Commodity con SDKs actuales. |
| Meta-agente "constructor" fiable | **Alta** | La dificultad no es generar código, sino que lo generado **funcione siempre**: validación, *rollback*, pruebas y auditoría. |
| Sandbox de ejecución Python y UI | Media-alta | Requiere aislamiento serio, cuotas y manejo de secretos. |
| WhatsApp oficial a escala | **Alta (no técnica)** | Exige ser Tech Provider/BSP de Meta, verificación de negocio, plantillas y calidad del número. |
| Voz telefónica | Alta | Latencia, carriers y costos por minuto. |
| Canal de partners y facturación por tokens | Media | Requiere *metering*, Stripe, wallets y comisiones diarias. |

---

## 4. Ingeniería inversa del modelo de negocio

### 4.1 Precios (públicos, en USD)

| Concepto | Precio |
|---|---|
| Registros 0–1.000 | Gratis |
| Registros 1.001–10.000 | $25/mes |
| Cada bloque adicional de 10.000 | +$20/mes |
| Créditos de IA | $1,50 por millón de tokens de entrada / $10 por millón de tokens de salida (pago por uso, recarga automática opcional) |
| Crédito de bienvenida | $10 |
| Usuarios, canales, automatizaciones, storage | **Ilimitados y sin costo** |
| Extensión de auditoría | 60 días $20, 90 días $30, 180 días $60, 365 días $120 al mes |

**Lectura estratégica:**
- **No cobra por usuario ni por funcionalidad.** Así elimina la fricción de adopción en equipos y convierte el consumo en la métrica de ingreso: cuanto más trabajan los agentes, más factura.
- **Margen en tokens [Inferencia]:** cobra una tarifa única ($1,50 / $10) sin importar el modelo. Esa tarifa está alineada con el precio de lista de modelos "pro", pero el producto declara Gemini 2.5 **Flash** como motor de varias funciones, y Flash cuesta varias veces menos. Si enruta la mayor parte del tráfico a modelos baratos, el margen bruto sobre IA podría superar el 60–70 % antes de la comisión al partner. *Conviene verificar los precios actuales de cada proveedor antes de usar esta cifra.*
- **Registros como segundo eje de ingreso:** es el *lock-in* natural, porque una vez que los datos operativos del negocio viven ahí, cambiarse cuesta.

### 4.2 Programa de partners (el motor de crecimiento)

| Nivel | Requisito | Comisión recurrente sobre tokens de sus clientes |
|---|---|---|
| Casual | Registro gratis | — |
| **Partner** | Fee de admisión de **$149** (pago único) | 12 % |
| **Master** | Más de 200 puntos activos | 16 % y perfil destacado |
| **Wizard** | Más de 500 puntos activos | 20 % y los mejores leads como "brazo oficial de implementación" |

- Puntos: se empieza con 100. Cada recarga de un cliente suma el 10 % de su valor en puntos y los puntos **decaen un 1 % diario**, lo que obliga a mantener clientes activos.
- El partner cobra su implementación a su propio precio (Satia sugiere **$500–3.000**). Satia factura la plataforma directamente al cliente.
- El cliente queda **vinculado al código de referido** del partner. La implementación es co-branded: el cliente sabe que la plataforma es Satia.
- Satia **genera demanda** y reparte los leads entre partners certificados según industria e idioma.
- Su propio ejemplo: un cliente que consume $200/mes genera $24–40/mes para el partner.

**Lectura:** Satia **tercerizó la consultoría** y se quedó con la plataforma. Es el mismo patrón que Shopify Experts o HubSpot Solutions Partners. Gracias a eso escala en LatAm sin un equipo de implementación propio, que es exactamente el problema de escalamiento que plantea el brief de Redesign Lab.

### 4.3 Go-to-market

- PLG (registro gratis) más **plantillas por vertical**, que funcionan como landing SEO y como onboarding.
- Academy, canal de YouTube ("Sati-so"), Instagram y Facebook (página creada alrededor de 2025).
- FAQ con *schema.org* para posicionamiento SEO y en buscadores con IA.
- Contacto comercial visible: un único correo personal. Señala un equipo pequeño o una etapa temprana **[Inferencia]**.

### 4.4 Riesgos y debilidades observables

1. **Dependencia de Meta:** si cambian las políticas o precios de WhatsApp, el negocio se ve afectado directamente.
2. **Fiabilidad del constructor:** el código generado por IA en producción, sin prácticas de ingeniería detrás, puede dar problemas de soporte.
3. **Segmento pyme (micro/pequeña):** ticket bajo y churn alto.
4. **Sin testimonios ni casos publicados** en el sitio: todavía hay poca prueba social.
5. **Datos en EE. UU.** (Supabase/AWS y APIs en EE. UU.): puede ser una objeción para empresas medianas con requisitos de residencia de datos.

---

## 5. Implicaciones para la nueva vertical de IA de Redesign Lab

### 5.1 Satia frente al modelo del brief

| Dimensión | Satia | Vertical de Redesign Lab (brief) |
|---|---|---|
| Qué vende | Plataforma (software) | **Proceso**: inmersión de 1 mes con 5–6 soluciones en producción |
| Segmento | Micro y pequeña empresa | **Mediana** empresa |
| Lock-in | Alto (datos más código de referido) | Explícitamente **sin dependencia**: deja capacidad instalada |
| Proveedor de IA | Gemini/OpenAI, oculto al cliente | **Agnóstico** |
| Monetización | Uso (tokens y registros) más canal | **One-shot pricing** más upsell (licencias y retainer) |
| Escala | Partners hacen la implementación | Debe escalar sin presencia del equipo |

**Conclusión:** Satia es más un **proveedor potencial o un referente** que un competidor directo. Satia vende la herramienta; Redesign Lab vende la transformación. La tensión de fondo está en el principio "agnóstico / sin dependencia", que choca con el lock-in deliberado de Satia.

### 5.2 Qué copiar (patrones de valor probado)

1. **Precio transparente y sin cobro por usuario.** Encaja con el "one-shot pricing" y con el argumento de control de costos.
2. **Gobernanza como argumento de venta:** auditoría, permisos, aprobación humana y escalamiento. Para una empresa mediana pesa más que "la IA es mágica".
3. **Plantillas por proceso y vertical.** Equivalen a la "biblioteca de recursos" del brief y convierten cada caso resuelto en un activo reutilizable. Por ejemplo, el agente de consolidación de Excels se vuelve una plantilla.
4. **Economía de canal:** comisiones recurrentes, niveles con decaimiento y reparto de leads. Sirve si a futuro la vertical quiere certificar a otros implementadores con la metodología de Redesign Lab.
5. **Meta-modelo simple:** tablas, agentes, automatizaciones y vistas. Es una buena taxonomía para estructurar las "5–6 soluciones" de la inmersión.

### 5.3 Qué **no** copiar (por ahora)

- **No construir un clon de Satia.** El costo real está en la fiabilidad del constructor, el estatus de BSP de Meta, la voz y la operación del canal: meses de ingeniería y un producto distinto al que define el brief.
- No atar al cliente a una plataforma propia, porque contradice el principio de capacidad instalada.

### 5.4 Opciones estratégicas

| Opción | Descripción | Pros | Contras |
|---|---|---|---|
| A. Ser partner de Satia | Usar Satia como herramienta de entrega en algunas inmersiones | Rápido, ingreso recurrente del 12–20 % e incluye WhatsApp oficial | Lock-in, pyme-céntrico, contradice el principio de agnosticismo, datos en EE. UU. |
| B. Plataforma propia tipo Satia | Construir constructor, agentes, datos y canales | Control total y valoración de software | Caro, lento y fuera del foco del brief |
| **C. Metodología + kit agnóstico (recomendada)** | Inmersión con un **catálogo de patrones** (plantillas) implementables sobre la herramienta que el cliente ya tiene (Google Workspace / M365, Claude/Gemini/ChatGPT, n8n/Make, Sheets/Excel). Satia queda como una opción más del catálogo para casos de WhatsApp en pymes | Coherente con el brief, escala por plantillas y monetiza el partnership de nube | Exige disciplina para documentar y estandarizar |

### 5.5 Primera entrega sugerida (respuesta a la sección 7 del brief)

**Prototipo funcional del agente de consolidación de reportes**, construido como **plantilla reutilizable** y documentado con la misma taxonomía de Satia (tabla, agente, automatización y vista):

1. **Entrada:** varios Excel de distintas áreas, recibidos por correo o en una carpeta compartida.
2. **Agente validador:** revisa el esquema esperado, detecta columnas faltantes o formatos inválidos y **pide el reenvío automáticamente** al responsable.
3. **Consolidación:** unifica los archivos en una tabla maestra (Sheets/Excel o base de datos) y registra cada paso en un log de auditoría.
4. **Vista:** un dashboard simple con el estado por área (recibido, con errores, consolidado).
5. **Métricas de evidencia:** horas ahorradas, número de iteraciones de reenvío y tiempo de cierre del reporte. Responden al principio de "evidencia sobre promesa".

Este prototipo cumple tres funciones a la vez: es una **demo vendible**, es la **primera plantilla del catálogo** y da contenido de autoridad (video corto y caso documentado).

### 5.6 Preguntas abiertas para resolver con Roy Pérez

1. **¿"Cloud Network Partner" se refiere a Google Cloud o al programa de partners de Claude (Anthropic)?** La referencia a suscripciones de unos $19–20/mes y a paquetes de unas 30 licencias sugiere licencias de un asistente de IA por usuario. La respuesta define el stack por defecto del kit y el modelo de upsell.
2. Para el prototipo, ¿qué stack base usamos: Google Workspace + Apps Script/Gemini, M365 + Power Automate/Copilot, o Python + LLM vía API?
3. ¿Satia (u otra plataforma) entra en el catálogo como opción para clientes que necesitan WhatsApp?
4. ¿El piloto interno fallido puede documentarse como el **caso 0** de la metodología?
5. ¿Hay que cumplir requisitos de residencia de datos o confidencialidad con las empresas medianas objetivo, por ejemplo en finanzas o salud?

---

## 6. Anexo: evidencia técnica relevante

- Cabeceras: `server: Vercel`, `x-powered-by: Next.js`, `x-vercel-id: iad1::…`, `set-cookie: NEXT_LOCALE=en`.
- Autenticación: regex en el cliente `/(?:^|; )sb-[^=]+-auth-token/` y `supabase.auth.getSession()`.
- DPA, subprocesadores: Supabase Inc./AWS (hosting, PostgreSQL con RLS, auth, storage), Google LLC (Gemini: inferencia, visión, *captioning*), OpenAI LLC (razonamiento, embeddings), Meta Platforms (WhatsApp Cloud API, Instagram Graph API) y carriers telefónicos (voz, SIP). Todos en EE. UU.
- Plantillas: scripts Python con `import satia_sdk`, `import db`, `os.environ.get("SATIA_TIMEZONE", "America/Bogota")`; componentes HTML con `satia.createEntity(...)`, `satia.getEntities(...)` y `satia.getSchema()`; secretos declarados en `required_secrets`.
- Entidad legal: Satia LLC, 8 The Green, Suite B, Dover, Delaware 19901, EE. UU.
