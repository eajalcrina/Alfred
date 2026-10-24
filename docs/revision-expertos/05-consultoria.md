# Revisión: experto en consultoría de gestión y transformación

## 1. Veredicto en una línea
La idea es sólida como servicio administrado. Como "intervención de un mes" con Plan A es frágil: el mes alcanza para construir el sistema, pero no para que la empresa lo adopte.

## 2. Lo que funciona
- **El entregable es un sistema que opera, no un informe.** Con eso se sale de la consultoría de diagnóstico, que es la parte más comoditizada del mercado, y la conversación de venta pasa de "recomendaciones" a "resultados medibles".
- **La regla "IA coordina, código calcula" y el uso de `evals/`** muestran criterio de ingeniería. Pocas boutiques de IA en la región separan la exactitud de los KPI del modelo. Ese argumento convence a un gerente de finanzas.
- **Un proceso por intervención, con un catálogo**, es la forma correcta de escalar una boutique: se cobra cada vez menos por el diseño y cada vez más por la configuración. Es el mismo camino que siguieron las firmas de implementación de ERP.
- **Hay un ancla en Excel y WhatsApp.** Pedirle al usuario que cambie de canal es la principal causa de abandono en la mediana empresa latinoamericana. Diseñar sobre las herramientas que ya usa reduce la resistencia.
- **El Plan B genera ingreso recurrente.** Una boutique que vive solo de proyectos tiene un flujo de caja inestable.

## 3. Lo que no funciona o es riesgoso
- **Un mes no es realista para lo que promete la frase de venta.** Levantar el proceso, investigarlo, rediseñarlo, construir, integrar y capacitar suman, siendo optimistas, entre 6 y 10 semanas en una empresa mediana. El cuello de botella no es Claude Code. Son los accesos a datos, las aprobaciones de TI y seguridad, la disponibilidad de los usuarios clave y los datos sucios. Mi supuesto: entre la semana 1 y la 2 se pierde tiempo esperando credenciales y archivos.
- **La gestión del cambio casi no aparece en el documento.** Un sistema que "solicita información y hace recordatorios" cambia quién responde a quién. Sin un patrocinador con autoridad, sin rediseño de roles y sin un ritual de uso (por ejemplo, el cierre semanal pasa por el sistema), los usuarios lo ignoran. Las alertas por WhatsApp que nadie atiende se vuelven ruido en pocas semanas.
- **El Plan A es un supuesto débil.** Mantener un repositorio con agentes, MCP, scripts en Python y evals exige un perfil técnico que la mediana empresa típica no tiene. Lo más probable es que el sistema se degrade en 3 a 6 meses y que la reputación la pague la firma.
- **Dependencia de proveedor no reconocida.** El documento sostiene que no hay dependencia, pero el entregable está atado a Claude Code o Cowork, a licencias por usuario y a la madurez de los conectores MCP. Supuesto: hoy no existen MCP oficiales y estables para Siigo, Contpaqi, Defontana ni para la facturación electrónica local, así que habrá que construirlos y mantenerlos.
- **Propiedad intelectual en conflicto.** El plan quiere que "cada intervención cree un activo reutilizable", pero el cliente que paga 15.000 USD esperará ser dueño del repositorio. Si el contrato no lo resuelve, el modelo de catálogo no funciona.
- **El precio no cuadra con el esfuerzo.** Entre 6.000 y 15.000 USD por 4 semanas de trabajo senior, más 60 a 90 días de operación asistida "obligatoria", deja un margen bajo o negativo en los primeros clientes.
- **La métrica de éxito no es la correcta.** Las horas ahorradas al día 30 dicen poco. Lo que predice la renovación es el uso real (usuarios activos, porcentaje del proceso que pasa por el sistema).

## 4. Recomendaciones para adaptarlo o hacerlo viable (priorizadas)
1. **Reestructurar la oferta en 90 días con hitos de decisión:** diagnóstico pagado de 1 a 2 semanas, construcción de 4 semanas y adopción de 6 a 8 semanas. Hay que vender "30 días a producción", no "30 días a transformación".
2. **Hacer del Plan B (o el A+) la opción por defecto** y permitir el Plan A solo si el cliente pasa una certificación de preparación: un dueño interno técnico con tiempo asignado y un traspaso documentado.
3. **Poner cláusulas de dependencia del cliente en el contrato:** accesos listos al día 5, un dueño del proceso con al menos 30 % de dedicación y aprobaciones de TI con plazo. Si el cliente no cumple, el reloj del proyecto se detiene.
4. **Resolver la propiedad intelectual:** el cliente es dueño de su instancia y de sus datos, y Redesign Lab conserva las plantillas base y los patrones con licencia de uso.
5. **Construir la "plantilla 0" internamente antes de vender**, con un proceso horizontal (consolidación de reportes o cobranzas) y medir cuánto toma de verdad.
6. **Integrar la gestión del cambio como componente con nombre propio:** un patrocinador, campeones por área, un mapa de cambios de rol y rituales de uso. Los KPI de adopción se revisan cada semana.
7. **Separar en la propuesta tres partidas:** honorarios, licencias o consumo de IA y conectores a medida. Así se evita que el cliente perciba sobreprecio.

## 5. Cómo diferenciarse de soluciones equivalentes
Las alternativas reales del mercado son:
- **Integradores grandes:** Globant, con sus AI Pods por suscripción; Accenture, Deloitte y NTT Data, con ofertas de IA agéntica; Softtek y Stefanini en la región.
- **Plataformas con red de implementadores:** Satia y sus partners, Microsoft Copilot Studio y Power Automate a través de sus partners, y Google Agentspace.
- **Agencias de automatización** que trabajan sobre n8n o Make.

Los integradores grandes no bajan a tickets de 15.000 USD con profundidad de proceso. Las agencias de n8n entregan automatizaciones sin rediseño ni gobernanza. La diferenciación defendible es:
- **Profundidad en el proceso por vertical**, con línea base y resultados publicados. Hoy casi nadie publica casos con cifras en LatAm (supuesto razonable).
- **Garantía ligada a resultados:** parte del honorario variable según KPI de adopción o de tiempo de ciclo.
- **Gobernanza y exactitud auditables** (log de acciones, evals, KPI calculados con código) como argumento frente a "chatbots que inventan números".
- **Neutralidad real:** documentar el proceso en un formato que pueda migrar a otra plataforma, y no solo afirmarlo.

## 6. Una pregunta clave que el equipo debe responder
¿Venden una transformación de proceso (proyecto con fin y el cliente como dueño) o un "empleado digital" administrado (servicio recurrente del que la firma es responsable)? El contrato, el precio, el equipo y la definición de éxito cambian por completo según la respuesta, y hoy el documento intenta ser las dos cosas a la vez.
