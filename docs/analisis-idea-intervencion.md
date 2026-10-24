# Intervención de procesos con agentes de IA: análisis de la idea

> Versión 0.1 · 24-oct-2026 · Redesign Lab, nueva división de IA para empresas (sin nombre aún)
> Documento de trabajo: complementa a `docs/analisis-satia.md`.

## La idea original

Una empresa nos contrata para ordenar y optimizar un proceso relevante. Intervenimos durante un tiempo fijo y desafiante (un mes) para levantar toda la información del proceso: usuarios, documentos, datos. La cargamos en Claude Code junto con una investigación extensa sobre ese proceso o problema. Con eso creamos un **repositorio "estratega + equipo de agentes"** que, de forma conversacional, interactúa con los usuarios de la empresa: solicita información, hace recordatorios, procesa datos, entrega análisis, alertas y recomendaciones, y genera los productos finales del proceso (bases de datos, dashboards, Excel, reportes, indicadores).

- **Plan A:** la empresa se hace responsable del mantenimiento y la actualización.
- **Plan B:** se contrata un plan de mantenimiento para que la herramienta siga funcionando según lo diseñado.

---

## 1. La idea en una frase

> **"Convertimos un proceso crítico de tu empresa en un sistema de agentes de IA que lo opera contigo, en 30 días."**

El servicio vende tres cosas:
- **La intervención:** levantar el proceso, investigarlo y rediseñarlo.
- **El activo:** un sistema de agentes con todo el conocimiento del proceso.
- **La continuidad:** el cliente lo mantiene (Plan A) o lo mantenemos nosotros (Plan B).

Respecto a Satia: Satia vende la plataforma y deja que otros implementen. Nosotros venderíamos **la implementación con conocimiento profundo del proceso**, que es justo lo que Satia terceriza.

---

## 2. Repositorio, MCP, skills y agentes: en qué se diferencian

| Concepto | Qué es | Analogía | En esta idea |
|---|---|---|---|
| **Repositorio** | Una carpeta versionada (git) con todo lo que el sistema sabe y sabe hacer | **La oficina**, con manuales, archivos y procedimientos | El entregable central: el "cerebro" del proceso |
| **CLAUDE.md** | El archivo de instrucciones principales del repositorio | **El manual del gerente** | El "estratega": objetivos, reglas, contexto de la empresa |
| **Agentes (subagentes)** | Roles especializados con instrucciones propias | **Los empleados** | Recolector, analista, reportero, auditor |
| **Skills** | Procedimientos reutilizables (instrucciones + scripts) | **Los protocolos de trabajo** | "Validar Excel", "Generar reporte mensual" |
| **MCP** (Model Context Protocol) | Un estándar abierto para conectar la IA con sistemas externos | **Los cables y teléfonos** hacia afuera | Leer Google Sheets o el ERP, enviar correos o WhatsApp |
| **Plugin** | Un paquete instalable con skills, agentes y conectores MCP | **La oficina empaquetada para mudarla** | La forma de instalar el sistema en el equipo del cliente |

**Conclusión:** no hay que elegir entre repositorio y MCP. El entregable es un **repositorio (o un plugin) que usa conectores MCP**: el repositorio guarda el conocimiento y los procedimientos, y los MCP le dan "manos" para actuar en los sistemas de la empresa.

### Estructura sugerida del repositorio

```
proceso-cobranzas-empresaX/
├── CLAUDE.md              # El estratega: objetivos, reglas, KPIs, contexto
├── conocimiento/          # Levantamiento: entrevistas, documentos, investigación
├── .claude/agents/        # Recolector, analista, reportero, auditor
├── .claude/skills/        # Procedimientos: validar-excel, generar-reporte, alertas
├── scripts/               # Cálculos exactos de indicadores (Python)
├── plantillas/            # Formatos de Excel, reportes, dashboards
├── .mcp.json              # Conectores: Drive, Sheets, Gmail, ERP, WhatsApp
└── evals/                 # Pruebas para verificar que sigue funcionando
```

---

## 3. Viabilidad técnica

### Lo que ya funciona hoy
- Agentes especializados, skills y conectores MCP para Google Drive, Sheets, Gmail, Slack, HubSpot y otros.
- Generación de Excel, Word, PowerPoint, PDF y dashboards.
- Tareas programadas (rutinas) que se ejecutan solas.
- Ingerir documentos y una investigación extensa como base de conocimiento.

### Los 6 retos críticos

| # | Reto | Por qué importa | Cómo resolverlo |
|---|---|---|---|
| 1 | **Interfaz** | El usuario de negocio no usará una terminal | Claude Code para **construir**; para **usar**, la app de Claude (Cowork o Proyectos con plugins), o los agentes conectados a WhatsApp, Slack o Teams mediante el Agent SDK |
| 2 | **Proactividad** | Un chat no escribe por iniciativa propia; los recordatorios y alertas requieren un disparador | Tareas programadas (rutinas o cron) que envían mensajes por correo o WhatsApp |
| 3 | **Datos vivos** | Un repositorio no es una base de datos | Separar el **conocimiento** (repo) de los **datos** (Sheets, Supabase o el ERP). Es la lección de Satia: tablas como fuente de verdad |
| 4 | **Exactitud** | Un modelo de IA puede equivocarse calculando indicadores | **La IA coordina y el código calcula**: los KPI salen de scripts, no de la IA "a ojo" |
| 5 | **Seguridad y privacidad** | Se manejan datos sensibles de la empresa y sus personas | Permisos, aprobación humana para acciones sensibles, registro de acciones, acuerdo de tratamiento de datos y cumplimiento de la ley de cada país (Perú, Colombia, Chile, Brasil, México) |
| 6 | **Mantenimiento** | Cambian modelos, APIs, formatos de archivo y personas | Pruebas automáticas (`evals/`), versionado y un dueño interno designado |

**Veredicto técnico:** es **viable** si se limita a **un proceso acotado** por intervención. Levantar "todo de la empresa" en un mes no lo es. El reto principal no es la IA sino la **interfaz y la continuidad**.

---

## 4. Viabilidad como negocio

### Fortalezas
- **Entregable tangible**: un sistema funcionando, no una presentación ni un piloto genérico.
- **Diferenciación real** frente a la "consultoría de IA" comoditizada.
- **Cada intervención crea un activo reutilizable**: el repositorio de "cobranzas" sirve de base para el próximo cliente. Así se escala.
- **Coherente con el brief**: evidencia sobre promesa, capacidad instalada y no casarse con un proveedor. MCP es un estándar abierto y el conocimiento queda en texto portable.

### Riesgos

| Riesgo | Detalle | Mitigación |
|---|---|---|
| **El Plan A muere** | En una mediana empresa latinoamericana es probable que nadie mantenga el sistema; si deja de funcionar, la reputación la pagamos nosotros | Exigir un **dueño interno** capacitado; un período de acompañamiento obligatorio de 60 a 90 días; el Plan B como opción recomendada |
| **Alcance inflado** | "Levantar todo" sin límites revienta el mes | Un proceso, KPIs de línea base el día 1 y entregables cerrados por contrato |
| **Horas senior** | La intervención intensiva limita el margen | Estandarizar con un **catálogo de procesos** y plantillas base |
| **Ciclo de venta** | Las medianas empresas tardan en decidir | Un diagnóstico corto pagado como puerta de entrada |
| **Costos de IA** | Licencias y consumo variable | Presupuesto de uso definido y gobernanza (el argumento de "control de costos" del brief) |

### Precios: hipótesis a validar

| Componente | Rango indicativo (USD) |
|---|---|
| Diagnóstico (1 semana) | 1.000 – 2.500 (abonable a la intervención) |
| Intervención de 30 días | 6.000 – 15.000, según país y complejidad |
| Plan B, mantenimiento | 500 – 1.500 al mes |
| Licencias y consumo de IA | Aparte y transparente |

*Son referencias para empezar a probar el mercado, no cifras validadas. Hay que contrastarlas con 3 a 5 conversaciones con clientes reales.*

---

## 5. Mejoras para que funcione en América Latina

1. **WhatsApp como interfaz principal**, con el correo como respaldo. Es donde vive la operación en la región; el usuario no debería tener que aprender otra herramienta.
2. **Excel y Google Sheets como cara visible de los datos.** La mediana empresa vive en Excel: el sistema lee y entrega en Excel, sin obligar a migrar.
3. **Integraciones locales:** facturación electrónica (SUNAT, DIAN, SAT, SII), ERP comunes (Siigo, Alegra, Contpaqi, Defontana, SAP Business One) y bancos locales.
4. **Catálogo de procesos estándar** en lugar de empezar de cero cada vez: consolidación de reportes, cobranzas, compras y aprobaciones, rendición de gastos, gestión de proveedores, onboarding de personal y **reportes de impacto y ESG** (conecta con el resto del portafolio de Redesign Lab).
5. **Tres planes en vez de dos:**

| Plan | Qué incluye | Para quién |
|---|---|---|
| **A · Autónomo** | Entrega + capacitación + manual | Empresas con un equipo interno capaz |
| **A+ · Acompañado** | Bolsa de horas de soporte trimestral | La mayoría: el punto medio realista |
| **B · Gestionado** | Mantenimiento, monitoreo, mejoras y compromiso de servicio | Procesos críticos |

6. **Fases claras:** Diagnóstico (1 semana) → Intervención (4 semanas) → Operación asistida (60–90 días) → Plan A, A+ o B.
7. **Medición obligatoria:** línea base el día 1 y resultados el día 30 (horas ahorradas, errores, tiempo de ciclo). Cada cliente se convierte en un caso de evidencia.
8. **Gobernanza como argumento de venta** (lección de Satia): registro de cada acción, permisos y aprobación humana.
9. **A futuro, una red de implementadores certificados** en la metodología de Redesign Lab, siguiendo el modelo de partners de Satia, para escalar a otros países sin estar presente.
10. **Satia como herramienta complementaria** cuando el cliente necesite atención masiva por WhatsApp, sin depender de ella.

### Arquitectura en capas

| Capa | Qué contiene |
|---|---|
| **Interfaz** | WhatsApp, correo, app de Claude, Slack o Teams |
| **Orquestación** | Estratega + agentes + tareas programadas |
| **Conocimiento** | Repositorio: CLAUDE.md, skills, investigación |
| **Acción** | Conectores MCP: Drive, Sheets, ERP, mensajería |
| **Datos** | Sheets, base de datos o ERP: la fuente de verdad |

---

## 6. Recomendación y próximos pasos

**La idea es buena y diferenciada**, con dos ajustes clave:
- **acotar a un proceso** por intervención;
- **resolver la interfaz y la continuidad desde el diseño**, no al final.

Pasos sugeridos:
1. **Elegir un proceso piloto.** Propuesta: la consolidación de reportes en Excel (ya está en el brief).
2. **Conseguir una empresa piloto cercana**, idealmente del ecosistema de Redesign Lab, a precio reducido a cambio de poder publicar el caso.
3. **Construir la "plantilla 0" del repositorio**, con la estructura de la sección 2.
4. **Validar precios** con 3 a 5 conversaciones con empresas medianas.
5. **Definir con Roy Pérez** la interfaz (WhatsApp, Slack o la app de Claude) y el stack por defecto.
