# Ronda 2: experto en ERP para empresas medianas de LatAm

## 1. Mi postura en una línea
Cambió en parte. Al sacar la integración desaparece el riesgo que más pesaba en mi revisión de la ronda 1, pero aparece otro: un **sistema en la sombra** que copia datos del ERP, se desfasa sin que nadie lo note y termina contradiciendo al contador. Es viable si el Cerebro **persigue** y el ERP **registra**. Si los dos registran, no lo es.

## 2. Sobre los ajustes del fundador
1. **Sin ESG: de acuerdo.** No tiene relación con el ERP ni con el dolor de caja de la mediana empresa.
2. **Sin integraciones: con matices.** Tiene razón en no escribir nunca en el ERP ni en el sistema del Estado. Eso evita el riesgo fiscal y el veto del partner del ERP. Pero hay que separar *integración* (una API) de *ingesta* (una exportación periódica). Sin la segunda, la cobranza, el reporte gerencial y las comisiones trabajan con datos viejos. Los procesos cuya verdad vive fuera del ERP funcionan bien sin integración. Los que dependen de saldos solo funcionan con una exportación disciplinada.
3. **Precio accesible con margen por eficiencia: con matices.** La eficiencia real no está en los modelos de IA. Está en tener **lectores de exportaciones por ERP** ya hechos: el reporte de antigüedad de Siigo no tiene el formato del de Contpaqi ni del de Alegra. Ese es el catálogo por ERP que pedí en la ronda 1, ahora sin API. Sin esos lectores, cada cliente nuevo cuesta horas de limpieza que el precio bajo no cubre.
4. **"Un Cerebro que crea cerebros" como ERP de marca: en desacuerdo con la palabra ERP.** Para un gerente de finanzas, un ERP es libro mayor, impuestos, inventario valorizado y pista de auditoría. Llamar ERP a algo que no hace nada de eso invita a una comparación que se pierde. Además asusta al contador y al partner, que lo leerán como reemplazo. "Cerebro" funciona. "ERP" no.
5. **Por piezas hasta un "ERP de IA" que vale más que un ERP: con matices.** Que cueste más que el ERP es esperable: Bind o Alegra cuestan USD 30–100 al mes. Lo defendible es *"vale más porque hace que el ERP se use"*, no *"es un ERP mejor"*. El riesgo de fondo es la fragmentación: si cada pieza crea su propio maestro de clientes, a la tercera pieza hay tres versiones de la verdad.

## 3. Debate con el panel
- **Investigación de rubros (distribución B2B):** dice que la cobranza "se ataca con un simple reporte de antigüedad exportado a Excel". **La refuerzo con una advertencia.** El reporte de antigüedad no refleja los pagos aplicados ayer. El error más caro posible es mandarle un recordatorio por WhatsApp a un cliente que ya pagó, porque el daño cae sobre la relación comercial del cliente, no sobre la nuestra. Sin una exportación fresca con fecha visible, la pieza estrella se vuelve en contra.
- **Investigación (P16 Inventario "posponer", P8 Pedidos "exigente"):** **la refuerzo y voy más lejos: sacarlos del catálogo.** Sin integración, el stock del Cerebro siempre va atrasado respecto del ERP, y un pedido confirmado sin stock real es una promesa rota.
- **Experto en IA aplicada:** propone "Postgres como fuente de verdad". **Lo rebato en parte.** Postgres puede ser la fuente de verdad de los *datos del proceso*: promesas de pago, evidencias, aprobaciones, vencimientos. Para facturas, saldos y pagos es solo una *copia fechada*. Si el contrato no marca esa diferencia, nace el ERP paralelo.
- **Experto en medianas empresas:** en la ronda 1 propuso la conciliación bancaria como piloto. **Ahora lo rebato.** Sin integración, conciliar es repetir el trabajo del contador sobre los libros, sin poder registrar el resultado. Sí comparto su tesis de que el retorno se mide en caja y no en horas.
- **Experto en branding:** "productizar antes de nombrar". **Lo refuerzo.** Una marca "ERP" sobre un catálogo que todavía no existe promete más de lo que el producto puede cumplir.

## 4. Desde mi especialidad: qué haría
1. **Clasificar el catálogo por semáforo, según dónde vive la verdad del dato:**
    - **Verde (la verdad vive fuera del ERP):** P6 Vencimientos, P5 Control de obra, P7 Órdenes de trabajo, P15 Acuerdos de reuniones, P3 Compras hasta antes de la orden de compra, P4 Gastos hasta antes del asiento, P10 Turnos, P11 Onboarding, P12 Flota, P13 Reclamos y P9 Cotizaciones. Empezar aquí.
    - **Amarillo (necesita una exportación periódica del ERP):** P1 Cobranza, P2 Flujo de caja, P14 Reporte gerencial y P17 Comisiones.
    - **Rojo (fuera del catálogo):** inventario, pedidos contra stock, conciliación bancaria, asientos, facturación electrónica, cálculo tributario y nómina legal.
2. **Volver al ERP por su puerta de importación, no por API.** El Cerebro entrega propuestas (gastos rendidos, compras aprobadas, comisiones calculadas) en la plantilla de importación por Excel que ya trae el ERP. *Supuesto: Siigo, Alegra y Contpaqi la tienen; verificar caso por caso.* El contador revisa e importa. Así el registro queda en el ERP y no hace falta integración.
3. **Diagnóstico de exportabilidad en la semana 0**, en lugar del diagnóstico de integrabilidad de la ronda 1. Qué reportes saca el ERP, en qué formato, quién los saca y si se pueden programar para que lleguen por correo (*supuesto: varios ERP en la nube lo permiten*). Sin una persona responsable de la exportación semanal, no se firma ninguna pieza amarilla.
4. **Un control de cuadratura en cada ciclo.** El total de la cartera y el número de facturas del Cerebro deben coincidir con la última exportación. Si la diferencia supera un umbral, se frenan los mensajes salientes y se avisa a una persona.
5. **Un solo maestro de clientes, proveedores y personas para todas las piezas**, con el código del ERP como identificador. Esto evita la fragmentación entre piezas.
6. **Venderle primero al contador:** "te quitamos llamadas y planillas, no tus libros". Él decide si el sistema convive con el ERP o choca con él.
7. **Cambiar el lenguaje:** no "ERP de IA", sino "la capa que hace que tu ERP se cumpla".

## 5. Lo que no negociaría
**Ningún dato contable, tributario o de inventario nace ni se corrige en el Cerebro.** El Cerebro solo lo lee de una exportación fechada y solo lo devuelve como propuesta que una persona registra en el ERP.

## 6. Pregunta para el fundador
En cada cliente, **¿quién exporta el reporte del ERP cada lunes, y qué hace la pieza (frena, avisa o sigue con datos viejos) el lunes que esa persona no lo hace?**
