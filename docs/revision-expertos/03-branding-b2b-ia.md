# Revisión: experto en branding de soluciones de IA para B2B

## 1. Veredicto en una línea
Hay un buen servicio detrás, pero todavía no hay posicionamiento: el documento describe *cómo se construye* (repositorio, Claude Code, MCP) y no *qué compra* un gerente de operaciones, y su promesa central ("en 30 días", "sin dependencia") choca con su propio modelo de entrega.

## 2. Lo que funciona
- **Entregable con forma de resultado.** "Un sistema funcionando en un proceso" es más fácil de vender que la "estrategia de IA". En B2B mediano, lo que se ve y se mide le gana al taller y al diagnóstico.
- **Medir la línea base el día 1 y el resultado el día 30.** Es el activo de marca más valioso del documento. Si se cumple, cada cliente se vuelve una prueba, y eso es justo lo que le falta a Satia (no publica casos) y a la mayoría de las agencias de automatización.
- **Un proceso por intervención y un catálogo de procesos.** Permite tener un nombre de producto ("cobranzas", "consolidación de reportes") en lugar de vender horas. La categoría se gana con productos, no con capacidades.
- **La regla "la IA coordina, el código calcula" y la gobernanza (registro de acciones, aprobación humana).** Son argumentos de confianza que le importan a un CFO, que no se deja convencer por "la IA es mágica".
- **WhatsApp y Excel como interfaz.** Es la lectura correcta de la región y reduce la fricción de adopción, que es la objeción real.

## 3. Lo que no funciona o es riesgoso
- **Vende la arquitectura, no el valor.** "Repositorio estratega + equipo de agentes" es lenguaje interno. Al comprador le da igual el git y el MCP, y además le genera ansiedad (¿quién entiende esto?). La tabla de la sección 2 es útil para el equipo, pero no debe llegar al mensaje comercial.
- **"Agnóstico / sin dependencia" no es creíble con este stack.** Todo se construye sobre Claude Code y sus convenciones (CLAUDE.md, subagentes, skills). Que el conocimiento esté en texto portable es cierto, pero el sistema operativo depende de un proveedor. Prometer neutralidad y entregar algo de un solo proveedor es un riesgo de confianza. Es mejor decir "tú eres el dueño" que "agnóstico".
- **El Plan A le hace daño a la marca.** El propio documento admite que en la mediana empresa latinoamericana nadie mantendrá el sistema. Venderlo como opción principal es sembrar fracasos que se atribuirán a la marca. "Capacidad instalada" y "un sistema que opera contigo" tiran en direcciones opuestas.
- **"30 días" es una promesa engañosa.** El recorrido real es diagnóstico (1 semana), intervención (4 semanas) y operación asistida (60 a 90 días): unos cuatro meses. Si el titular dice 30 días y la realidad son 120, la credibilidad se erosiona.
- **Precio contra posicionamiento.** Entre 6.000 y 15.000 USD por un mes de trabajo senior intensivo te coloca como "consultora barata", justo la categoría de la que se quiere escapar. Supuesto: con el levantamiento, la investigación y la construcción, el margen probablemente no aguante sin plantillas maduras.
- **La "diferenciación real" se afirma, pero no se demuestra.** No se nombra ningún competidor de la categoría (solo Satia, que es una plataforma y no un par directo).
- **La arquitectura de marca está sin resolver.** Redesign Lab se asocia con impacto y regeneración. Una división de "agentes de IA para cobranzas" puede diluir esa identidad o quedar desconectada de ella. El documento no decide si se apalanca el nombre madre o no.
- **Antropomorfizar ("estratega", "empleados")** genera expectativas de autonomía que la tecnología no siempre cumple, y despierta temor a reemplazar empleos en los equipos que deben adoptarla.

## 4. Recomendaciones (priorizadas)
1. **Productizar antes de nombrar.** Definir dos o tres "sprints" con nombre de proceso, precio fijo, entregables cerrados y una métrica garantizada (por ejemplo, el tiempo de cierre del reporte mensual). La marca se construye sobre el producto ancla, no sobre la división.
2. **Rehacer los planes.** Que el Plan B (gestionado) sea el plan por defecto e incluido el primer trimestre, y que el Plan A sea una excepción para clientes con equipo técnico. Comunicarlo como "operación asistida", no como "mantenimiento".
3. **Cambiar la promesa de tiempo** a "primer resultado medible en 30 días" en lugar de "sistema en 30 días".
4. **Sacar la tecnología del mensaje.** Claude, MCP y el repositorio van a la página de "cómo lo hacemos" y a la conversación con el área de TI, no al titular.
5. **Elegir un territorio de posicionamiento** (para explorar, no son nombres definitivos):
    - **A. "Procesos que se operan solos"**: centrado en el resultado operativo (cierre, cobranza, reporte) y medido en horas y errores. Es el más vendible a gerentes de finanzas y operaciones.
    - **B. "Tu sistema, tu propiedad"**: soberanía y control (el conocimiento y los datos quedan en la empresa, con gobernanza y auditoría). Contrasta con las plataformas que amarran al cliente y encaja con el ADN de "capacidad instalada".
    - **C. "Rediseño con evidencia"**: apalanca el nombre madre (*Redesign*) y su credibilidad metodológica, con un nicho en reportes de impacto y ESG donde el portafolio de Redesign Lab tiene legitimidad y pocos competidores de IA (supuesto a validar).
6. **Decidir la arquitectura de marca** (marca respaldada "X by Redesign Lab" frente a una marca independiente) en función del territorio. C exige el respaldo; A probablemente funciona mejor con independencia.

## 5. Cómo diferenciarse de soluciones equivalentes
- **Frente a las grandes consultoras y sus brazos de IA** (Accenture, Globant con sus "AI Pods", BCG X, QuantumBlack de McKinsey): competir en tamaño de cliente, velocidad y precio cerrado. Ellas no atienden con rentabilidad a la empresa mediana latinoamericana (supuesto razonable).
- **Frente a plataformas no-code** (Satia, Copilot Studio de Microsoft, Zapier/Make con agentes): profundidad en el proceso y propiedad del activo, frente a la herramienta genérica más un implementador. Ojo: estas plataformas reducen cada mes la barrera técnica, así que la ventaja tiene que estar en el conocimiento del proceso y en la medición, no en "saber construir agentes".
- **Frente a las agencias de automatización con IA** (un ecosistema amplio sobre n8n y Make, muy fragmentado en LatAm): metodología, evaluaciones (`evals/`), gobernanza y casos publicados con cifras. Hoy la mayoría vende flujos sueltos sin medir resultados.
- **Frente al modelo de ingeniero desplegado en el cliente** (forward deployed engineers, popularizado por Palantir y adoptado por empresas de agentes como Sierra o Decagon): es el referente conceptual más cercano. Se puede tomar su lógica ("nos instalamos en tu proceso"), pero a escala y precio de empresa mediana.
- **Diferenciador defendible:** una biblioteca pública de casos con línea base y resultado. Ningún competidor regional la tiene hoy (supuesto, no verificado de forma exhaustiva).

## 6. Una pregunta clave que el equipo debe responder
**¿Quién opera el sistema el día 91, quién paga por ello y está dispuesto a hacerlo?** La respuesta define si se trata de una consultora de proyectos, de un servicio gestionado recurrente o de una fábrica de plantillas, y con eso la categoría, el precio y la marca.
