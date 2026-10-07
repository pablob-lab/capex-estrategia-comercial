# 4. Herramientas y operación

> Precios en USD/mes consultados el 6-oct-2026 en las páginas oficiales de cada proveedor (enlaces en [fuentes](anexos/fuentes.md)). Pueden cambiar. "NV" = no verificado.
> Equipo de referencia: 4 socios + 2 empleados + 1 rol nuevo = **~7 usuarios**.

---

## 4.1 Stack recomendado

Hay que elegir **una sola plataforma central** que junte CRM y WhatsApp. Si se compran 5 herramientas sueltas, el equipo volverá al Excel.

### Opción recomendada: "Stack ligero" (~US$300–450/mes + mensajes de Meta)

| Necesidad | Herramienta recomendada | Qué resuelve | Alternativas | Costo aprox./mes | Complejidad | Prioridad |
|---|---|---|---|---|---|---|
| **CRM + pipeline (solicitantes e inversionistas)** | **Kommo Advanced** | Dos embudos visuales, WhatsApp API oficial integrado (hasta 3 números), bot básico, tareas y recordatorios. Sirve para un equipo que viene de Excel y vive en WhatsApp | HubSpot Sales Pro (más robusto, ~US$540–600 + US$1.500 de onboarding); Attio Plus (~US$35–44/usuario, moderno pero sin WhatsApp nativo); Bitrix24 Standard (US$99–144 plano) | US$35 × 7 ≈ **US$245** | Media | **Alta (mes 1)** |
| **IA conversacional en WhatsApp para precalificar y hacer seguimiento** | Bot de Kommo (Salesbot) **o** Respond.io con agente de IA | Responde en <1 min, 24/7; hace las 4–5 preguntas eliminatorias; pide el n.º de partida; agenda la llamada; manda nurturing a los "B" | Respond.io Growth (US$159, sin recargo sobre Meta); WATI Pro (~US$50); Leadsales (US$97–247); Treble.ai (cotizar) | Incluido / US$50–159 | Media | **Alta (mes 2)** |
| **Formulario de precalificación** | **Tally** | Formulario con lógica condicional conectado al CRM | Typeform (US$25–56), Jotform (US$34–49), Meta Lead Ads nativo | US$0–24 | Baja | Alta |
| **Gestión documental del expediente** | **Google Workspace** (Drive con carpeta por operación y plantilla de subcarpetas) | Expediente único y compartido con el abogado/fiduciario; permisos; versión final | Notion (US$10–20/usuario) como wiki del manual de procesos | S/28–56 por usuario (~US$55–110 total) | Baja | **Alta (mes 1)** |
| **Firma digital** | **DNIe + ReFirma (RENIEC)** para contratos privados; **DocuSign** para contratos con inversionistas y referidores | Firma remota de contratos de intermediación, referidores, inversionistas, declaraciones juradas | ZapSign, Adobe Sign (NV) | ReFirma gratis; DocuSign ~US$30–45/usuario (1–2 usuarios) | Baja | Media |
| **Cobranza y recordatorios** | Plantillas "utility" de WhatsApp disparadas desde el CRM según el calendario de pagos | Recordatorio el día de vencimiento (no antes, porque los clientes lo ven agresivo [ENTREVISTA]), +1 día, +4 días; escalamiento a carta notarial a los 7 días | Respond.io, WATI | ~US$0,03 por mensaje (NV) | Media | Media (mes 2–3) |
| **Distribución de oportunidades a inversionistas** | Pipeline de inversionistas en el CRM + **ficha PDF estándar** + envío **1:1** (no grupos abiertos) | Trazabilidad de quién vio qué y cuándo; exclusividad por tiempo; reduce riesgo regulatorio | Portal privado con login (fase 2) | Incluido | Media | **Alta** |
| **Automatización entre herramientas** | **Make** | Formulario → CRM → carpeta de Drive → aviso al equipo; calendario de pagos → recordatorios | Zapier (US$20–69), n8n (€20–50 o autoalojado) | US$9–16 | Media | Media |
| **Analítica y reporting** | **Looker Studio** (gratis) leyendo una Google Sheet exportada del CRM | Tablero semanal de KPIs (ver 4.3) | Power BI Pro (~US$14/usuario), Metabase (~US$100) | US$0 | Baja-media | Alta (mes 1) |
| **Verificación de solicitantes** | Consulta SUNARP en línea (partida, CRI, gravámenes, Alerta Registral) + central de riesgo (Sentinel/Equifax) | Filtrar antes de gastar en abogado | — | CRI ~S/70; gravamen ~S/25; centrales: cotizar | Baja | Alta |

**Costo total estimado:** **US$350–550 al mes** más mensajes de Meta (unos US$30–80 al mes con el volumen esperado [SUPUESTO]). Es **menos que el margen de una sola operación base dividido entre 40**.

### Ruta de implementación
1. **Semana 1–2:** Kommo + importar el Excel + definir etapas de los dos pipelines + estructura de carpetas en Drive.
2. **Semana 3–4:** tablero en Looker Studio; checklist del expediente como plantilla.
3. **Semana 5–8:** bot de precalificación + formulario Tally + automatizaciones en Make.
4. **Semana 9–12:** recordatorios de cobranza + ficha de inversionista + reporte mensual automatizado.

---

## 4.2 Qué se puede estandarizar o automatizar (y qué no)

Miguel Ángel objetó que el proceso "no se puede sistematizar porque depende del área legal" [ENTREVISTA]. **Tiene razón a medias.** Los plazos de terceros no se controlan. Lo que sí se controla es **cuándo se disparan**, **en paralelo o en serie**, y **cuánto tiempo muerto queda entre una etapa y otra**.

| Etapa | ¿Depende de terceros? | ¿Qué se puede hacer? | Ahorro estimado [SUPUESTO] |
|---|---|---|---|
| Primer contacto y filtro | No | **Automatizar** con bot y formulario | 1–2 días y horas de socios |
| Consulta de partida y gravámenes | SUNARP (horas) | **Estandarizar**: se pide el mismo día que el lead se precalifica | 1–2 días |
| CRI | SUNARP (3–5 días hábiles) | **No se acelera**, pero se pide **el día 1** en paralelo con la tasación, pagado por el cliente | 3–4 días |
| Documentos del cliente | Cliente, municipalidad | **Estandarizar**: checklist con plazos y recordatorios automáticos | 2–3 días |
| Tasación | Perito (4–7 días) | **Alianza** con 2 tasadoras con turno garantizado; se pide el día 1 | 2–3 días |
| Revisión legal de la partida | Abogado | **Estandarizar**: checklist legal y precio fijo; el abogado revisa lo que ya llegó filtrado | 1 día |
| Aprobación | Miguel Ángel | **Matriz de aprobación**: casos estándar (LTV ≤40%, zona A) los aprueba Cristóbal o el Nuevo rol | 1–2 días |
| Propuesta PDF | No | **Automatizar** con una plantilla que se llena desde el CRM | 1 día → 1 hora |
| Exclusividad a preferentes | Inversionistas | **Estandarizar**: 24 h (no 48 h) o hasta respuesta; envío 1:1 | 1 día |
| Fideicomiso, minuta, notaría | Fiduciario, notaría, SUNARP | **No se automatiza**. Minuta modelo pre-aprobada con el fiduciario y la notaría; datos precargados | 1 día |
| Cobranza | No | **Automatizar** recordatorios; escalamiento humano | Horas de seguimiento |

**Resultado esperado:** el ciclo promedio baja de **15–18 días a 9–12 días** sin tocar los plazos de SUNARP ni del perito [SUPUESTO; validar con el experimento E4].

---

## 4.3 Tablero mínimo de KPIs (desde el mes 1)

Se revisa **cada lunes** en 30 minutos entre los socios.

| Área | KPI | Definición | Frecuencia |
|---|---|---|---|
| **Demanda** | Leads por canal | Contactos nuevos por origen (pauta, orgánico, referidor, alianza) | Semanal |
| | % precalificados | Precalificados / leads | Semanal |
| | Costo por lead calificado (CPL-Q) | Inversión en pauta / leads calificados | Semanal |
| | Expedientes abiertos | Con pago de análisis y documentos | Semanal |
| | Tasa de cierre | Desembolsados / expedientes abiertos | Mensual |
| **Velocidad** | Ciclo total | Días desde el lead calificado hasta el desembolso (promedio y máximo) | Semanal |
| | Días por etapa | Verificación, tasación, aprobación, fondeo, estructuración | Semanal |
| **Resultado** | Operaciones desembolsadas | N.º y monto | Semanal |
| | Ticket promedio y mediana | | Mensual |
| | Ingreso por comisiones y margen neto por operación | Comisión – costos directos – referidor | Mensual |
| | Costo hundido | Gasto en operaciones caídas | Mensual |
| **Oferta (inversionistas)** | Capital comprometido disponible | Suma declarada lista para invertir | Semanal |
| | Días de fondeo | Desde que se envía la propuesta hasta que el fondeo queda completo | Semanal |
| | Inversionistas activos y nuevos | | Mensual |
| | % de reinversión | Capital cancelado que se reinvierte en ≤30 días | Mensual |
| **Riesgo** | Morosidad >7 / >30 / >90 días | % de la cartera intermediada | Mensual |
| | LTV promedio de la cartera | Monto / valor de tasación | Mensual |
| | Cartas notariales enviadas | | Mensual |
| **Cumplimiento** | % de operaciones con KYC completo y TCEA bajo el tope BCRP | | Mensual |

---

## 4.4 Procedimientos estándar que conviene escribir (manual de operación)

1. **Criterios de calificación** (1 página): inmueble, titularidad, zona, LTV máximo por zona, montos, exclusiones (salud, terrenos, copropiedad sin todos los titulares, etc.).
2. **Matriz de aprobación**: quién aprueba qué según monto y LTV.
3. **Checklist de expediente** con responsable y plazo por documento.
4. **Hoja de costo total para el cliente**: tasa, comisión, gastos notariales, registrales y del fiduciario, penalidades, TCEA.
5. **Ficha estándar para inversionistas.**
6. **Política de cobranza**: calendario de mensajes y escalamiento.
7. **Política de referidores**: tabla y contrato.
8. **Política PLAFT/KYC** (validar con abogado si CAPEX es sujeto obligado ante la UIF).

---

## 4.5 Perfil del rol comercial-operativo

**Nombre sugerido del puesto:** *Gerente(a) de Operaciones Comerciales*. "Ejecutivo comercial" se queda corto y atrae el perfil equivocado.

**Misión:** llevar cada operación de punta a punta, desde el primer contacto hasta el desembolso, con el criterio de Miguel Ángel. Ser la cara de confianza de CAPEX frente a solicitantes e inversionistas.

**Responsabilidades**
1. Atender y calificar a los solicitantes que llegan precalificados (llamada, visita, negociación de monto y plazo).
2. Coordinar el expediente: SUNARP, tasadora, abogado, fiduciario, notaría. **Dueño(a) del ciclo de días.**
3. Preparar la propuesta y presentarla a inversionistas preferentes; gestionar el fondeo.
4. Mantener el CRM al día (si no está en el CRM, no existió).
5. Reportar los KPIs semanales.
6. Documentar el manual de operación junto a Miguel Ángel durante los primeros 60 días.
7. A los 90 días: aprobar operaciones estándar dentro de la matriz.

**Perfil**
- **Experiencia:** 4 o más años en una de estas áreas: banca hipotecaria o de negocios (ej. funcionario de créditos hipotecarios o pyme), cajas municipales, área legal-registral de una inmobiliaria o notaría, o corretaje inmobiliario con operaciones de financiamiento.
- **Conocimientos imprescindibles:** lectura de partidas registrales, gravámenes y tasaciones; nociones de garantías (hipoteca, fideicomiso); cálculo de cuotas y TCEA.
- **Habilidades:** comunicación que transmite seguridad con dos públicos muy distintos (deudor bajo presión e inversionista exigente); orden; uso de CRM; trato ético.
- **Señales de alerta (descartar):** vendedor de "cierre agresivo" sin conocimiento técnico; quien minimiza el riesgo frente al cliente.

**Compensación sugerida [SUPUESTO]:** fijo de S/5.000–7.000 + variable del **5–8% de la comisión** de cada operación que lleve de punta a punta (con un ticket base son S/1.500–2.400 por operación) + bono trimestral por ciclo ≤12 días y cero incidentes de cumplimiento. A 6–8 operaciones al mes el costo total es de ~S/15–25k, cubierto con menos de una operación base.

**Proceso de selección (3 semanas)**
1. Publicar en LinkedIn y en la red de contactos de banca y notarías (semana 1).
2. Filtro por CV y llamada de 20 minutos (Renzo).
3. **Caso práctico:** entregarle una partida, una tasación y un pedido de monto reales (anonimizados) y pedirle su recomendación y su hoja de costo total (Miguel Ángel).
4. Entrevista con un inversionista de confianza ("¿le confiarías tu dinero?").
5. Período de prueba de 90 días con los KPIs del sprint 3.
