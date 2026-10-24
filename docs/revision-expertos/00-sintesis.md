# Revisión de expertos: síntesis

> 24-oct-2026 · Evaluación de `docs/analisis-idea-intervencion.md` por siete especialistas simulados (revisores de IA con roles asignados, no personas reales). Las revisiones completas están en esta carpeta. Las cifras de precios, leyes y productos de terceros son supuestos de los revisores y deben verificarse.

## Veredicto

**La idea es viable y diferenciada, pero como servicio gestionado y no como "repositorio que el cliente mantiene".** Los siete coinciden: el valor está en el conocimiento del proceso y en resultados medidos, no en la tecnología. El modelo actual promete demasiado en 30 días, cobra poco y deja al cliente solo.

| Experto | Veredicto en una línea |
|---|---|
| [IA aplicada](01-ia.md) | Viable como servicio gestionado de un proceso acotado; confunde la herramienta para construir con el sistema que opera |
| [Medianas empresas LatAm](02-medianas-latam.md) | Tesis correcta; subestima la fricción de compra, legal y tributaria, y elige un piloto de ROI débil |
| [Branding B2B de IA](03-branding-b2b-ia.md) | Buen servicio sin posicionamiento: vende cómo se construye, no qué compra el gerente |
| [Modelo de negocio](04-modelo-negocio.md) | Consultoría con gancho tecnológico; ni escalable ni recurrente con estos precios |
| [Consultoría](05-consultoria.md) | Sólido como servicio administrado; el mes alcanza para construir, no para que se adopte |
| [ERP](06-erp.md) | Viable como rediseño de procesos alrededor del ERP; subestima el acceso a datos y la IA nativa |
| [Storytelling](07-storytelling.md) | Buena materia prima, pero la protagonista es la tecnología y no el problema del gerente |

## Lo que funciona (consenso)

1. **Entregar un sistema funcionando, no un informe.** Saca la oferta de la consultoría comoditizada (7 de 7).
2. **Línea base el día 1 y resultado el día 30.** Es el activo de marca más valioso: cada cliente se vuelve una prueba (7 de 7).
3. **"La IA coordina, el código calcula".** Hace los números auditables ante un CFO (6 de 7).
4. **Catálogo de procesos.** Es la única palanca para bajar el costo de cada entrega (6 de 7).
5. **Excel y WhatsApp como cara visible.** El usuario no cambia su forma de trabajar (5 de 7).
6. **Gobernanza como argumento de venta:** registro de acciones y aprobación humana (5 de 7).

## Lo que no funciona (consenso)

| # | Problema | Quiénes lo señalan |
|---|---|---|
| 1 | **El Plan A es casi ficción.** La mediana empresa no tiene quién mantenga agentes, conectores y evals; el sistema se degrada en 3 a 6 meses y la reputación la paga la marca | 7 de 7 |
| 2 | **"30 días" es una promesa engañosa.** Accesos, contratos de datos y aprobaciones de TI consumen de 2 a 4 semanas; con la adopción, el recorrido real es de unos 90 a 120 días | 6 de 7 |
| 3 | **"Agnóstico, sin dependencia" no es creíble** si todo se construye sobre Claude Code y el Agent SDK | 6 de 7 |
| 4 | **Precios bajos y casi todo one-shot.** USD 6.000 pierde dinero; el Plan B a USD 500/mes no paga guardias; la operación asistida va regalada | 5 de 7 |
| 5 | **Conflicto de propiedad intelectual.** Si el cliente es dueño del repositorio, no se puede reutilizar en el siguiente | 5 de 7 |
| 6 | **No es un repositorio, es software en producción.** Recordatorios y mensajes a 20 usuarios exigen alojamiento, monitoreo, SLA y responsabilidad legal | 4 de 7 |
| 7 | **Las integraciones con ERP locales están inmaduras.** No hay MCP oficiales para Siigo, Alegra, Contpaqi o Defontana; la integración puede comerse medio mes | 4 de 7 |
| 8 | **El mensaje usa jerga técnica** (repositorio, MCP, agentes) y protagoniza la herramienta, no al cliente | 3 de 7 |
| 9 | **Falta la gestión del cambio.** Sin sponsor con autoridad ni rituales de uso, los recordatorios se vuelven ruido | 3 de 7 |
| 10 | **Riesgos no tratados:** retenciones tributarias a servicios del exterior, leyes de datos nuevas (México 2025, Chile 21.719), políticas de Meta para IA en WhatsApp, inyección de instrucciones vía correos externos | 2 de 7 |

## Recomendaciones (priorizadas)

1. **Invertir el modelo: implementación + suscripción por proceso.** El servicio gestionado es el plan por defecto; el Plan A solo para clientes con equipo técnico verificado y con un pago de traspaso.
2. **Reformular la promesa:** "30 días para que funcione, 90 para que se quede". Fases: precondiciones firmadas (accesos, acuerdo de datos, sponsor) → construcción de 4 semanas → adopción de 6 a 8 semanas, incluida en el precio.
3. **Revisar precios (hipótesis de los revisores):** implementación de USD 12.000–20.000 por proceso del catálogo y suscripción de USD 1.200–2.500 al mes. El consumo de IA se cobra aparte y transparente. Condición de viabilidad: que al menos el 60 % de los clientes tome la suscripción.
4. **Separar la propiedad intelectual en el contrato:** el cliente es dueño de sus datos y su configuración; Redesign Lab conserva el motor y el catálogo bajo licencia.
5. **Diagnóstico de integrabilidad antes de vender:** ERP, versión, API disponible, partner del ERP y credenciales de solo lectura. Sin acceso de lectura en 5 días, no se firma.
6. **Empezar en solo lectura + propuestas.** El agente prepara (borradores, listas, conciliaciones sugeridas) y una persona ejecuta. Escribir en el ERP queda para una fase 2.
7. **Acotar el foco de los primeros 12 meses:** 2 procesos, 2 o 3 ERP y 2 países con la facturación resuelta.
8. **Arquitectura para operar, no solo para construir:** Agent SDK alojado, orquestador determinista, base de datos como fuente de verdad, trazas y evals contractuales (30 a 50 casos de referencia).
9. **Gestión del cambio con nombre propio:** sponsor, campeones por área, rituales de uso y KPI de adopción semanales.
10. **Mensaje sin jerga y con el cliente como protagonista.** Glosario externo: repositorio → "el manual vivo del proceso"; agentes → "asistentes que piden, revisan y avisan"; MCP → "conexión con los sistemas que ya usas".
11. **Convertir al partner del ERP en aliado** (co-entrega o reparto de ingresos), no en un obstáculo.
12. **Contar el piloto fallido como "caso 0"** en cuatro partes: qué creíamos, qué hicimos, qué falló (con un dato) y qué cambiamos.

## Dónde no hay acuerdo

| Tema | Postura A | Postura B |
|---|---|---|
| **Proceso piloto** | Consolidación de reportes: bajo riesgo, solo lectura y sin depender de ERP locales (IA, ERP) | Cobranzas o conciliación bancaria: mueven dinero visible y justifican el precio (medianas, modelo de negocio) |
| **Interfaz inicial** | Correo + Excel/Teams en el piloto; WhatsApp en una segunda fase vía proveedor oficial (IA) | WhatsApp desde el inicio, con aprobación humana (medianas, branding) |
| **Ecosistema por defecto** | Microsoft 365, donde vive la mayoría de la mediana empresa regional (medianas) | Según el partnership de nube de Redesign Lab (brief original) |

**Propuesta para resolver el piloto:** hacer primero la consolidación de reportes como "plantilla 0" interna, para medir horas reales y probar la arquitectura, y ofrecer cobranzas como primer producto comercial, con un KPI en dinero (DSO, cartera vencida).

## Cómo diferenciarse

| Frente a | Competidores mencionados | Nuestra diferencia |
|---|---|---|
| Grandes consultoras e integradores | Accenture, Big Four, Globant (AI Pods), Softtek, Stefanini, NTT Data | Precio cerrado, ticket de mediana empresa, velocidad y KPI garantizado |
| Plataformas de agentes y no-code | Microsoft Copilot Studio, Google Gemini Enterprise, Zapier Agents, n8n, Make, Relevance AI, Lindy, UiPath | Rediseño del proceso antes de automatizar y responsabilidad por el resultado |
| Plataformas conversacionales de la región | Satia, Treble, Botmaker, Blip, Yalo | Procesos internos de back-office (finanzas, compras), donde ellas no entran |
| IA nativa del ERP | Copilot de Business Central, NetSuite, Odoo AI, SAP Business AI, TOTVS Carol | Trabajo transversal entre ERP, Excel, correo y personas; activar lo nativo como "quick win" |
| Agencias y freelancers de automatización | Ecosistema n8n y Make en la región | Metodología, evals, gobernanza y casos publicados con cifras |
| El cliente configurando Claude o Copilot por su cuenta | — | Conocimiento del proceso, medición y operación gestionada con SLA en español |

**Ventaja defendible a largo plazo:** una biblioteca pública de casos con línea base y resultado en dinero, un catálogo vertical con benchmarks propios de LatAm (días de cobranza, tiempos de cierre por industria) y un nicho donde Redesign Lab ya tiene autoridad: **reportes de impacto y ESG**.

## Territorios de posicionamiento (branding)

| Territorio | Idea | Arquitectura de marca |
|---|---|---|
| A. "Procesos que se operan solos" | Resultado operativo medido en horas, errores y dinero | Probablemente marca independiente |
| B. "Tu sistema, tu propiedad" | Soberanía y control: datos y conocimiento quedan en la empresa | Cualquiera |
| C. "Rediseño con evidencia" | Apalanca *Redesign* y su credibilidad metodológica; nicho de impacto y ESG | Marca respaldada: "X by Redesign Lab" |

Frases centrales propuestas: *"Tu proceso más lento, funcionando y medido en 30 días."* · *"Tu equipo deja de perseguir Excels: el sistema pide, revisa y reporta."* · *"Un mes para ordenar un proceso. Un tablero para demostrarlo."*

## La pregunta de fondo

Cuatro de los siete expertos llegan, por caminos distintos, a la misma decisión pendiente:

> **¿Redesign Lab quiere ser una consultora (proyecto con fin, el cliente es dueño) o un operador de servicio (suscripción recurrente, nosotros respondemos cuando algo falla)?**

El contrato, el precio, el equipo, la marca y la definición de éxito cambian según la respuesta. Hoy la propuesta intenta ser las dos cosas a la vez.

Otras preguntas abiertas de los expertos:
- ¿Qué proceso genera un ahorro de al menos 5 veces lo que el cliente pagaría el primer año (unos USD 35.000)?
- ¿Para qué 2 o 3 ERP y en qué país garantizamos acceso de lectura en la primera semana?
- ¿Qué número concreto debía cambiar en el piloto fallido y por qué no cambió?
- ¿Quién opera el sistema el día 91 y quién paga por ello?
