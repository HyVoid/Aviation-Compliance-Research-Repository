[ 🌐 عربي ](README.ar.md) | [ 🇩🇪 Deutsch ](README.de.md) | [ 🇫🇷 Français ](README.fr.md) | [ 🇳🇱 Nederlands ](README.nl.md) | 🇪🇸 [ Español ](README.sp.md) | [ 🇬🇧 English ](README.md)

# Prevenga las infracciones de tiempos de vuelo y servicio antes del despacho

![License](https://img.shields.io/badge/license-Apache%202.0-blue)
![Platform](https://img.shields.io/badge/platform-Microsoft%20Excel-217346)
![Regulation](https://img.shields.io/badge/regulation-CARs%20702%2F705-red)

**Diseñado para operadores canadienses de las partes 702 y 705 que necesitan rastrear el tiempo de vuelo, el tiempo de servicio, la exposición a la fatiga y los límites de cumplimiento rodantes antes de asignar a un piloto.**

[Vista previa en vivo](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/) | [Comprar Excel completo](https://www.theseusworkshop.com/l/dutytracker?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=cars-flight-duty-tracker)

Rastree los límites rodantes de tiempo de vuelo, detecte riesgos de incumplimiento en segundos y mantenga una única fuente de verdad auditable para los registros de servicio de los pilotos.

---

## Vista previa rápida

<img width="1672" height="941" alt="ChatGPT Image May 25, 2026, 11_47_04 AM" src="https://github.com/user-attachments/assets/cc792931-2477-40d4-9bd7-e92418817c77" />

> Vea la vista previa interactiva del libro de trabajo: [demostración del rastreador de servicio de pilotos](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/)

---

## Por qué existe esto

La mayoría de las infracciones de tiempos de vuelo y servicio no son causadas por malas intenciones.

Suelen ocurrir porque las ventanas rodantes, la actividad mixta 702/705, las reglas acumulativas de fatiga, los servicios reasignados y los registros fragmentados son difíciles de monitorear manualmente.

El riesgo es simple:

```text
Pilot assigned
-> Manual check
-> Prior records missed
-> Violation discovered after the flight
```

Este libro de trabajo está diseñado para cambiar el flujo de trabajo:

```text
Pilot considered for assignment
-> Duty record entered once
-> Rolling limits checked automatically
-> Compliance risk flagged before dispatch
```

El problema comercial no es solo la regulación. Es la visibilidad operativa. Los despachadores y planificadores necesitan saber si un piloto puede tomar legal y seguramente la siguiente asignación antes de que se libere el vuelo.

---

## Tres trampas de cumplimiento que atrapan a los operadores

### Trampa 1 — Las ventanas rodantes se leen mal como períodos calendáricos

Los límites de 28, 90 y 365 días se deslizan hacia adelante cada día, no cada mes.
Un piloto que voló 95 horas entre el 1 y el 28 de mayo y luego voló 8 horas el 29 de mayo
**no** se ha reiniciado cuando comienza junio. La ventana del 1 de junio aún alcanza hasta el 4 de mayo.

Los planificadores que reinician mentalmente los límites en los límites de mes subcuentan rutinariamente la exposición.
Esta es la trampa estructuralmente más invisible: el modelo mental se siente correcto; el cálculo está mal.

### Trampa 2 — Las horas no se agrupan entre 702 y 705

Cuando el mismo piloto realiza un levantamiento aéreo bajo la parte 702 el lunes y un charter de pasajeros
bajo la parte 705 el miércoles, ambos conjuntos de horas cuentan para los mismos límites de acumulación rodantes.

Los operadores que mantienen hojas de seguimiento separadas para cada subparte — una división natural del flujo de trabajo —
subcuentan sistemáticamente. La regulación no reconoce ese límite operativo.

### Trampa 3 — Las infracciones se descubren después del vuelo

La verificación manual normalmente ocurre después de que se emite una asignación de servicio, o después de que el vuelo
ha partido. Para cuando se identifica una infracción, el incumplimiento ya ha ocurrido.
La aplicación de Transport Canada se aplica de forma retroactiva.

La interceptación previa al vuelo requiere que el estado de cumplimiento sea visible *antes* de que se asigne un piloto —
lo que requiere que todos los datos históricos estén actualizados y que todos los cálculos se ejecuten automáticamente en
el momento del despacho.

Normalmente está oculto en la relación entre:

- el servicio planificado de hoy
- el historial de servicio previo del piloto
- la hora de presentación
- el número de sectores
- la acumulación de tiempo de vuelo
- el descanso requerido
- los procedimientos específicos del operador

Por eso la revisión manual con hojas de cálculo a menudo detecta el problema tarde, o lo omite por completo.

---

## Para quién es esta herramienta

| Usuario | Caso de uso práctico |
|---|---|
| Despachadores de vuelo | Verificar la disponibilidad del piloto antes de emitir una autorización de despacho |
| Planificadores de tripulación | Construir listas de turnos con visibilidad de la capacidad legal restante |
| Pilotes jefes | Revisar la carga de trabajo de los pilotos y la exposición acumulada antes de aprobar asignaciones |
| Gerentes de seguridad | Mantener registros estructurados para revisión interna y preparación de auditorías |
| Pequeños operadores AOC | Reemplazar el seguimiento manual disperso con un flujo de trabajo de Excel ligero y único |

Más adecuado para operadores canadienses con 3–30 pilotos que realizan operaciones mixtas 702/705,
donde el software de gestión de tripulación dedicado es prohibitivo en costo pero los enfoques manuales ya no escalan.

---

## Lo que hace el libro de trabajo

### Registro de tiempo de servicio
Un único punto de entrada de datos para todos los registros de servicio de los pilotos. Los despachadores registran la información básica de vuelo y servicio
una sola vez; los cálculos se ejecutan automáticamente en segundo plano.

### Monitoreo de ventanas rodantes
Cálculo automático de los límites de acumulación de la parte 705 en las tres ventanas regulatorias simultáneamente:
- 100 horas en cualquier período de 28 días consecutivos
- 300 horas en cualquier período de 90 días consecutivos
- 1.000 horas en cualquier período de 365 días consecutivos

### Estado de cumplimiento previo al despacho
El estado de cumplimiento de cada piloto es visible antes de que se emita la asignación.
Sin referencia cruzada manual. Sin descubrimiento posterior al vuelo.

### Validación de la matriz FDP
Los límites del período de servicio de vuelo (FDP) de la parte 705 — una matriz de dos variables de hora de presentación × número de sectores —
están pre-codificados. El máximo FDP legal se actualiza automáticamente según cuándo se presenta el piloto
y cuántos sectores están programados.

### Informes listos para auditoría
Cada entrada está estructurada y es rastreable desde el primer día. Los registros históricos de cumplimiento pueden
filtrarse por piloto, rango de fechas o estado y exportarse sin posprocesamiento.

---

## Escenario de ejemplo

**Perfil del operador:** 12 pilotos. Operaciones mixtas de las partes 702 y 705. Una única oficina de despacho.

**El problema:** Cada mañana, el despachador pasa 90 minutos verificando manualmente los límites
de servicio rodantes antes de asignar los vuelos del día. Las horas de vuelo se rastrean en dos
hojas de cálculo separadas — una para operaciones 702, otra para 705. Cuando un piloto vuela bajo ambas subpartes
en la misma semana, los totales agrupados se consolidan a mano.

A lo largo de tres meses de operaciones, se detectaron dos excedencias de límites — ambas después de que el vuelo
ya había partido.

| | Antes | Después |
|---|---|---|
| Estructura de registros | Dos hojas separadas, una por subparte | Un libro de trabajo unificado único |
| Tiempo de verificación matutina | ~90 min en todos los pilotos | Menos de 3 segundos por piloto |
| Agrupación de horas 702/705 | Consolidación manual | Automática en ambas subpartes |
| Descubrimiento de infracciones | Posterior al vuelo; exposición retroactiva ante TC | Previo al despacho; bloqueado antes de la asignación |

---

El valor no es que Excel reemplace el juicio de cumplimiento. El valor es que los cálculos rutinarios dejan de depender de la memoria, las verificaciones de copiar y pegar y los archivos fragmentados.

---

## Por qué la regulación funciona así

Transport Canada regula la fatiga de la tripulación de vuelo porque la fatiga es un peligro para la seguridad, no solo un problema administrativo. Las reglas están diseñadas para controlar la carga de trabajo acumulada, la programación del servicio, la oportunidad de descanso y el riesgo de pérdida de alerta.

Por eso las regulaciones consideran factores como:

- el tiempo total de vuelo en ventanas de días consecutivos
- los límites del período de servicio de vuelo
- la hora de presentación y el ritmo circadiano
- el número de vuelos o sectores
- los períodos de descanso y el tiempo libre de servicio
- la supervisión y los registros del operador

La lógica operativa es directa: dos horarios pueden tener el mismo número de horas de servicio pero crear diferentes riesgos de fatiga según la programación, la frecuencia, el número de sectores y la acumulación previa.

Referencias oficiales útiles:

- [Transport Canada: Flight and duty time regulations](https://tc.canada.ca/en/aviation/commercial-air-services/fatigue-management-aviation/flight-duty-time-regulations-prescriptive-vs-performance-based-options)
- [Transport Canada Advisory Circular AC 700-047](https://tc.canada.ca/en/aviation/reference-centre/advisory-circulars/advisory-circular-ac-no-700-047)
- [Canadian Aviation Regulations SOR/96-433](https://tc.canada.ca/en/corporate-services/acts-regulations/list-regulations/canadian-aviation-regulations-sor-96-433)

---

## Cómo funcionan las ventanas rodantes

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

## Lógica del libro de trabajo

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

## Acerca de este proyecto

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
