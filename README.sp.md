[ 🌐 عربي ](README.ar.md) | [ 🇩🇪 Deutsch ](README.de.md) | [ 🇫🇷 Français ](README.fr.md) | [ 🇳🇱 Nederlands ](README.nl.md) | [ 🇪🇸 Español ](README.sp.md) | [ 🇬🇧 English ](README.md)
# Rastreador de Tiempos de Vuelo y Servicio CARs 702 y 705 de Canadá (Plantilla de Excel) — Prevenga la Fatiga de Pilotos y las Infracciones de Despacho

![License](https://img.shields.io/badge/license-Apache%202.0-blue)
![Platform](https://img.shields.io/badge/platform-Microsoft%20Excel-217346)
![Regulation](https://img.shields.io/badge/regulation-CARs%20702%2F705-red)

Una **hoja de cálculo de Excel automatizada de seguimiento de tiempos de vuelo y servicio conforme a las Canadian Aviation Regulations (CARs) Partes 702 y 705** diseñada para operadores aéreos comerciales. Esta **calculadora de tiempo de servicio de pilotos** y **herramienta de programación de Gestión del Riesgo de Fatiga (FRMS)** ayuda a los despachadores de vuelo, planificadores de tripulación y Pilotos Jefes a rastrear los **límites rodantes de tiempo de vuelo (ventanas de 28/90/365 días)**, calcular los **máximos del Período de Servicio de Vuelo (FDP)**, monitorear los **períodos de descanso obligatorios** y prevenir las **infracciones de cumplimiento de Transport Canada** antes del despacho del vuelo.

> [**Lance la demostración web interactiva del Rastreador de Tiempos de Vuelo y Servicio CARs 702/705 (Prueba de un Solo Uso)**](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/)
>
> > [**Descargue el Libro de Excel de Cumplimiento de Tiempos de Vuelo y Servicio CARs Multi-Piloto**](https://www.theseusworkshop.com/l/dutytracker?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=cars-flight-duty-tracker)

Elimine los errores manuales de las hojas de cálculo, automatice la **agrupación de tiempos de vuelo del trabajo aéreo de la subparte 702 y de las aerolíneas de la 705 de las CARs**, detecte **riesgos de incumplimiento por fatiga de la tripulación** en segundos y mantenga una única fuente de verdad **lista para auditorías de Transport Canada** para los registros de servicio de los pilotos.

---

## Vista previa interactiva: Calculadora de Servicio de Pilotos CARs 702/705

<img width="1672" height="941" alt="Canadian CARs 702 and 705 Flight Duty Time Tracker Excel Template Dashboard for Pilot Scheduling and Transport Canada Compliance" src="https://github.com/user-attachments/assets/cc792931-2477-40d4-9bd7-e92418817c77" />

> **Pruebe la lógica antes de comprar:** [Pruebe la vista previa web interactiva de la calculadora canadiense de tiempos de vuelo y servicio de pilotos](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/)

---

## Por qué la programación manual de tripulaciones falla en las auditorías de cumplimiento de Transport Canada

La mayoría de las **infracciones de tiempos de vuelo y servicio de las CARs** no son causadas por malas intenciones. Ocurren porque las **ventanas rodantes de tiempo de vuelo**, las **operaciones de vuelo mixtas de las subpartes 702/705**, las **reglas acumulativas de fatiga de la tripulación**, las extensiones por servicio dividido y los libros de registro de pilotos fragmentados son casi imposibles de cruzar manualmente durante un despacho matutino ajetreado.

El riesgo tradicional de la programación manual se ve así:

```text
Pilot assigned to flight
-> Manual check across separate 702 and 705 spreadsheets
-> Rolling 28-day / 90-day boundary miscalculated
-> Violation discovered retroactively during a Transport Canada PVI / Audit
```

Este **libro de Excel de cumplimiento de aviación automatizado** rediseña el flujo de trabajo previo al despacho:

```text
Pilot considered for flight assignment
-> Duty & sector details logged once in a unified tracker
-> Rolling CARs 702/705 limits & FDP matrix validated automatically
-> Non-compliant dispatch blocked BEFORE flight release
```

El problema comercial no es solo la alineación regulatoria—es la **visibilidad operativa previa al vuelo**. Los despachadores de vuelo y los planificadores de tripulación necesitan certeza inmediata sobre si un tripulante puede aceptar legal y seguramente el siguiente sector antes de que se libere el plan de vuelo operativo (OFP).

---

## Tres trampas de cumplimiento de las CARs 702 y 705 en las hojas de cálculo manuales

### Trampa 1 — Las ventanas rodantes de tiempo de vuelo se leen mal como meses calendáricos
Bajo las **CARs de Transport Canada**, los **límites de tiempo de vuelo de 28, 90 y 365 días consecutivos** se deslizan hacia adelante cada 24 horas, no al final de cada mes calendario. Un piloto comercial que registra 95 horas de vuelo entre el 1 y el 28 de mayo y vuela 8 horas el 29 de mayo **no** se reinicia el 1 de junio. La ventana rodante del 1 de junio aún mira hacia atrás hasta el 4 de mayo. Los planificadores de tripulación que reinician mentalmente las horas de los pilotos en los límites del mes subcuentan rutinariamente la exposición acumulada.

### Trampa 2 — Las horas de vuelo no se agrupan entre las subpartes 702 y 705 de las CARs
Cuando el mismo tripulante vuela una **misión de trabajo aéreo / levantamiento bajo la parte 702 de las CARs** el lunes y un **charter de pasajeros conmutado o de aerolínea bajo la parte 705 de las CARs** el miércoles, ambos tiempos de vuelo deben agruparse hacia los mismos **límites acumulativos rodantes de servicio**. Los operadores aéreos que mantienen hojas de seguimiento de Excel separadas para cada subparte del AOC subcuentan sistemáticamente la exposición total a la fatiga del piloto.

### Trampa 3 — Infracciones de FDP y descanso descubiertas después del vuelo
La verificación manual del libro de registro a menudo ocurre después de que se emite la liberación de un vuelo o cuando se totalizan las horas de nómina mensuales. Para cuando se señala una excedencia del **Período de Servicio de Vuelo (FDP) máximo** o del **tiempo libre de servicio (período de descanso)**, la infracción regulatoria ya ha ocurrido—exponiendo al titular del Certificado de Operador Aéreo (AOC) a las **sanciones monetarias administrativas (AMPs) de Transport Canada**.

La verdadera **intercepción previa al despacho** requiere una verificación cruzada automatizada de:
- El **Período de Servicio de Vuelo (FDP)** planificado de hoy y la **hora de presentación local (aclimatado vs. no aclimatado)**
- La **acumulación de tiempo de vuelo** histórica del piloto de 28/90/365 días
- El **número de sectores** programado y la duración promedio de los sectores
- Los **intervalos de descanso obligatorios previos y posteriores al vuelo** y el **tiempo libre de servicio de 36 horas / 7 días**

---

## Para quién es esta plantilla de Excel de cumplimiento de aviación (Roles y escenarios de uso)

Si busca una alternativa asequible al software empresarial de gestión de tripulaciones sin sacrificar la precisión regulatoria, esta herramienta está creada para sus escenarios operativos diarios:

| Rol de Aviación | Escenario de Búsqueda y Flujo de Trabajo Operativo | Beneficio Principal de Cumplimiento |
|---|---|---|
| **Despachadores de Vuelo** | Necesitan una **calculadora de legalidad de pilotos previa al despacho** para verificar la disponibilidad de la tripulación durante las liberaciones matutinas de vuelos o solicitudes de charter de último momento. | Banderas instantáneas de **cumplimiento Go / No-Go** antes de firmar el plan de vuelo operativo. |
| **Planificadores de Tripulación** | Buscan una **hoja de cálculo de roster y seguimiento de fatiga de la tripulación** para construir horarios mensuales sin exceder los topes rodantes de 28/90/365 días. | Visibilidad en tiempo real de la **capacidad legal de vuelo restante** por piloto en toda la flota. |
| **Pilotos Jefes y DFO** | Requieren una **plantilla de monitoreo de tiempo de vuelo del Piloto Jefe** para supervisar la carga de trabajo de la tripulación, aprobar extensiones de servicio y prevenir la fatiga sistémica. | Panel centralizado que muestra la **agrupación de horas mixtas CARs 702/705** y alertas de alta utilización. |
| **Gerentes de SMS y Seguridad de Aviación** | Buscan un **registro de cumplimiento de Transport Canada listo para auditoría** para prepararse para las Inspecciones de Validación de Programas (PVI) y las auditorías SMS. | Registros históricos estandarizados y a prueba de manipulación sin posprocesamiento requerido. |
| **Operadores AOC Pequeños y Medianos** | Operadores regionales canadienses, de evacuación médica, bush y charter (3–30 pilotos) que necesitan **software de bajo costo de seguimiento de servicio de vuelo en Excel**. | Reemplaza los registros de papel dispersos y las hojas frágiles hechas a mano con un **motor de cumplimiento de Microsoft Excel** determinista. |

---

## Lo que le ayuda a rastrear: Mapeo de punto de dolor a solución

En lugar de actuar como un libro de registro digital pasivo, este libro funciona como un **motor de reglas regulatorias CARs 702/705** activo:

| Punto de Dolor Operativo (Lo que falla manualmente) | Métrica de Cumplimiento de Alta Frecuencia Rastreada | Solución Automatizada del Libro (Cómo lo resuelve) |
|---|---|---|
| **Cálculo manual de ventanas rodantes:** Contar hacia atrás 28, 90 y 365 días en un calendario de pared para más de 15 pilotos cada mañana. | **Límites Rodantes Acumulativos de Tiempo de Vuelo** (`100h / 28d`, `300h / 90d`, `1,000h / 365d`) | Las fórmulas de matriz dinámica deslizan automáticamente las ventanas retrospectivas de 28, 90 y 365 días hacia adelante cada día y calculan las horas legales restantes exactas. |
| **Búsquedas complejas en la tabla FDP:** Cruzar las horas de presentación de los pilotos con los aterrizajes programados en el manual de las CARs bajo presión de tiempo. | **Matriz del Período de Servicio de Vuelo (FDP) de la parte 705 de las CARs** (Hora de Presentación × Número de Sectores) | Las tablas de búsqueda regulatorias pre-codificadas ajustan automáticamente el **FDP Legal Máximo** del piloto en el momento en que ingresa la hora de presentación y el número de sectores. |
| **Vuelo multi-subparte en silos:** Olvidar sumar las horas de patrulla contra incendios de la parte 702 del martes a los límites del charter de pasajeros de la parte 705 del viernes. | **Agrupación de Horas entre Subpartes (CARs 702 / 703 / 704 / 705)** | Un esquema de datos unificado etiqueta cada vuelo por subparte pero agrega todas las horas de vuelo y servicio en un único perfil maestro de cumplimiento por piloto. |
| **Reasignaciones de último momento:** Un cliente añade dos tramos adicionales a mitad del día, y el despacho no sabe si la tripulación excederá los límites de servicio. | **Estado de Legalidad Go/No-Go Previo al Despacho** | El formato condicional en tiempo real activa alertas visuales de **Advertencia (Cerca del Límite)** y **Infracción (Bloqueado)** *antes* de que se despache el vuelo. |
| **Preparación de auditoría caótica:** Pasar días limpiando fórmulas rotas y fechas faltantes antes de una inspección de Transport Canada. | **Registros Históricos Listos para Auditoría de Transport Canada** | Un libro mayor estructurado y filtrable le permite exportar historiales de cumplimiento limpios por piloto, matrícula de aeronave, rango de fechas o estado regulatorio con un solo clic. |

---

## La Lógica Comercial y la Metodología

### El Problema Comercial Central: Cumplimiento de Alto Impacto vs. Economía del Software
Los operadores aéreos canadienses pequeños y medianos (con 3 a 30 pilotos) enfrentan una presión estructural. Por un lado, **las regulaciones de riesgo de fatiga y tiempo de servicio de Transport Canada** conllevan exactamente la misma responsabilidad estricta para una operación charter de 10 pilotos que para una gran aerolínea. Por otro lado, las plataformas SaaS empresariales de programación de tripulaciones (como Navblue, Jeppesen o los módulos empresariales de FL3XX) requieren elevadas tarifas anuales de licencia, onboarding prolongado y administración dedicada de TI. Forzados a elegir, los AOC más pequeños recurren a hojas de cálculo caseras—introduciendo **decaimiento silencioso de fórmulas, errores de copiar y pegar, y riesgo de aplicación retroactiva**.

### La Metodología: Intercepción Determinista Previa al Despacho
Para resolver esto sin los costos empresariales, este libro aplica una **Metodología de Intercepción Determinista Previa al Despacho** construida de forma nativa dentro del motor de cálculo de Microsoft Excel:

1. **Normalización Relacional de Datos de Entrada Única:** En lugar de organizar las hojas por mes o por subparte de las CARs (lo que rompe el seguimiento longitudinal), todas las entradas operativas se capturan en un único libro mayor de transacciones normalizado (`Flight & Duty Log`). Cada entrada está indexada por `Pilot_ID`, `UTC/Local_Date`, `Subpart_Tag`, `Report_Time` y `Sector_Count`.
2. **Modelado de Matrices Temporales de Ventana Deslizante:** En lugar de usar rangos estáticos de suma mensual (`SUM(B2:B31)`), el motor usa una evaluación de matriz dinámica acotada por fechas (`[Current_Assignment_Date - N_Days, Current_Assignment_Date]`). Cada fila evalúa su propio contexto histórico en los horizontes de 28, 90 y 365 días simultáneamente, garantizando que las infracciones históricas y las proyecciones futuras de horarios se calculen con 100% de consistencia matemática.
3. **Codificación de Matriz Regulatoria Bidimensional:** La **Tabla FDP de la parte 705 de las CARs** (que gobierna las horas máximas de servicio según los ritmos circadianos de la hora del día y los sectores de trabajo) está codificada de forma inmutable en una matriz de referencia. Mediante la coincidencia multi-criterio (`INDEX/MATCH` a través de umbrales de bandas horarias y rangos de sectores), el libro elimina el error humano de búsqueda durante las ventanas de despacho de alta presión.
4. **Control de Cumplimiento Shift-Left:** Tomado del principio de pruebas "Shift-Left" de la ingeniería de software, la validación de cumplimiento se mueve de la **auditoría posterior al vuelo** a la **fase de simulación previa a la asignación**. Al calcular `Projected_Accumulation = Historical_Rolling_Total + Planned_Duty_Input`, el modelo actúa como un disyuntor preventivo—señalando asignaciones ilegales mientras aún son hipotéticas.

---

## Comparación del Flujo de Trabajo Operativo: Hojas Manuales vs. Rastreador CARs Automatizado

**Perfil de Referencia del Operador:** 12 pilotos comerciales | AOC mixto de **parte 702 (Trabajo Aéreo)** y **parte 705 (Aerolínea/Charter)** de las CARs | Una única mesa central de despacho.

**El Cuello de Botella Operativo:** Cada mañana, el despachador de vuelo dedica 90 minutos a verificar manualmente los límites rodantes de servicio de los pilotos antes de liberar el horario de vuelos del día. Las horas de vuelo están divididas en dos archivos de Excel desconectados—uno para operaciones 702 y otro para 705. Cuando un capitán vuela bajo ambas subpartes en la misma semana, los totales acumulados agrupados deben calcularse a mano. Durante un pico estacional de 90 días, dos excedencias de límites rodantes se pasaron por alto—ambas descubiertas *después* de la salida de la aeronave, creando una exposición inmediata al **cumplimiento de Transport Canada**.

| Dimensión Operativa y de Cumplimiento | Antes: Hojas de Cálculo Manuales Desconectadas | Después: Libro Unificado de Cumplimiento CARs 702/705 |
|---|---|---|
| **Arquitectura de Registros de Vuelo y Servicio** | Fragmentada en archivos separados de las CARs 702 y 705; las pestañas mensuales rompen las retrospectivas rodantes | **Base de datos única unificada en Excel** con seguimiento longitudinal continuo de varios años |
| **Verificación de Legalidad Matutina Previo al Despacho** | ~90 minutos de conteo manual de fechas y verificaciones con calculadora para 12 pilotos | **Menos de 3 segundos por piloto** mediante banderas automatizadas del panel previo al despacho |
| **Agrupación de Horas Multi-Subparte (702/705)** | Copiar y pegar manual propenso a errores entre hojas al final de la semana | **Agrupación 100% automatizada en tiempo real** entre todas las subpartes de las CARs al ingresar los datos |
| **Validación de Tabla FDP y Límites de Sectores** | Búsqueda manual en manuales regulatorios en PDF; alto riesgo de malinterpretar las bandas horarias circadianas | **Cálculo dinámico instantáneo del FDP** basado en la hora de presentación del piloto y los sectores programados |
| **Detección de Infracciones y Riesgo de Auditoría de TC** | **Descubrimiento posterior al vuelo**; aplicación retroactiva de Transport Canada y exposición a AMPs | **Intercepción previa al despacho**; asignaciones de tripulación no conformes bloqueadas antes de la liberación del vuelo |

---

## Flujo de Trabajo de Inicio Rápido: Cómo Validar la Legalidad de un Piloto en 4 Pasos

¿Quiere ver qué tan rápido puede verificar la disponibilidad legal de un piloto? Siga este flujo de trabajo de 4 pasos para probar un despacho de vuelo único ahora mismo, y luego pase al seguimiento de flota completo:

1. **Lance el Sandbox Web Interactivo (Paso 1 — Prueba Gratuita de un Solo Piloto):**
   Abra la [**Vista Previa Web en Vivo de la Calculadora de Tiempos de Vuelo y Servicio CARs 702/705**](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/) en su navegador. No se requiere instalación para probar un escenario único de asignación de tripulación.
2. **Ingrese la Hora de Presentación y el Número de Sectores Planificados (Paso 2 — Verificación de la Matriz FDP):**
   Ingrese la **hora de presentación local** programada de su piloto, las **horas de vuelo planificadas** y el **número de sectores de vuelo**, luego seleccione la regla de operación (**parte 702 o parte 705 de las CARs**). Observe cómo la calculadora determina instantáneamente el **Período de Servicio de Vuelo (FDP) Legal Máximo**.
3. **Verifique los Límites Acumulativos Rodantes de 28 / 90 / 365 Días (Paso 3 — Compuerta Previo al Despacho):**
   Revise el **Indicador de Estado de Cumplimiento Previo al Despacho** automatizado. El motor señala de inmediato si el vuelo propuesto empuja al piloto por encima de los topes regulatorios de Transport Canada de **100 horas (28 días)**, **300 horas (90 días)** o **1.000 horas (365 días)**.
4. **Actualice al Libro de Excel Multi-Piloto Completo (Paso 4 — Operaciones Continuas de Flota):**
   La vista previa web es ideal para una verificación de legalidad única, pero se reinicia al cerrar su navegador. Para guardar registros históricos de pilotos, agrupar horas entre **más de 30 pilotos** y mantener **registros de auditoría permanentes de Transport Canada**, [**Descargue Aquí la Plantilla de Excel Completa y Reutilizable de Tiempos de Vuelo y Servicio CARs 702/705**](https://www.theseusworkshop.com/l/dutytracker?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=cars-flight-duty-tracker).

---

*El valor operativo no es que Microsoft Excel reemplace el juicio de cumplimiento de un Piloto Jefe. El valor es que los **cálculos regulatorios rutinarios de las CARs 702/705** dejan de depender de la memoria humana, el conteo manual de calendarios y las hojas de cálculo fragmentadas.*

---

## Por Qué la Regulación Funciona Así

Transport Canada regula la fatiga de las tripulaciones de vuelo porque la fatiga es un peligro para la seguridad, no solo un problema administrativo. Las reglas están diseñadas para controlar la carga de trabajo acumulada, la programación del servicio, la oportunidad de descanso y el riesgo de pérdida de alerta.

Por eso las regulaciones consideran factores como:

- el tiempo total de vuelo en ventanas de días consecutivos
- los límites del período de servicio de vuelo
- la hora de presentación y la programación circadiana
- el número de vuelos o sectores
- los períodos de descanso y el tiempo libre de servicio
- la supervisión y los registros del operador

La lógica operativa es directa: dos horarios pueden tener el mismo número de horas de servicio pero crear diferentes riesgos de fatiga según la programación, la frecuencia, el número de sectores y la acumulación previa.

Referencias oficiales útiles:

- [Transport Canada: Flight and duty time regulations](https://tc.canada.ca/en/aviation/commercial-air-services/fatigue-management-aviation/flight-duty-time-regulations-prescriptive-vs-performance-based-options)
- [Transport Canada Advisory Circular AC 700-047](https://tc.canada.ca/en/aviation/reference-centre/advisory-circulars/advisory-circular-ac-no-700-047)
- [Canadian Aviation Regulations SOR/96-433](https://tc.canada.ca/en/corporate-services/acts-regulations/list-regulations/canadian-aviation-regulations-sor-96-433)

---

## Cómo Funcionan las Ventanas Rodantes

El límite de acumulación de 28 días requiere que el tiempo total de vuelo en cualquier ventana consecutiva de 28 días
no exceda las 100 horas. La ventana se desliza hacia adelante cada día — no es un mes calendario.

| Fecha | La ventana cubre | Efecto neto |
|---|---|---|
| 15 de junio | 19 de mayo – 15 de junio | 92 h en la ventana |
| 16 de junio | 20 de mayo – 16 de junio | − horas voladas el 19 de mayo + horas voladas el 16 de junio |
| 17 de junio | 21 de mayo – 17 de junio | continúa deslizándose |

**La trampa en números:**  
El piloto tiene 92 horas en la ventana. Programado para 10 horas el 16 de junio.

- Si voló 4 horas el 19 de mayo: 92 − 4 + 10 = **98 h** — legal.  
- Si voló 0 horas el 19 de mayo: 92 − 0 + 10 = **102 h** — infracción.

Un modelo mental de reinicio mensual aprueba ambos. La ventana rodante no.

Cada piloto lleva tres de estos cálculos simultáneamente: 28 días, 90 días y 365 días.
Para 15 pilotos, eso son 45 cálculos rodantes en vivo por ciclo de despacho, cada uno requiere hasta
365 días de búsqueda histórica. Las matemáticas no requieren juicio. La automatización elimina la clase de error por completo.

**Por qué la hora de presentación también gobierna el FDP:** Los límites FDP de la parte 705 dependen de cuándo comienza el servicio.
Un servicio que comienza a las 09:00 puede durar legalmente hasta 13 horas; el mismo servicio que comienza a la 01:00
está limitado a cerca de 11 horas — porque se extiende hacia la ventana circadiana 02:00–05:59 donde
las tasas de error por fatiga aumentan bruscamente. Una diferencia de 30 minutos en la hora de presentación puede cambiar
el máximo legal hasta en 2 horas. El número de sectores añade una segunda dimensión: cada aproximación
y aterrizaje adicional acumula carga cognitiva medible, y la matriz reduce el FDP
permitido en consecuencia.

---

## Lógica del Libro de Trabajo

El libro de trabajo está organizado en torno a un flujo de trabajo de despacho práctico:

1. Ingresar los datos del piloto y la asignación planificada.
2. Identificar el contexto de la operación.
3. Extraer el historial de servicio y vuelo relevante para ese piloto.
4. Calcular los totales de las ventanas rodantes.
5. Comparar la asignación planificada con los límites configurados.
6. Marcar el estado claro, de advertencia o de riesgo.
7. Preservar los registros para revisión y exportación.

El libro de trabajo está pensado para ser una herramienta de apoyo a la decisión y análisis. No reemplaza la responsabilidad legal del operador de interpretar y aplicar las CARs vigentes, el manual de operaciones de la empresa, las exenciones aprobadas o los procedimientos FRMS.

---

## Compra

Use el libro de trabajo de Excel completo aquí:

[Compre el rastreador de Excel completo](https://www.theseusworkshop.com/l/dutytracker?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=cars-flight-duty-tracker)

---

## Limitaciones

- **Dependencia de la integridad de datos** — los cálculos son tan precisos como las entradas; los registros tardíos, faltantes o incorrectos producen un estado de cumplimiento incorrecto sin advertencia
- **No es una opinión legal** — este libro de trabajo refleja la interpretación del autor de las regulaciones; la posición oficial de Transport Canada rige, y las aplicaciones de casos límite deben validarse con asesoría legal o su Inspector Principal de Operaciones de TC
- **Retraso en enmiendas regulatorias** — las enmiendas de las CARs no se reflejan automáticamente; los operadores son responsables de monitorear los cambios regulatorios de TC y actualizar el libro de trabajo en consecuencia
- **Alcance: solo partes 702 y 705** — los operadores bajo la parte 703 (taxi aéreo) o la parte 704 (servicio conmutado) trabajan bajo límites específicos diferentes no codificados en esta versión
- **Techo de escala** — diseñado para 3–30 pilotos; más allá de aproximadamente 30, la profundidad de cálculo puede degradar el rendimiento de Excel
- **Sensibilidad a la versión de Excel** — requiere Excel 2016 o posterior en Windows; el comportamiento en Excel para Mac o Office 365 web puede diferir
- **Casos límite no totalmente automatizados** — las disposiciones de tripulación aumentada, las reglas de servicio dividido y ciertas extensiones de descanso implican condiciones regulatorias que requieren juicio del despachador y no están totalmente codificadas en esta versión

---

## Acerca de Este Proyecto

Este libro de trabajo es parte de un esfuerzo más amplio por traducir requisitos operativos y regulatorios complejos
en herramientas ligeras que las organizaciones pequeñas y medianas realmente puedan usar.

Sin ERP. Sin proyecto de software personalizado. Sin cuentas adicionales.

Solo lógica de negocio clara, datos estructurados y apoyo a la decisión repetible —
entregado en software que su equipo ya tiene.

Si su operación implica problemas de cumplimiento, programación o asignación de recursos
que actualmente viven en la cabeza de alguien o en una hoja de cálculo desconectada,
[vea qué más está disponible →](https://www.theseusworkshop.com)

---

## License

Distribuido bajo la [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).

---

