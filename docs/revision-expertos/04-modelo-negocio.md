# Revisión: experto en modelos de negocio basados en tecnología

## 1. Veredicto en una línea
Es un negocio de consultoría con buen gancho tecnológico, pero tal como está planteado no es escalable ni recurrente: los precios no cubren bien las horas senior y el Plan A le resta valor al único ingreso que podría repetirse.

## 2. Lo que funciona
- **Vende un resultado tangible y medible.** Un proceso operando con línea base el día 1 y resultados el día 30 se defiende mejor ante un CFO que un taller o un "piloto de IA". Las empresas medianas pagan por resultados auditables, no por exploración.
- **Elige bien al cliente.** La mediana empresa tiene procesos con dueño, datos en Excel y ERP, y presupuesto para tickets de USD 10.000 o más. Es el segmento que Satia no atiende bien, porque su ticket está pensado para micro y pequeñas empresas.
- **La regla "la IA coordina y el código calcula"** es la decisión técnica correcta. Reduce el riesgo de errores en los KPI y deja la exactitud en scripts verificables (`evals/`), no en el modelo.
- **El catálogo de procesos** es la única palanca real para bajar el costo por entrega. Si el tercer proyecto de cobranzas cuesta la mitad de horas que el primero, el margen mejora con cada cliente.

## 3. Lo que no funciona o es riesgoso
- **El rango de USD 6.000–15.000 se queda corto en la parte baja.** Supuesto: dos personas (un senior y un analista) con unas 220 horas en conjunto, a un costo cargado de USD 35–55 por hora en LatAm, cuestan unos USD 8.000–12.000. A USD 6.000 se pierde dinero. Además, la "operación asistida de 60–90 días" no tiene precio: son dos o tres meses de soporte regalado que se descuentan del margen de la intervención.
- **La mezcla de ingresos es casi toda one-shot.** El Plan A es, en la práctica, "no pagarnos nunca más", y el documento admite que probablemente fracase. Así, cada mes el negocio empieza desde cero y depende del pipeline comercial. Eso se valora como una consultora (más o menos 1x de ingresos), no como un negocio recurrente.
- **El Plan B a USD 500/mes tiene un margen bajo.** Supuesto: entre 6 y 10 horas al mes por cliente (cambios de modelo, conectores MCP que se rompen, rotación de personal, ajustes) más monitoreo cuestan USD 300–550. Con ese costo, cobrar USD 500 deja casi nada.
- **"El repositorio" no es el producto que el cliente va a usar.** Si la interfaz es WhatsApp con el Agent SDK, alguien tiene que alojar la aplicación, pagar la API de Meta, gestionar secretos y responder cuando falla. Eso es software en producción operado por un tercero, con su propia responsabilidad legal y SLA. Esto choca de frente con la idea del Plan A de "lo mantiene el cliente".
- **Hay supuestos débiles:**
    - **Reutilización.** Las cobranzas sobre Siigo en Colombia y sobre SAP B1 en México comparten poco código. Supuesto: la reutilización real es del 30–50 %, no la mayoría.
    - **Propiedad intelectual.** Si el cliente es dueño del repositorio, ¿con qué derecho se reutiliza en el siguiente cliente?
    - **Licencias por usuario.** Supuesto: Claude Team o Enterprise cuesta entre USD 25 y 60 por usuario al mes; con 30 usuarios, el cliente paga más en licencias que a ustedes en el Plan B.
    - **Dependencia de un proveedor.** Todo se apoya en Claude Code, lo que contradice el principio de "agnóstico" del brief.

## 4. Recomendaciones para adaptarlo o hacerlo viable (priorizadas)
1. **Invertir el modelo: setup más suscripción por proceso, no intervención más mantenimiento opcional.** La operación gestionada debe ser el plan por defecto, con un mínimo de 12 meses. El Plan A queda solo como opción premium de traspaso, con un pago de salida.
2. **Precio de setup entre USD 12.000 y 20.000 por proceso del catálogo.** Los procesos fuera del catálogo se cotizan aparte y más caros, o no se aceptan.
3. **Suscripción entre USD 1.200 y 2.500 al mes por proceso**, con alcance escalonado (usuarios, frecuencia de reportes, integraciones). El consumo de IA se cobra con un margen explícito del 20–30 %, como hace Satia con los tokens.
4. **Licenciar, no ceder, la plantilla base.** El cliente es dueño de sus datos y de su configuración; Redesign Lab conserva la propiedad del motor y del catálogo.
5. **Cobrar la operación asistida** dentro del primer trimestre de la suscripción, no como regalo.

**Unit economics por cliente (todos los valores son supuestos):**

| Concepto | Valor |
|---|---|
| Setup | USD 15.000; costo de entrega USD 9.000 (180 h × USD 50) → margen bruto 40 % |
| Suscripción | USD 1.800/mes; costo de servicio USD 600 (8 h más infraestructura) → margen bruto 67 % |
| CAC (diagnóstico subsidiado más ventas) | USD 4.000 |
| Retención | 85 % anual; vida media de unos 30 meses |
| LTV bruto | 6.000 + (1.200 × 30) = USD 42.000 |
| LTV/CAC | aproximadamente 10x |
| Payback | Inmediato con el setup |

**Condición de viabilidad:** que al menos un 60 % de los clientes tome la suscripción. Con una tasa de adopción del 20 %, el LTV/CAC cae por debajo de 3x.

6. **Medir las horas por entrega desde el piloto.** La meta es bajar a 100 horas o menos en el tercer cliente del mismo proceso. Si no se logra, no hay catálogo, solo consultoría a medida.
7. **Elegir dos procesos y dos ERP** para los primeros 12 meses, por ejemplo consolidación de reportes y cobranzas sobre Siigo/Alegra y Excel. Nada más.

## 5. Cómo diferenciarse de soluciones equivalentes
- **Competencia real:**
    - **Plataformas que se implementan con partners:** Microsoft Copilot Studio y Power Automate, Google Gemini Enterprise (antes Agentspace), UiPath con su línea agéntica y Satia.
    - **Agencias de automatización** sobre n8n, Make, Zapier Agents, Relevance AI o Lindy, a menudo con precios de USD 2.000–5.000 por proyecto (supuesto basado en ofertas públicas típicas).
    - **Integradores grandes de la región** con "AI studios" (Globant, Softtek, Accenture), más caros y lentos.
    - **El propio ERP**: Siigo, Alegra o SAP están incorporando IA nativa al software que el cliente ya paga.
- **Dónde está la diferencia defendible:**
    - **El conocimiento del proceso y la medición de impacto**, no la tecnología.
    - **Un catálogo vertical con benchmarks propios de LatAm**: por ejemplo, días de DSO o tiempos de cierre de reportes por industria, construidos con los datos de los clientes. Ninguna plataforma horizontal los tiene.
    - **La gobernanza y el cumplimiento local** de protección de datos (Perú, Colombia, Chile, Brasil, México) como argumento de venta para la mediana empresa.
    - **La garantía por resultado**: parte del setup se condiciona a una mejora pactada del KPI. Las agencias de n8n no pueden ofrecerla porque no miden.
- **Agnosticismo real:** que el motor pueda correr sobre Claude, Gemini o M365. De lo contrario, Microsoft y Google ganan por estar integrados con lo que el cliente ya usa.

## 6. Una pregunta clave que el equipo debe responder
**¿Qué proceso concreto genera, en una empresa mediana típica, un ahorro anual medible de al menos 5 veces lo que pagaría el primer año (unos USD 35.000), y está dispuesto ese cliente a pagar una suscripción para que siga funcionando, en lugar de llevarse el repositorio?** Si en 3 a 5 conversaciones no aparece un "sí" a ambas partes, el modelo es consultoría pura y debe valorarse y dimensionarse como tal.

*No hice búsquedas web: los precios de licencias, los costos por hora y los rangos de la competencia salen de mi conocimiento y son supuestos que hay que confirmar.*
