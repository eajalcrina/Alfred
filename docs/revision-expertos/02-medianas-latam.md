# Revisión: experto en empresas medianas de América Latina

## 1. Veredicto en una línea
La tesis es correcta: la mediana empresa compra resultados implementados, no plataformas. Pero el plan subestima la fricción de compra, legal y tributaria de la región, sobreestima la capacidad interna para el Plan A, y elige como piloto el proceso con el ROI menos defendible.

## 2. Lo que funciona
- **Encaja con cómo compra la mediana empresa.** El gerente general o el dueño (en muchos casos empresa familiar) desconfía de las plataformas self-service y de los pilotos sin fin. Un precio cerrado, un plazo fijo y un entregable visible se aprueban más fácil que un SaaS por consumo.
- **Excel y WhatsApp como interfaz.** Es un acierto. La operación real de la región pasa por planillas y grupos de WhatsApp, no por un CRM.
- **"La IA coordina y el código calcula".** Es lo que permite defender los números ante un CFO o un auditor externo.
- **El catálogo de procesos** es la única vía para que el margen aguante con horas senior a 6.000–15.000 USD.
- **Medir la línea base el día 1.** En la región casi nadie mide antes, así que los consultores no pueden probar impacto. Medir es diferenciador por sí solo.

## 3. Lo que no funciona o es riesgoso
- **Un mes no alcanza para el ciclo completo.** En una mediana empresa, el NDA, el acuerdo de tratamiento de datos, la aprobación de TI para dar acceso al ERP o al correo y la agenda de usuarios clave consumen 2 a 4 semanas antes de tocar un dato. El "diagnóstico de 1 semana" no lo resuelve: el reloj debe empezar cuando hay accesos, no cuando se firma.
- **El Plan A es casi ficción.** Las áreas de TI medianas (de 1 a 5 personas) dan soporte, operan el ERP y la red. No mantienen prompts, skills ni conectores MCP. El documento lo intuye, pero sigue ofreciendo A como opción principal. Debería ser la excepción.
- **El ROI por "horas ahorradas" es débil en la región.** Un analista junior cuesta aproximadamente 600–1.500 USD al mes según el país (supuesto, varía mucho). Si suman las licencias de Claude por usuario, el consumo y el Plan B, el sistema puede costar más que la persona que reemplaza. El caso de negocio debe expresarse en dinero de caja (DSO, multas evitadas, días de cierre), no en horas.
- **El piloto propuesto es el más débil.** La consolidación de reportes ahorra fricción, pero rara vez mueve dinero visible. Cobranzas o conciliación bancaria sí lo hacen.
- **Faltan la fricción tributaria y la de facturación.** Supuesto a verificar con un tributarista. Facturar servicios desde el exterior activa retenciones a no domiciliados: alrededor del 30 % en Perú, 20 % en Colombia por servicios técnicos y montos relevantes en México y Chile. El cliente exige además factura electrónica local para deducir el gasto. Sin entidad o socio de facturación por país, el precio efectivo cambia o la venta se cae.
- **El riesgo regulatorio está tratado como una casilla.** La nueva LFPDPPP de México (2025) y la Ley 21.719 de Chile (con vigencia escalonada) endurecen las reglas, y la transferencia internacional de datos hacia EE. UU. exige cláusulas específicas. Además, un repositorio con entrevistas y datos personales en git es un pasivo, no solo un activo.
- **La dependencia de WhatsApp no está resuelta.** Claude no trae WhatsApp nativo. Hace falta un BSP (Twilio, 360dialog u otro) y cumplir la política de Meta de 2026, que restringe los asistentes de IA de propósito general en la API de WhatsApp Business. Los bots acotados a una tarea siguen permitidos (verificar el texto vigente).
- **Hay un sesgo hacia Google Workspace.** Asumo que gran parte de la mediana empresa regional vive en Microsoft 365 (Excel, Outlook, Teams). El stack MCP por defecto debería priorizarlo.
- **Faltan ERPs clave.** Brasil se rige por TOTVS, Sankhya y Omie; Argentina por Tango; México por Aspel; Perú usa Starsoft y Concar. Brasil exige además portugués, LGPD y un ciclo de venta propio: no debería estar en la primera ola.
- **Conflicto de propiedad intelectual.** "El repositorio del cliente X sirve para el cliente Y" choca con la confidencialidad que exigirá cualquier gerente legal. Hay que separar en el contrato el framework (propiedad de Redesign Lab) de la configuración y los datos (propiedad del cliente).
- **Resistencia cultural.** Un agente que "persigue" a gerentes pidiendo información será ignorado si no tiene detrás la autoridad explícita del sponsor. A eso se suma el temor a ser reemplazado en mandos medios.

## 4. Recomendaciones para adaptarlo o hacerlo viable (en orden)
1. **Cambiar el piloto a cobranzas o conciliación**, con un KPI en dinero (DSO, cartera vencida mayor a 60 días) y precio parcialmente variable atado a ese resultado.
2. **Redefinir las fases:** precondiciones (accesos, DPA, sponsor y dueño interno firmados) antes de iniciar los 30 días; operación asistida de 60–90 días incluida en el precio.
3. **Volver obligatorio el Plan A+ o el B**, y dejar el Plan A solo para clientes con un equipo técnico verificado.
4. **Empezar por 2 países** con estructura de facturación resuelta: México y Colombia (mercado y madurez) o Perú, si allí está la red de Redesign Lab. Precio en USD con opción en moneda local.
5. **Stack por defecto Microsoft 365 + Excel**, con Google como alternativa y WhatsApp a través de un BSP con aprobación humana.
6. **Explorar cofinanciamiento público** (CORFO en Chile, iNNpulsa en Colombia, ProInnóvate en Perú). Supuesto: verificar las convocatorias vigentes. Reduce el ticket que percibe el cliente.
7. **Contrato con propiedad intelectual separada** (framework frente a configuración) y una cláusula de portabilidad.

## 5. Cómo diferenciarse de soluciones equivalentes
- **Consultoras grandes y tecnológicas** (Big 4, Accenture, Globant con sus AI Pods, Softtek, Stefanini): son caras y lentas para un ticket de mediana empresa. Diferenciación: precio cerrado, 30 días y KPI garantizado.
- **Partners de Microsoft (Copilot Studio + Power Automate) y de UiPath:** competencia directa en clientes con M365. Diferenciación: rediseño del proceso y no solo la automatización; independencia del proveedor de IA.
- **Plataformas conversacionales regionales** (Satia, Treble, Botmaker, Yalo): están centradas en ventas y atención por WhatsApp. Diferenciación: procesos internos de back-office (finanzas, compras), donde ellas no entran.
- **IA dentro del propio ERP** (Siigo, Alegra, TOTVS) y **freelancers de n8n o Make:** más baratos. Diferenciación: gobernanza, auditoría, evals y responsabilidad contractual por el resultado.
- **La ventaja defendible** es un catálogo de procesos financieros con evidencia publicada de casos en dinero. "Usamos Claude Code" no lo es: se copia en semanas.

## 6. Una pregunta clave que el equipo debe responder
¿Qué ejecutivo con presupuesto propio, en cuál de los países objetivo, pagaría 10.000 USD más un mantenimiento mensual por mover qué indicador en dinero, y quién en su empresa será dueño del sistema el día 91?
