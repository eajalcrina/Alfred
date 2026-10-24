# Ronda 2: experto en modelos de negocio basados en tecnología

## 1. Mi postura en una línea
Cambió en parte. En la ronda 1 dije que era consultoría sin recurrencia; ahora el modelo por piezas con suscripción tiene forma de negocio recurrente. Pero su viabilidad depende de la **tasa de expansión**, no del precio de entrada. Una pieza de entrada barata que no se expande pierde dinero.

## 2. Sobre los ajustes del fundador
1. **Sin ESG: de acuerdo.** El ticket no da y el canal está saturado. Además libera foco comercial.
2. **Sin integraciones: con matices.** Baja el costo de instalación, y eso ayuda al margen. A cambio crea otro riesgo de churn: si el cliente deja de enviar las exportaciones de Excel, el sistema se queda sin datos y parece que "no funciona". Hace falta una ingesta estandarizada (plantilla de exportación por ERP), aunque no sea una integración.
3. **Precio accesible y margen por eficiencia: con matices.** El orden está invertido. Primero hay que medir la curva de horas y después bajar el precio. Bajar el precio contando con una eficiencia que todavía no existe es subsidiar con la caja.
4. **"Un Cerebro que crea cerebros": con matices.** Desde lo económico, una marca de producto permite cobrar como software y no por hora. Pero decir "como un ERP" pone el ancla equivocada: el cliente compara con un ERP en la nube de USD 30–95 al mes (investigación, sección 4).
5. **Por piezas: de acuerdo con el mecanismo y en desacuerdo con el objetivo declarado.** Que "termine costando más que un ERP" está bien como resultado, pero es un mal objetivo y un peor mensaje (ver punto 4.5).

## 3. Debate con el panel
- **Refuerzo al experto en medianas empresas LatAm:** el ROI por horas es débil porque un analista cuesta USD 600–1.500 al mes. Un "sistema" de USD 3.500 al mes equivale a dos o tres analistas. Si el tablero no muestra dinero (DSO, margen por obra, multas evitadas), el CFO lo recorta en la primera revisión de presupuesto. El ROI en caja es la defensa contra el churn, no un argumento de venta.
- **Rebato en parte la escalera de la investigación** (entrada de USD 2.500–5.000 más USD 300–600 al mes). Supuesto: operar una pieza cuesta unas 4 horas al mes más infraestructura, unos USD 250–300. A USD 300 el margen bruto es cero. El piso debería ser de unos USD 450 al mes.
- **Rebato mi propia cifra de la ronda 1** (instalación de USD 12.000–20.000): suponía integración con el ERP. Sin integración, USD 6.000–9.000 es razonable para piezas de alto valor.
- **Refuerzo al experto en IA:** los tokens de agentes que se disparan solos pueden desbordarse. Hay que cobrarlos aparte, con un tope pactado. Aun así es la palanca de margen menos importante (supuesto: menos del 10 % del costo).
- **Matizo al experto en ERP:** decía que el ERP es la fuente de verdad. Sin integración, la base común de las piezas pasa a ser la fuente de verdad operativa. De ahí sale la retención del "sistema", pero también la responsabilidad legal por esos datos.

## 4. Desde mi especialidad: qué haría
**4.1 Cliente tipo a 24 meses (Ruta A; todo es supuesto: USD 50 por hora, CAC de USD 3.000 y USD 1.000 por cada expansión)**

| Mes | Evento | Instalación (costo) | MRR | Costo de servicio al mes |
|---|---|---|---|---|
| 1 | Entrada: P14 mínimo | 3.000 (50 h = 2.500) | 450 | 300 |
| 4 | + P1 Cobranza | 8.000 (120 h = 6.000) | 1.450 | 550 |
| 10 | + P2 Flujo de caja | 6.000 (90 h = 4.500) | 2.250 | 750 |
| 16 | + P3, paso a "Sistema" | 4.000 (70 h = 3.500) | 3.500 | 900 |

- **Ingresos a 24 meses:** unos USD 75.500, de los cuales USD 21.000 son instalación y USD 54.500 son recurrentes.
- **Costos:** USD 16.500 de instalación y USD 16.800 de servicio. El margen bruto recurrente es de alrededor del 69 %.
- **Contribución después de CAC y expansión:** unos USD 36.000, cerca del 48 %.
- **Si el cliente no pasa de la entrada:** ingresa USD 13.800 contra unos USD 12.700 de costo. Queda en punto de equilibrio y no aporta nada.

**Conclusión:** todo el valor está en las piezas 2 a 4.

**4.2 Prioridades**
1. **Diseñar la escalera para empujar la expansión.** La instalación de entrada se abona como crédito a la segunda pieza si se contrata dentro de los 6 meses. Meta: al menos el 50 % de los clientes de entrada pasan a una segunda pieza y la retención neta de ingresos (NRR) supera el 120 %.
2. **Palancas de eficiencia, por impacto:**
    - **(a)** Horas de instalación por plantilla: bajar de 180 a 100 y luego a 70 horas en la tercera instalación del mismo proceso. Es el 50 % del costo.
    - **(b)** Automatizar la propia entrega: ingesta, evals y onboarding con guiones.
    - **(c)** Operación multicliente: una persona por cada 15–20 piezas activas.
    - **(d)** Modelos: enrutar a modelos baratos, usar caché y dejar el cálculo al código.
3. **Precio = núcleo + piezas con precio decreciente.** El "Cerebro base" (maestros de datos, canal y tablero) se cobra una sola vez. Así el cliente ve por qué la pieza 4 sale más barata.
4. **Piezas que se pueden dar de baja por separado.** Bajar una pieza no debe obligar a cancelar el sistema. Esto evita el churn de todo o nada.
5. **"Más caro que un ERP":** es un riesgo de percepción. Cuando la factura se ve como un solo bloque, el CFO la revisa entera. No usarlo nunca hacia afuera. Hacia adentro, que el precio total se mantenga por debajo del 20 % del valor medido en el tablero (supuesto) y revisarlo cada año.

## 5. Lo que no negociaría
Ninguna pieza se vende sin una suscripción mensual con un margen bruto de al menos el 60 %. La entrada puede ser barata en la instalación, nunca en lo recurrente.

## 6. Pregunta para el fundador
En sus primeras conversaciones con gerentes, ¿cuántos nombraron sin ayuda una segunda pieza por la que pagarían? Si son menos de la mitad, la escalera no tiene peldaños, solo una entrada.
