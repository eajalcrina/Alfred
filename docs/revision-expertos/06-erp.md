# Revisión: experto en ERP para empresas medianas de LatAm

### 1. Veredicto en una línea
Es viable como servicio de **rediseño de procesos alrededor del ERP**. Como "agentes que operan el proceso", tal como está planteado, no lo es: subestima el acceso a datos del ERP, la IA que los propios ERP ya traen y el poder de veto del partner.

### 2. Lo que funciona
- **Ataca el hueco real.** La mediana empresa latinoamericana tiene el ERP para el registro contable y tributario, pero el proceso vive en Excel, correo y WhatsApp (conciliaciones, cobranza, consolidación, rendiciones). Ahí ni el ERP ni el partner entregan valor, porque el partner cobra por módulo y parametrización, no por rediseñar el proceso.
- **"La IA coordina y el código calcula"** es la decisión correcta. Los KPI financieros que salen del LLM "a ojo" no pasan una auditoría ni el cierre mensual.
- **Separar el conocimiento (repo) de los datos (ERP/Sheets)** respeta el principio de que el ERP es la fuente de verdad. Es la condición mínima para que el área de finanzas acepte el sistema.
- **El proceso piloto (consolidación de reportes) es de bajo riesgo**: es de solo lectura sobre el ERP y no toca la emisión de documentos tributarios.
- **El catálogo por proceso** es reutilizable de verdad, siempre que se ate a un ERP concreto (ver recomendaciones).

### 3. Lo que no funciona o es riesgoso
- **El "conectado vía MCP" es el supuesto más débil.** Hoy existe soporte MCP o similar oficial en NetSuite (AI Connector Service) y en Business Central (servidor MCP; *supuesto: verificar si sigue en preview*), y Odoo tiene una API XML/JSON-RPC madura. Para Siigo, Alegra y Defontana hay APIs REST, pero no MCP oficial (*supuesto*), y sus límites de llamadas y cobertura de endpoints son desiguales. Contpaqi y Softland suelen estar *on-premise*, con SDK o acceso directo a SQL Server. SAP B1 requiere Service Layer, y muchas instalaciones no lo tienen expuesto. **En la práctica, la mitad del mes se puede ir en la integración**, no en los agentes.
- **Escribir en el ERP es otra liga.** Crear notas de crédito, asientos o documentos electrónicos (SUNAT, DIAN, SAT, SII) tiene consecuencias legales. Un agente que escribe sin la capa de validación del ERP y del PSE/PAC es un riesgo fiscal que ninguna empresa mediana aceptará en 30 días.
- **La IA nativa erosiona parte de la propuesta.** Business Central ya trae Copilot y agentes (pedidos de venta, cuentas por pagar). NetSuite trae NetSuite Next, Text Enhance y conciliación bancaria asistida. Odoo 18/19 incorpora IA en documentos, conciliación y OCR. SAP B1 integra funciones de SAP Business AI. TOTVS tiene Carol (*supuesto: alcance en mid-market*). El cliente preguntará: "¿por qué no activo lo que ya pago?".
- **El partner del ERP es un actor ignorado.** Controla las credenciales, los ambientes y el soporte, y muchas veces tiene contrato de mantenimiento. Un tercero que toca datos o personalizaciones sin él provoca bloqueo o pérdida de garantía de soporte. El documento no lo menciona ni como canal ni como amenaza.
- **Calidad de datos.** Maestros duplicados, centros de costo inconsistentes y planes de cuentas mal homologados entre filiales son la norma. Los agentes amplifican el desorden, no lo corrigen.
- **Plan A.** En una empresa con ERP, el "dueño interno" suele ser el contador o el jefe de TI con un analista. Mantener un repo con Claude Code, conectores y evals no es realista para ese perfil.
- **Los precios no incluyen la integración.** USD 6.000–15.000 por un mes, con integración incluida, queda corto para SAP B1 o Softland *on-prem*.

### 4. Recomendaciones (priorizadas)
1. **Hacer un diagnóstico de integrabilidad antes de vender** (semana 0). Checklist: qué ERP y versión, nube u *on-prem*, API o Service Layer disponible, quién es el partner, credenciales de solo lectura y PSE/PAC. Si no hay acceso de lectura en 5 días, no se firma la intervención.
2. **Mantener la intervención en solo lectura más una capa de "propuesta".** El agente prepara (borradores de asiento, listas de cobranza, conciliaciones sugeridas) y un humano ejecuta en el ERP. La escritura directa se deja para el Plan B y la fase 2.
3. **Limitar el catálogo a 2 o 3 ERP al inicio** según el país objetivo (p. ej. Siigo y Alegra en Colombia, Defontana y Softland en Chile, Contpaqi en México, Business Central regional) y construir un conector propio robusto por cada uno. Así el catálogo pasa de "proceso genérico" a "proceso por ERP".
4. **Hacer un mapa de "IA nativa vs. hueco"** en cada diagnóstico: qué resuelve ya el ERP (activarlo es un *quick win* y genera credibilidad) y qué queda fuera (multi-sistema, Excel, WhatsApp, seguimiento a personas). El servicio vende lo segundo.
5. **Convertir al partner en aliado.** Ofrecerle reparto de ingresos o hacer co-entrega, y que asuma el mantenimiento de la integración. Esto resuelve parte del Plan A.
6. **Dedicar un sprint de calidad de datos maestros** (clientes, proveedores, cuentas) como entregable explícito de la primera semana.
7. **Reprecificar por complejidad de integración** (nube con API / *on-prem* / sin API).

### 5. Cómo diferenciarse de soluciones equivalentes
- **Frente a la IA nativa del ERP** (Copilot de BC, NetSuite Next, Odoo AI, SAP Business AI): trabajo transversal entre ERP, Excel, correo y WhatsApp, con el rediseño del proceso. Lo nativo se queda dentro de su propio módulo.
- **Frente a las plataformas de automatización contable** (Nubox, Chipax, Fintoc + conciliación, Xepelin en cobranza; *supuesto: cobertura por país*): ellas venden un producto estándar; la propuesta aquí es el proceso propio del cliente, documentado y portable.
- **Frente a integradores e iPaaS** (n8n, Make, Zapier, Workato, Celigo para NetSuite) y RPA (UiPath, Rocketbot, de origen chileno): esos mueven datos; el diferencial es la capa conversacional y la de seguimiento a personas (recordatorios, pedido de datos, explicación de desviaciones).
- **Frente a partners ERP y consultoras** (Big Four, partners Gold de SAP y Microsoft): velocidad de 30 días, línea base medida y un activo que el cliente conserva.
- **Frente a Satia:** enfoque en mediana empresa con ERP y gobierno de datos financieros, no en pyme con WhatsApp.

### 6. Pregunta clave
**¿Para qué 2 o 3 ERP y en qué país garantizamos acceso de lectura fiable a los datos en la primera semana, y quién (nosotros o el partner del ERP) mantiene esa integración cuando el ERP se actualice?**
