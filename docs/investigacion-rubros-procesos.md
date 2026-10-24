# Adopción de "sistemas de IA por piezas" en empresas medianas de LatAm: rubros, procesos, rutas y precio

> 24-oct-2026 · Investigación de apoyo a `docs/tesis-v02.md`. Restricciones: sin integraciones a ERP ni a plataformas del Estado; sin ESG; solo procesos internos de alto valor. Todo lo marcado **[Supuesto]** es criterio experto sin fuente.

## 0. Qué dicen los datos (en breve)

- **La mediana empresa ya usa IA, pero casi ninguna la tiene integrada a sus procesos.** Según Microsoft, el 88 % de las medianas colombianas ya usa IA y las mipymes destinan en promedio el 29 % de su presupuesto tecnológico a IA. Los beneficios más citados son ahorro de tiempo (58 %), productividad (52 %) y menos errores humanos (41 %) ([ITSitio/Microsoft](https://www.itsitio.com/co/?p=177284)). La encuesta de IDC para Lenovo da otro cuadro: el 65 % de las empresas latinoamericanas está en etapa temprana y solo el 5 % adoptó la IA de forma sistemática. Las barreras que reporta son datos de mala calidad y la dificultad de integrar la IA a los procesos existentes ([DPL News](https://dplnews.com/?p=269676)).
- **El problema es "cómo", no "si".** El 34 % no tiene claro cómo integrar la IA y el 26 % no encuentra talento. La mediana empresa muestra "confianza considerable", mientras que la pequeña está más dividida ([SAP](https://news.sap.com/latinamerica/2025/06/el-poder-transformador-de-la-ia-en-america-latina/)).
- **El valor aparece cuando se rediseña el flujo de trabajo.** McKinsey (2025) reporta que el 88 % de las organizaciones usa IA, pero casi dos tercios no la ha escalado y solo el 39 % ve impacto en el EBIT. Las que capturan valor son las que rediseñan sus procesos ([IT Brief / McKinsey](https://itbrief.co.uk/story/mckinsey-report-shows-ai-interest-but-slow-scaling)). Esto respalda la tesis de vender procesos instalados y no licencias.
- **La base digital es frágil.** Más del 70 % de las mipymes no tiene presencia en internet ([CEPAL vía DPL News](https://dplnews.com/?p=237636)). En Perú, los servicios van "dos o tres pasos adelante" y la industria pesada (construcción, agro, minería) va atrás ([El Peruano](https://www.elperuano.pe/noticia/292915-peru-avanza-en-adoptar-la-inteligencia-artificial)).

**Lectura:** el comprador ideal ya probó ChatGPT o Copilot, vio el potencial y no sabe convertirlo en un proceso que funcione solo. Ese hueco es exactamente la oferta. **[Supuesto]**

---

## 1. Rubros más abiertos

Escala de 1 a 5. Para "madurez mínima", 5 significa que basta con Excel y WhatsApp. Para "facilidad sin ERP", 5 significa que el proceso vive casi entero fuera del ERP. Las puntuaciones son **[Supuesto]** de criterio experto.

| # | Rubro | Dolor | Disposición a pagar | Madurez mínima | Sin ERP | Total |
|---|---|---|---|---|---|---|
| 1 | **Distribución y comercialización B2B** (consumo masivo, ferretería, insumos, repuestos) | 5 | 4 | 4 | 4 | **17** |
| 2 | **Constructoras y contratistas medianos** (obra civil, montaje, instalaciones) | 5 | 4 | 4 | 5 | **18** |
| 3 | **Servicios de campo y tercerización intensiva en personal** (mantenimiento, seguridad, limpieza, facility) | 5 | 4 | 4 | 5 | **18** |
| 4 | Logística y transporte de carga (3PL, flotas) | 5 | 3 | 3 | 4 | 15 |
| 5 | Manufactura liviana (alimentos, plásticos, envases) | 4 | 4 | 3 | 3 | 14 |
| 6 | Agroindustria y agroexportación | 4 | 4 | 3 | 4 | 15 |
| 7 | Salud ambulatoria privada (clínicas, laboratorios, odontología en cadena) | 4 | 3 | 3 | 3 | 13 |
| 8 | Importadoras | 4 | 4 | 4 | 4 | 16 |
| 9 | Servicios profesionales B2B (ingeniería, agencias, despachos) | 3 | 3 | 5 | 5 | 16 |
| 10 | Retail y restaurantes con varios locales o franquicias | 4 | 3 | 3 | 3 | 13 |
| 11 | Educación privada (colegios, institutos) | 3 | 3 | 4 | 4 | 14 |

### Detalle por rubro

**1. Distribución B2B.**
- *Por qué está abierta:* márgenes de un dígito, cientos de clientes con crédito y pedidos por WhatsApp. Los vendedores rotan y se llevan la cartera en la cabeza. En México, el 48 % de las facturas B2B se paga tarde, con 38 días de atraso promedio, y los incobrables suben al 6 % de las ventas a crédito ([Atradius](https://atradius.us/knowledge-and-research/reports/b2b-payment-practices-trends-mexico-2024)).
- *Qué la frena:* el inventario y los precios viven en el ERP; para trabajar sin integración hay que usar exportaciones a Excel.
- *Tamaño típico:* USD 5–50 M de facturación y 30–200 empleados.
- *Quién compra:* gerente general/dueño o gerente de finanzas.

**2. Constructoras y contratistas.**
- *Por qué está abierta:* cada obra es una "mini empresa" que se coordina por WhatsApp, Excel de presupuesto y fotos. Hay sobrecostos, valorizaciones o estimaciones atrasadas y vencimientos de pólizas y permisos.
- *Qué la frena:* cultura de obra poco digital y ciclos ligados a licitaciones.
- *Tamaño típico:* USD 5–40 M.
- *Quién compra:* gerente general, gerente de proyectos o controller.

**3. Servicios de campo y tercerización.**
- *Por qué está abierta:* cientos de técnicos o guardias, alta rotación, órdenes de trabajo en papel o WhatsApp, multas contractuales por SLA y vencimientos de certificaciones.
- *Qué la frena:* márgenes estrechos y presión sobre el precio.
- *Tamaño típico:* 100–1.500 empleados con USD 3–30 M de facturación.
- *Quién compra:* gerente de operaciones o gerente general.

**4. Logística y transporte.**
- *Por qué está abierta:* los costos logísticos equivalen al 18–35 % del valor del producto en la región, frente al 8 % en la OCDE (cifra del BID, citada en fuentes secundarias). Hay que conciliar guías, viajes, combustible y mantenimiento de flota.
- *Qué la frena:* muchos ya usan TMS o GPS y tienen poca caja.
- *Quién compra:* gerente de operaciones.

**5. Manufactura liviana.**
- *Por qué está abierta:* hay mermas, programación de producción en Excel y compras de insumos.
- *Qué la frena:* la planta exige datos de máquinas o del ERP, lo que vuelve más difícil trabajar sin integración.
- *Quién compra:* gerente de planta o de finanzas.

**6. Agroexportación.**
- *Por qué está abierta:* tiene picos de mano de obra (planillas por destajo), certificaciones con auditorías y trazabilidad documental.
- *Qué la frena:* la estacionalidad y que las operaciones están en zonas rurales.
- *Quién compra:* gerente de operaciones o administración.

**7. Salud ambulatoria.**
- *Por qué está abierta:* hay agendas, liquidación de honorarios médicos, cobranza a aseguradoras e inventario de insumos.
- *Qué la frena:* datos sensibles y regulación, y que el software clínico ya cubre parte.
- *Quién compra:* gerente administrativo.

**8. Importadoras.**
- *Por qué está abierta:* hay que seguir órdenes de compra, embarques, documentos de proveedores y costeo de importación en Excel.
- *Qué la frena:* el ciclo es largo y depende de agentes externos.
- *Quién compra:* gerente de comercio exterior o finanzas.

**9. Servicios profesionales.**
- *Por qué está abierto:* hay control de horas, rentabilidad por proyecto y facturación de hitos. Su madurez digital es alta.
- *Qué lo frena:* el dolor en dinero es menor y tienden a "hacerlo ellos mismos" con herramientas genéricas.
- *Quién compra:* socio director.

**10. Retail y restaurantes multi-local.**
- *Por qué está abierto:* cuadres de caja, mermas, turnos y checklists de apertura.
- *Qué lo frena:* el POS ya trae reportes y el ticket es bajo por local.
- *Quién compra:* gerente de operaciones.

**11. Educación privada.**
- *Por qué está abierta:* cobranza de pensiones, matrícula y comunicación con apoderados.
- *Qué la frena:* la estacionalidad y presupuestos rígidos.
- *Quién compra:* administrador o promotor.

### Los 3 rubros recomendados para empezar

1. **Constructoras y contratistas.** El proceso ya vive fuera de cualquier ERP: obra, documentos, fotos y WhatsApp. El dolor se mide en sobrecostos y multas, y el tablero por obra se ve en pocas semanas. **[Supuesto]**
2. **Servicios de campo y tercerización.** Tienen mucha coordinación de personas, es decir, recordatorios, evidencias y vencimientos, que es justo lo que el sistema hace mejor. El costo de no cumplir es contractual y medible (multas por SLA, renovaciones). **[Supuesto]**
3. **Distribución B2B.** Es el mayor volumen de empresas medianas y tiene el dolor más universal, la cobranza, que se ataca con un simple reporte de antigüedad exportado a Excel, sin integrar el ERP. Abre naturalmente el flujo de caja y luego el área comercial. **[Supuesto]**

Los tres comparten el mismo comprador: el gerente general o de operaciones de una empresa con dueño presente que decide en una o dos reuniones. **[Supuesto]**

---

## 2. Procesos internos de mayor interés

"Sin integración" no significa "sin datos". Los datos entran por exportaciones a Excel, correos reenviados, formularios, fotos o mensajes de WhatsApp. Los KPI en dinero son **[Supuesto]** salvo cuando se indica una fuente.

| # | Proceso | Problema típico | Qué hace el sistema | Entradas | KPI de valor | Rubros donde más duele | Complejidad |
|---|---|---|---|---|---|---|---|
| P1 | **Cobranza y cuentas por cobrar** | Cartera vencida sin seguimiento sistemático; el vendedor "se olvida" | Pide el reporte de antigüedad semanal, prioriza clientes, redacta recordatorios con el tono adecuado, registra promesas de pago, alerta por incumplimientos y genera el tablero de DSO | Excel exportado, correos, WhatsApp | −5 a −15 días de DSO. Con USD 10 M de ventas, 10 días de DSO liberan unos USD 274.000 de capital de trabajo | Distribución, importadoras, servicios, educación | Baja |
| P2 | **Flujo de caja de 13 semanas** | La caja se arma a mano el viernes y nadie confía en ella | Consolida cuentas por cobrar, cuentas por pagar, planillas y compromisos; pide supuestos a los responsables, compara proyección vs. real y alerta por quiebres | Extractos y Excel de CxC/CxP, correos | Evita sobregiros y créditos caros; 4–8 h semanales del contador | Todos | Media |
| P3 | **Requisiciones y aprobación de compras** | Compras por WhatsApp sin presupuesto ni aprobación | Recibe la solicitud por chat, valida contra presupuesto, pide 2–3 cotizaciones, arma el comparativo, enruta la aprobación y deja registro | WhatsApp, PDF de cotizaciones, Sheets de presupuesto | Ahorro del 3–8 % en compras no estratégicas y trazabilidad | Construcción, manufactura, servicios | Media |
| P4 | **Rendición de gastos, viáticos y caja chica** | Boletas en fotos, rendiciones atrasadas, fugas | Recibe fotos de boletas, extrae datos, valida política, consolida, alerta por anticipos sin rendir y genera el Excel contable | Fotos, WhatsApp, Excel | 50–70 % menos tiempo de rendición; detección de gastos fuera de política | Servicios de campo, construcción, distribución | Baja |
| P5 | **Control de obra o proyecto (presupuesto vs. real y avance)** | El presupuesto vive en un Excel que nadie actualiza y el sobrecosto se descubre al final | Pide avance semanal y fotos al residente, consolida costos, calcula desviación y margen proyectado, alerta y genera el informe al cliente o al directorio | Excel, fotos, WhatsApp, guías | 1–3 puntos de margen protegidos por obra | Construcción, ingeniería, instalaciones | Media |
| P6 | **Control documental y vencimientos** (pólizas, contratos, certificaciones, licencias, documentos de vehículos y personal) | Multas, bloqueos en el ingreso a cliente o mina, seguros vencidos | Mantiene el registro, recuerda a 60/30/7 días, pide el documento renovado, valida que llegó y emite un semáforo por cliente o sede | PDF, correo, WhatsApp | Multas y paralizaciones evitadas; horas de asistente | Servicios de campo, logística, construcción, agro | Baja |
| P7 | **Órdenes de trabajo y reportes de servicio en campo** | Técnicos reportan por WhatsApp sin evidencia y la facturación se atrasa | Crea la orden, pide check-in, fotos y firma, arma el informe para el cliente, alerta por SLA en riesgo y libera la facturación | WhatsApp, fotos, formularios | Facturación 5–10 días antes; multas por SLA evitadas | Mantenimiento, facility, telecom, seguridad | Media |
| P8 | **Toma y consolidación de pedidos por WhatsApp** | Pedidos en chats personales de vendedores, con errores de digitación | Interpreta el pedido, valida contra la lista de precios en Excel, confirma con el cliente y consolida para despacho | WhatsApp, Excel de precios y stock | Menos errores de pedido y 1–2 h diarias por vendedor | Distribución, alimentos | Media |
| P9 | **Seguimiento de cotizaciones y pipeline** | Se cotiza y no se hace seguimiento; no hay pronóstico de ventas | Registra cotizaciones enviadas, recuerda el seguimiento, pide estado al vendedor y genera el pronóstico semanal | Correo, PDF, Sheets | +3–5 puntos de tasa de cierre | Distribución, importadoras, B2B, construcción | Baja |
| P10 | **Turnos, asistencia y ausentismo** | Reemplazos de última hora y horas extra sin control | Recibe avisos de ausencia, propone reemplazos, consolida horas y alerta por exceso de horas extra o puestos descubiertos | WhatsApp, Excel de turnos | −10–20 % de horas extra; cobertura de puestos | Seguridad, limpieza, retail, salud | Media |
| P11 | **Ingreso de personal (onboarding) y legajo** | Expedientes incompletos y contingencias laborales | Pide documentos al nuevo ingreso, valida, recuerda capacitaciones obligatorias y emite estado del legajo | WhatsApp, PDF, formularios | Contingencias evitadas; días hasta que la persona es productiva | Tercerización, agro, construcción | Baja |
| P12 | **Mantenimiento de flota y equipos** | Mantenimientos preventivos olvidados y paradas imprevistas | Pide kilometraje u horómetro, programa preventivos, alerta, registra costos por unidad | WhatsApp, Excel | −20–30 % de paradas no programadas | Logística, construcción, agro | Baja |
| P13 | **Reclamos, devoluciones y postventa** | Reclamos perdidos en correos, sin causa raíz | Registra, clasifica, asigna, recuerda plazos, analiza causas y emite reporte mensual | Correo, WhatsApp | Tiempo de resolución y notas de crédito evitadas | Distribución, manufactura, retail | Baja |
| P14 | **Reporte gerencial mensual y comité** | El gerente espera 15–20 días por un PPT armado a mano | Pide insumos a cada área, consolida, calcula KPI con código, redacta hallazgos y alertas y genera el tablero | Excel de áreas, correos | 2–5 días-persona al mes; decisiones 2 semanas antes | Todos | Media |
| P15 | **Seguimiento de acuerdos y compromisos de reuniones** | Lo acordado en el comité no se cumple | Toma el acta, asigna responsables, recuerda, pide avance y reporta cumplimiento | Correo, actas, chat | Tasa de cumplimiento de acuerdos | Todos | Baja |
| P16 | **Inventario por conteos cíclicos y mermas** | Diferencias de inventario que se descubren al cierre | Programa conteos, recibe resultados, compara con el Excel exportado, alerta por diferencias y recomienda ajustes | Excel exportado, fotos | −1–2 % de merma | Distribución, retail, manufactura | Media |
| P17 | **Liquidación de comisiones e incentivos** | Disputas mensuales y cálculos opacos | Consolida ventas y cobranza exportadas, calcula con reglas en código, explica cada cálculo a cada vendedor | Excel | 1–3 días al mes y menos conflictos | Distribución, servicios | Baja |

### Matriz de priorización (valor × facilidad)

Escala de 1 a 5. Puntuación **[Supuesto]**.

| Proceso | Valor | Facilidad | Producto | Cuadrante |
|---|---|---|---|---|
| P1 Cobranza | 5 | 5 | **25** | Ganar rápido |
| P6 Vencimientos documentales | 4 | 5 | **20** | Ganar rápido |
| P14 Reporte gerencial | 5 | 4 | **20** | Ganar rápido |
| P4 Gastos y viáticos | 4 | 5 | 20 | Ganar rápido |
| P5 Control de obra | 5 | 4 | **20** | Ganar rápido (construcción) |
| P2 Flujo de caja | 5 | 3 | 15 | Estratégico |
| P7 Órdenes en campo | 5 | 3 | 15 | Estratégico |
| P3 Requisiciones y compras | 4 | 3 | 12 | Estratégico |
| P9 Cotizaciones y pipeline | 3 | 4 | 12 | Complemento |
| P15 Acuerdos de reuniones | 3 | 4 | 12 | Complemento (pieza de entrada) |
| P17 Comisiones | 3 | 4 | 12 | Complemento |
| P12 Flota | 3 | 4 | 12 | Complemento |
| P13 Reclamos | 3 | 4 | 12 | Complemento |
| P10 Turnos | 4 | 3 | 12 | Estratégico (tercerización) |
| P11 Onboarding | 3 | 4 | 12 | Complemento |
| P8 Pedidos por WhatsApp | 4 | 2 | 8 | Exigente (políticas de Meta y volumen) |
| P16 Inventario | 3 | 2 | 6 | Posponer |

### Top 5

1. **Cobranza (P1).** Retorno en dinero visible en 30–60 días y el dolor más universal.
2. **Reporte gerencial mensual (P14).** Es el "cerebro" visible para el dueño y el gancho natural para sumar piezas.
3. **Control de vencimientos documentales (P6).** Riesgo bajo, valor alto, se implementa en semanas y es ideal en servicios y construcción.
4. **Control de obra o proyecto (P5).** La pieza central en construcción.
5. **Flujo de caja de 13 semanas (P2).** Se apoya en la cobranza y convierte el sistema en una herramienta del CFO.

P4 (gastos) empata en puntaje y sirve como pieza de entrada barata.

---

## 3. Rutas "por piezas" (land and expand)

La lógica es que **cada pieza crea datos maestros y hábitos que la siguiente reutiliza**: clientes, proveedores, obras, personas, responsables y el canal de WhatsApp o correo ya aceptado. El "sistema de IA" de la empresa es esa base común más los procesos conectados. **[Supuesto]**

### Ruta A: "Cerebro financiero" (distribución, importadoras, servicios B2B)

**P1 Cobranza → P2 Flujo de caja → P3 Compras y aprobaciones → P4 Gastos → P14 Reporte gerencial**

- La cobranza crea el maestro de clientes y la proyección de entradas, que es la mitad del flujo de caja.
- El flujo de caja revela que las salidas no se controlan, lo que abre la pieza de compras.
- Compras y gastos completan las salidas.
- Con entradas y salidas sistematizadas, el reporte gerencial se arma casi solo. El dueño pasa a ver "su empresa" en un tablero, y ese es el momento del "sistema".

### Ruta B: "Operación en terreno" (construcción, servicios de campo, logística)

**P6 Vencimientos → P7 Órdenes de trabajo o P5 Control de obra → P3 Compras → P10 Turnos y P11 Onboarding → P14 Reporte gerencial**

- Vencimientos es la pieza de menor riesgo. Crea el maestro de personas, vehículos, sedes y clientes, y acostumbra al personal de campo a responder al sistema por WhatsApp.
- Con ese hábito instalado, las órdenes de trabajo o el avance de obra se capturan por el mismo canal.
- El control de obra expone desviaciones de costo, cuya fuente principal son las compras.
- La gestión de personas cierra el ciclo de capacidad.
- El reporte gerencial consolida margen por obra o contrato.

### Ruta C: "Motor comercial" (distribución, manufactura liviana)

**P9 Cotizaciones y pipeline → P1 Cobranza → P17 Comisiones → P13 Reclamos → P8 Pedidos por WhatsApp → P14 Reporte gerencial**

- El pipeline crea el maestro de clientes y vendedores.
- La cobranza conecta "vender" con "cobrar", y las comisiones sobre lo cobrado alinean incentivos.
- Los reclamos explican pérdidas de clientes.
- Recién con datos ordenados conviene automatizar pedidos, que es la pieza más compleja.

**Recomendación de diseño [Supuesto]:** vender siempre P14 (reporte gerencial) como la "pieza 0 o 1" en una versión mínima. Así el dueño ve desde el principio que cada nueva pieza "enciende" una nueva sección de su tablero, y eso hace tangible la expansión.

---

## 4. Señales de precio

### Lo que pagan hoy por software comparable

- **ERP y contabilidad en la nube para pymes:**
    - Bind ERP (México) cuesta MXN 570–1.700 al mes, más IVA, con 2 a 6 usuarios; el timbrado se paga aparte ([Tiendanube](https://www.tiendanube.com/blog/mx/bind-erp/)). Equivale a unos USD 30–95 al mes **[Supuesto: tipo de cambio ~18 MXN/USD]**.
    - Alegra (Colombia) va de COP 74.900 a 319.900 al mes, y Siigo Nube Emprendedor cuesta COP 191.327 al mes, según el comparativo de Alegra ([Alegra](https://blog.alegra.com/colombia/alegra-vs-siigo-colombia/)). Equivale a unos USD 18–80 al mes **[Supuesto: ~4.000 COP/USD]**.
    - **Implicación:** el gasto en software "core" de la mediana empresa es bajo. Una pieza de IA a USD 1.000 al mes cuesta 10 a 30 veces lo que pagan por su ERP, así que debe justificarse por resultado y no como software.
- **IA genérica:** Microsoft 365 Copilot cuesta unos USD 30 por usuario al mes, más una licencia base de USD 12,50–57 ([eesel](https://www.eesel.ai/es/blog/copilot-pricing)). Para 20 usuarios son unos USD 850–1.700 al mes, y aun así no opera ningún proceso. Es un ancla útil: "por lo mismo, te entregamos un proceso funcionando".
- **Automatización:** Zapier cuesta USD 30–104 al mes y n8n entre USD 20 y 800 al mes en la nube ([CostBench](https://www.costbench.com/compare/n8n-vs-zapier/)). Es la referencia "hazlo tú mismo" contra la que competirá la pieza.
- **WhatsApp Business Platform:** cobra por mensaje según categoría y país. Desde octubre de 2026 hay 1.000 mensajes de servicio gratis al mes por número y los mensajes de utilidad se cobran ([Meta](https://developers.facebook.com/docs/whatsapp/pricing)). El costo variable es bajo, pero debe cobrarse aparte y de forma transparente.

### Presupuesto y costo de servicios

- **Peso de la IA en el gasto de TI:** las mipymes colombianas destinan el 29 % del presupuesto tecnológico a IA ([ITSitio/Microsoft](https://www.itsitio.com/co/?p=177284)). En el promedio latinoamericano, la IA llega al 20 % del gasto de TI, frente al 8 % de 2024 ([DPL News/IDC](https://dplnews.com/?p=269676)). El presupuesto existe y crece.
- **Costo de talento técnico:** un desarrollador senior en la región cuesta USD 68–100 por hora (México 75–95, Colombia 68–88, Chile 80–100) ([Index.dev](https://www.index.dev/blog/latam-developer-hourly-rates)). Hacerlo en casa (unas 120–200 h por proceso) costaría USD 8.000–20.000 sin conocimiento del proceso **[Supuesto]**.

### Calibración propuesta [Supuesto]

| Componente | Rango sugerido | Lógica |
|---|---|---|
| Pieza de entrada (P6, P4, P15) | USD 2.500–5.000 de instalación + USD 300–600 al mes | Precio de decisión de una reunión con el gerente general, por debajo del umbral habitual de aprobación del directorio |
| Pieza de alto valor (P1, P2, P5, P7, P14) | USD 6.000–12.000 de instalación + USD 600–1.500 al mes | Anclada al valor: en cobranza, liberar USD 274.000 de capital de trabajo (ejemplo de la sección 2) justifica pagar varias veces el precio |
| "Sistema" (4 o más piezas) | USD 2.500–4.500 al mes, todo incluido, con descuento por pieza | Comparable a 1–2 analistas administrativos, pero operando 24/7 |
| Consumo de IA y WhatsApp | Costo más un margen, aparte | Transparencia y protección del margen |

Los revisores internos proponen USD 12.000–20.000 de implementación y USD 1.200–2.500 al mes por proceso (`docs/revision-expertos/00-sintesis.md`). Ese rango es coherente para piezas complejas o clientes de USD 20 M o más de facturación, pero **es alto como "precio accesible" de entrada** frente a un gasto en software core de USD 30–100 al mes. La recomendación es una escalera: entrar barato con una pieza de bajo riesgo y cobrar en serio desde la segunda, que es donde se demuestra el valor **[Supuesto]**.

**Vacío de datos:** no se encontraron encuestas públicas con el presupuesto anual de software o consultoría de la mediana empresa latinoamericana desglosado por tamaño. Conviene validar los precios con 10–15 entrevistas de disposición a pagar en los tres rubros recomendados.

---

## Fuentes

- [ITSitio: estudio de Microsoft sobre IA en mipymes de Colombia (2025)](https://www.itsitio.com/co/?p=177284)
- [SAP News: El poder transformador de la IA en América Latina (2025)](https://news.sap.com/latinamerica/2025/06/el-poder-transformador-de-la-ia-en-america-latina/)
- [DPL News: IDC y Lenovo, CIO Playbook 2025, gasto en IA en LatAm](https://dplnews.com/?p=269676)
- [DPL News: CEPAL advierte baja adopción digital en mipymes (2024)](https://dplnews.com/?p=237636)
- [EuQueroInvestir: IDC, inversión en IA en LatAm 2026](https://euqueroinvestir.com/economia/brasil-lidera-investimentos-em-ia-na-america-latina-em-2026-diz-idc)
- [IT Brief: McKinsey State of AI 2025](https://itbrief.co.uk/story/mckinsey-report-shows-ai-interest-but-slow-scaling)
- [El Peruano: Perú avanza en adoptar la IA](https://www.elperuano.pe/noticia/292915-peru-avanza-en-adoptar-la-inteligencia-artificial)
- [Atradius: B2B payment practices trends, Mexico 2024](https://atradius.us/knowledge-and-research/reports/b2b-payment-practices-trends-mexico-2024)
- [Tiendanube: Bind ERP, precios](https://www.tiendanube.com/blog/mx/bind-erp/)
- [Alegra: Alegra vs. Siigo Colombia](https://blog.alegra.com/colombia/alegra-vs-siigo-colombia/)
- [eesel: precios de Microsoft Copilot](https://www.eesel.ai/es/blog/copilot-pricing)
- [CostBench: n8n vs. Zapier pricing](https://www.costbench.com/compare/n8n-vs-zapier/)
- [Meta: precios de WhatsApp Business Platform](https://developers.facebook.com/docs/whatsapp/pricing)
- [Index.dev: LATAM developer hourly rates 2025](https://www.index.dev/blog/latam-developer-hourly-rates)

**Notas sobre las fuentes:**
- La cifra de costos logísticos del BID (18–35 % frente al 8 % de la OCDE) no tiene enlace: los documentos originales del BID devolvieron error al abrirlos.
- El ejemplo de capital de trabajo (USD 274.000) es un cálculo propio sobre una empresa hipotética de USD 10 M de ventas, no un dato de fuente.
- Las encuestas de Defontana y del BCRP aparecieron en los resultados de búsqueda, pero no se pudieron abrir ni verificar, así que no se usan.
