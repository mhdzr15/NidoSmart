---
title: "Arquitectura eléctrica, hidráulica y de comunicaciones"
project: "NidoSmart"
document_type: "business-plan"
status: "draft"
version: "1.7"
last_updated: "2026-10-15"
---

# Arquitectura eléctrica, hidráulica y de comunicaciones

## 9.1 Sistema eléctrico

La instalación deberá contar con:

* Tablero eléctrico principal.
* Subtablero por módulo.
* Protección contra sobrecorriente.
* Protección contra descargas.
* Puesta a tierra.
* Medición energética por módulo.
* Circuitos separados para cargas críticas.
* Paros de emergencia.
* Contactores y relevadores industriales.
* Variadores para ventiladores cuando sea conveniente.
* UPS para controladores, comunicaciones y sensores.
* Generador o sistema de respaldo para cargas críticas.
* Posibilidad de integrar energía solar posteriormente.

Las cargas críticas son:

* Ventilación mínima.
* Agua.
* Controladores.
* Comunicaciones.
* Alarmas.
* Iluminación básica.

### 9.1.1 Arquitectura eléctrica preliminar (revisión septiembre 2026)

**Objetivo de esta revisión:** definir la arquitectura eléctrica mínima necesaria para cotizar la nave y su infraestructura asociada, a partir de las cargas reales ya confirmadas en las cotizaciones de FamTECH (v1/v2/v3, ver [registro de cotizaciones](../../evidence/quotations/README.md)) y de los equipos ya decididos en [Automatización](./08-automatizacion.md). **No se inventan potencias no proporcionadas por los proveedores** — donde el dato no existe, se marca explícitamente como pendiente.

#### Cargas conocidas (potencia confirmada por cotización)

| Equipo | Potencia | Tensión/fase | Fuente | Circuito propuesto |
|---|---|---|---|---|
| Motorreductor del skip-hoist feeder (alimentación) | **0.75 kW**, 1.5 A nominal, LRA 9–10.5 A | **380V trifásico** (confirmado, 2026-10-15); compatible con red mexicana 60 Hz sin costo adicional (confirmación informal de correo del 2026-07-21, aún sin cotización formal por escrito — ver [registro de cotizaciones](../../evidence/quotations/README.md#nuevos-pendientes-eléctricos-2026-09-18)) | FamTECH v1/v2, ítem I.3 "Drive unit"; datos de corriente confirmados 2026-10-15 ([respuesta](../../evidence/correspondence/2026-10-15_FamTECH_email_respuesta-lote3-electrico.rtfd/)) | Normal (no crítico) |
| Motor de la banda recolectora de huevo | **0.55 kW**, 1.3 A nominal, LRA 7.8–9.1 A | **380V trifásico** (confirmado, 2026-10-15) | FamTECH v1/v2, ítem IV.4 "drive unit" | Normal (no crítico) |
| Motor de la banda de retiro de gallinaza | **0.75 kW**, 1.4–1.7 A nominal (tabla de FamTECH da 1.5 A) | **380V trifásico**, motor de inducción (confirmado, 2026-10-15 — antes sin dato) | FamTECH v1/v2, ítem III.2/III.4 | Normal (no crítico) |
| Ventiladores/extractores (ventilación transversal) | **1.1 kW cada uno × 2 = 2.2 kW**, 2.2 A nominal c/u, LRA 13–15.4 A c/u ("50″ fan, domestic special power") | **380V trifásico** (confirmado, 2026-10-15) | FamTECH v3, ítem V.1 "Fan" | **Crítico** (ventilación mínima) |
| Actuadores lineales de entradas de aire CJ01 (2) + controladores de entrada (2) | **≈43 W pico c/u** (24V×1.8A a plena carga), 10–15W en reposo (ciclo corto — se desenergiza al llegar a posición) | **DC 24V** (confirmado, 2026-10-15) | FamTECH v3, ítems V.4–V.5 | **Crítico** (ventilación mínima) |
| Sensores DMR de temperatura/humedad | **0.8 W c/u continuos**, ≈0.033 A | DC 24V (confirmado, 2026-10-15) | FamTECH v3 | **Crítico** (controladores) |
| Bombas sumergibles del sistema de cooling pad | 0.55 kW cada una × 2 | Sin especificar | FamTECH v3, ítem V.7 "Submersible pump" | **No aplica** — cooling pads descartados para este sitio (ver [Automatización — Control ambiental](./08-automatizacion.md#control-ambiental), "Cooling pads — no se justifican") |
| Sistema de iluminación de pasillo (14 focos DC48V-7W-3000K regulables, 1 controlador de dimming) | **14 × 7W = 98W** en el lado DC48V; consumo real del lado de red (AC) depende de la eficiencia del driver del controlador de dimming, **no especificada**. **Resuelto en sentido de "sin cambio" (2026-10-15, con una inconsistencia numérica sin aclarar — ver [Automatización — Iluminación](./08-automatizacion.md#iluminación)):** FamTECH indicó que los 14 focos ya cotizados cubren la nave completa (ambos pasillos del bloque "double-sided"), sin partida adicional — pero esto no cuadra aritméticamente con su propia explicación anterior de "2 lámparas por punto × 7 puntos por pasillo". Mientras se aclara, se mantiene 98W como el valor de diseño. | DC48V (requiere driver/fuente AC→DC48V, presumiblemente integrado en el controlador de dimming) | FamTECH v4 (2026-09-21), ítem V "Lighting system" — ver [Automatización — Iluminación](./08-automatizacion.md#iluminación) | **Crítico** (iluminación básica) |

**Suma de potencia nominal conocida y necesaria para el alcance actual (excluye cooling pads, ya descartados): ≈4.35 kW** (0.75 + 0.55 + 0.75 + 2.2 + 0.098 kW; los actuadores CJ01 y sensores DMR suman unos pocos watts adicionales, despreciables frente a los motores). Esta cifra es la suma de placas de motor/equipo, **no** una demanda máxima calculada (no incluye factores de simultaneidad, arranque ni las cargas aún sin potencia — ver "Cargas pendientes" abajo); no debe usarse todavía para dimensionar el servicio de CFE, el generador ni el calibre de conductores. La iluminación (98W) es una carga eléctricamente trivial frente a los motores — no cambia el orden de magnitud del cálculo, pero sí introduce un requisito de diseño nuevo: un circuito a 48V DC (no 120/220V AC directo) para las luminarias, alimentado desde el controlador de dimming.

**Nota sobre continuidad del paquete de control ambiental:** el presupuesto consolidado ([sección 6](../investment-project/07-presupuesto-consolidado-inversion-inicial.md#6-ventilación-y-control-ambiental)) marca la cotización v3 como "Cotizado, en pausa" porque la decisión de 2026-07-22 pausó el paquete completo. Sin embargo, [Automatización — Control ambiental](./08-automatizacion.md#control-ambiental) ya aclaró que **los ventiladores, entradas de aire y controlador sí son necesarios** (la ventilación mínima no es opcional, [DEC-006](../governance/registro-de-decisiones.md#dec-006--automatización-intensiva-de-al-menos-90-de-las-tareas-repetitivas)) — lo que está descartado son específicamente los cooling pads. Esta arquitectura eléctrica asume que los 2 ventiladores de 1.1 kW y el sistema de entradas de aire motorizadas sí forman parte de la carga real de la nave, aunque su partida presupuestal siga etiquetada "en pausa".

**Arranque de motores (dato relevante para protecciones y generador):** el pendiente ya abierto en automatización ("Si el controlador YB permite programar ventilación escalonada... o solo operación on/off") implica que, si la respuesta es on/off, los 2 ventiladores arrancan a través de línea (sin variador), generando corriente de arranque varias veces la nominal — relevante para el dimensionamiento del generador y de las protecciones (ver abajo). Esto no se puede calcular sin la corriente de arranque real del motor (dato pendiente de FamTECH).

#### Cargas críticas — mapeo a equipo real

| Carga crítica (§9.1) | Equipo que la cubre | Potencia | Estado |
|---|---|---|---|
| Ventilación mínima | 2 ventiladores 1.1 kW + actuadores de las 12 entradas de aire CJ01 (2 "Electric linear actuator") | 2.2 kW (2.2 A nominal c/u) + actuadores ≈43W pico c/u, 24VDC | **Resuelto (2026-10-15)** |
| Agua | Bomba principal + bomba de respaldo ([9.2](#92-sistema-hidráulico)) + bomba dosificadora automática (FamTECH v1/v2, ítem II.1) | **Sin especificar ningún motor** | **Pendiente** (proveedor de bombeo aún no identificado, no depende de FamTECH) |
| Controladores | PLC/controlador propio de NidoSmart + controlador YB (FamTECH v3) + gateway + sensores DMR | Sensores DMR: 0.8W c/u confirmado. PLC/gateway: consumo propio, no depende de proveedor. **Controlador YB (7″): sigue sin dato** — FamTECH indicó que lo confirmaría por separado. | **Parcial** |
| Comunicaciones | Switch/router Ethernet industrial, equipo Starlink u otro enlace satelital de respaldo | Sin dimensionar | **Pendiente** |
| Alarmas | Smart alarm (FamTECH v3, sonido/luz) + sensores NH₃/CO₂/lux propios de NidoSmart | Consumo bajo, sin dato de placa | **Pendiente** |
| Iluminación básica | Sistema de pasillo FamTECH v4 (14 focos DC48V-7W, 1 controlador de dimming) — ver [Automatización — Iluminación](./08-automatizacion.md#iluminación) | **98W confirmado** (lado DC) | **Resuelto (2026-09-21)** en cuanto a potencia; sigue pendiente si el circuito entra al respaldo de UPS (decisión de diseño, no de datos — la carga es trivial) |

De las 6 cargas críticas declaradas en 9.1, **la ventilación y la iluminación básica ya tienen potencia de equipo confirmada**, y los controladores están parcialmente confirmados (sensores DMR sí, controlador YB no); agua y comunicaciones siguen dependiendo de proveedores aún no identificados. Esto es la limitación central para pasar de esta arquitectura preliminar a un cálculo de carga definitivo.

#### Cargas pendientes (sin potencia de ningún proveedor)

* Motor(es) de la bomba principal y de la bomba de respaldo del sistema hidráulico ([9.2](#92-sistema-hidráulico)) — proveedor aún no identificado.
* ~~Motor de la banda de retiro de gallinaza (FamTECH v1/v2, banda 1.0×1130 mm, ítem III.4) — la cotización no desglosa su potencia.~~ — **Resuelto (2026-10-15):** 0.75 kW, 380V trifásico, motor de inducción, 1.4–1.7 A nominal (ver tabla de "Cargas conocidas" arriba).
* ~~Actuadores eléctricos lineales de las 12 entradas de aire CJ01 y sus 2 controladores de entrada de aire (FamTECH v3, ítems V.4–V.5) — potencia no especificada.~~ — **Resuelto (2026-10-15):** DC 24V, ≈43W pico c/u, 10–15W en reposo (ver tabla arriba).
* ~~Motorreductor + torno de la cortina de blackout ("del mismo tipo ya cotizado por FamTECH para las ventanas de entrada de aire")~~ — **Resuelto, con corrección de supuesto (2026-10-15):** FamTECH aclaró que la única "cortina" en su alcance es la persiana de la ventana de entrada de aire pequeña, **sin motor ni control eléctrico**, y que ese ítem no está en la cotización. No hay, por tanto, un actuador CJ01 que reutilizar para la cortina de blackout propia de NidoSmart — debe sourcearse un motorreductor local independiente (ver [Automatización — Iluminación](./08-automatizacion.md#iluminación)).
* Tira LED complementaria por nivel (condicional — solo si el comisionamiento de iluminación revela déficit de lux en algún nivel, ver [Automatización — Iluminación](./08-automatizacion.md#iluminación); ya no se asume necesaria por defecto tras la cotización de iluminación de FamTECH), sensores de lux (4), sensor de NH₃ y sensor de CO₂ — todos de proveedores locales aún no identificados (ver [Automatización](./08-automatizacion.md), "Proveedores locales a buscar").
* PLC/controlador propio de NidoSmart, gateway, switch/router y equipo de enlace satelital de respaldo (Starlink u otro) — consumo aún no dimensionado, dependiente del hardware específico a elegir.
* ~~Consumo del controlador YB (7″) y de los sensores DMR de temperatura/humedad (FamTECH v3) — no especificado en la cotización.~~ — **Parcialmente resuelto (2026-10-15):** sensores DMR confirmados (0.8W c/u). **El controlador YB (7″) sigue sin dato** — FamTECH dijo que lo confirmaría por separado con su equipo técnico.

#### Tablero

* **Tablero principal (TGBT):** ubicado en el **cuarto técnico**, adosado al exterior de la nave junto al extremo con mayor carga eléctrica (ver [Diseño físico — 7.1.1](./07-diseno-fisico.md#711-layout-funcional-recomendado-dentro-de-la-nave-17×4×42-m), "Cuarto técnico (PLC, UPS, tablero)"). **Pendiente:** confirmar cuál extremo concentra la mayor carga real (Cabecera A: motor de alimentación 0.75 kW; Cabecera B: motor de banda de huevo 0.55 kW + motor de banda de gallinaza sin especificar) una vez que se conozca la orientación final de ventiladores/entradas de aire — el sistema es transversal (ancho de 4 m), por lo que los ventiladores probablemente no se ubiquen en ninguna de las dos cabeceras longitudinales, sino en uno de los muros de 4 m.
* **Subtablero:** para el alcance actual (1 nave, 5 sets) se propone un único subtablero alimentado desde el TGBT, con espacio físico reservado (no solo eléctrico) para los interruptores derivados de una segunda unidad, conforme al principio de dimensionar servicios compartidos con margen para el siguiente módulo ([DEC-010](../governance/registro-de-decisiones.md#dec-010--dimensionamiento-de-servicios-compartidos-para-300-aves-desde-el-módulo-piloto), objetivo actualizado a 1,280 aves) y a la expansión lineal de la misma nave ([DEC-014](../governance/registro-de-decisiones.md#dec-014--expansión-lineal-de-la-nave-con-equipo-de-alimentaciónrecolección-compartido-hasta-el-techo-declarado-por-el-proveedor)).
* **Capacidad del interruptor principal:** no puede fijarse todavía — depende del tipo de servicio eléctrico de CFE disponible en el predio (monofásico/trifásico, voltaje, capacidad contratada), dato aún no solicitado (ver "Información necesaria" abajo).

#### Circuitos

Separación propuesta, siguiendo el listado ya definido en 9.1 y el mapeo de cargas críticas de arriba:

**Circuitos normales (sin respaldo UPS/generador):**
1. Motorreductor del skip-hoist feeder (0.75 kW).
2. Motor de la banda recolectora de huevo (0.55 kW).
3. Motor de la banda de retiro de gallinaza (0.75 kW, 380V trifásico, confirmado 2026-10-15).
4. Tomas de uso general e iluminación de servicio (cuarto técnico, almacén, área de empaque — no dimensionado aún, ver [Diseño físico — 7.2](./07-diseno-fisico.md#72-áreas-generales-del-predio)).

**Circuitos de cargas críticas (con respaldo, ver UPS/Generador abajo):**
5. Ventilación mínima: 2 ventiladores (2.2 kW) + actuadores de entradas de aire.
6. Agua: bomba principal + bomba de respaldo + dosificador automático.
7. Controladores: PLC propio, controlador YB, gateway.
8. Comunicaciones: switch/router, equipo de enlace satelital de respaldo.
9. Alarmas: smart alarm, sensores NH₃/CO₂/lux.
10. Iluminación básica: sistema de pasillo FamTECH (14 focos DC48V-7W + controlador de dimming, 98W) — requiere circuito dedicado a 48V DC desde el driver del controlador, no 120/220V AC directo a las luminarias. **Confirmado (2026-09-22):** el controlador acepta enlace a PLC externo por terminales **0–10V** — esto agrega un conductor de señal analógica de baja tensión entre el PLC/controlador propio de NidoSmart y el controlador de dimming, a tender junto con la canalización de señal/control (ver "Canalizaciones" abajo), no con la de potencia.

Cada motor debe llevar su propio circuito derivado con protección independiente (ver "Protecciones"), consistente con "circuitos separados para cargas críticas" ya establecido en 9.1.

#### UPS

* Cubre, según el listado ya definido en 9.1, **controladores, comunicaciones y sensores** — cargas de baja potencia pero de continuidad crítica (electrónica de control, no motores).
* Los motores de ventilación y bombeo de agua **no son candidatos típicos de UPS** (la corriente de arranque de un motor excede lo que una UPS de este tipo puede entregar de forma económica); su continuidad ante falla de red depende del generador (abajo), no de la UPS. La UPS solo necesita cubrir el "puente" de tiempo entre la falla de red y el arranque/transferencia del generador.
* **Pendiente de decisión de diseño (ya no de datos):** con la potencia de iluminación confirmada (98W, ver "Cargas conocidas"), la pregunta de si el circuito entra al respaldo de UPS es puramente de diseño — la carga es trivial en kVA. En cualquier caso, el controlador de iluminación requiere reloj de tiempo real (RTC) con respaldo de batería local propio, independiente del corte de energía general.
* **No puede dimensionarse en kVA/Ah todavía** — depende de: (a) el consumo real en watts de PLC/gateway/comunicaciones y del controlador YB (únicos renglones de control que siguen sin dato — los actuadores CJ01 y los sensores DMR ya están confirmados, ≈43W pico y 0.8W c/u respectivamente, ambos triviales en kVA), y (b) el tiempo de autonomía objetivo hasta que arranque el generador (no definido).

#### Generador

* Cubre las cargas críticas de mayor potencia durante interrupciones prolongadas: ventilación mínima y bombeo de agua, como mínimo.
* **No puede dimensionarse en kVA todavía.** Faltan, como mínimo: la potencia del/los motor(es) de bomba de agua (sin proveedor identificado), la corriente de arranque real de los 2 ventiladores de 1.1 kW (si operan on/off sin variador, el arranque a través de línea exige varias veces la corriente nominal), y si se decide incluir iluminación y/o el motor de la banda de gallinaza en el respaldo.
* Transferencia automática (ATS) entre red CFE y generador recomendada para no depender de una acción manual durante una falla nocturna (coherente con la operación local autónoma del PLC, [DEC-007](../governance/registro-de-decisiones.md#dec-007--uso-de-un-plc-o-controlador-avícola-como-núcleo-del-control-crítico)).
* Tipo de combustible (diésel es lo más común para sitios rurales en México con suministro confiable) — sin decidir; depende de la disponibilidad de suministro/almacenamiento en el predio de San Francisco Acatepec (pendiente de verificar).

#### Puesta a tierra

* Sistema de tierra física (electrodo/varilla de cobre) con resistencia objetivo ≤25 Ω (mínimo normativo) o ≤10 Ω (buena práctica), a confirmar contra un estudio de resistividad del terreno — **no realizado todavía**.
* Red de tierra que interconecte: tablero principal, subtablero, PLC/gateway, controlador YB, carcasas de motores, y estructura metálica de la jaula tipo H (bonding) — relevante porque la jaula es una estructura metálica continua de 17 m dentro de la nave.
* Protección contra descargas atmosféricas (pararrayos): el sitio (San Francisco Acatepec, altiplano poblano) tiene temporada de lluvias con granizadas ya documentada en [Diseño físico — Condiciones climáticas del sitio](./07-diseno-fisico.md#condiciones-climáticas-del-sitio); la exposición a tormentas eléctricas de temporada no se ha verificado con dato de sitio o estación meteorológica — pendiente.

#### Protecciones

* Interruptor termomagnético general en el tablero principal, dimensionado según la capacidad de servicio de CFE (pendiente de confirmar, ver abajo).
* Interruptor derivado independiente por circuito (uno por motor, uno por grupo de cargas críticas de electrónica de control) — ver "Circuitos" arriba.
* Protección de sobrecorriente por motor (relevador térmico o guardamotor), ya prevista en el listado general de 9.1 — su calibre depende de la corriente nominal de cada motor, dato que falta para los motores de bomba de agua y de banda de gallinaza.
* Protección diferencial (falla a tierra) en los circuitos de agua/bombeo, por el riesgo de humedad en esa zona.
* Supresor de transitorios/surge protector — ya incluido de fábrica en el tablero de control ambiental cotizado por FamTECH v3 (ítem V.3 "Surge protector, installed in control box"); debe extenderse al tablero principal si éste queda fuera del alcance de ese tablero de control.
* Paro de emergencia, ya previsto en el listado general de 9.1 — pendiente definir cuántos puntos de paro y en qué ubicaciones (mínimo una por cabecera, dado el layout de dos extremos con equipo motriz, ver [7.1.1](./07-diseno-fisico.md#711-layout-funcional-recomendado-dentro-de-la-nave-17×4×42-m)).

#### Canalizaciones

* Separación física entre canalización de potencia (motores, tablero, iluminación) y canalización de señal/control (Ethernet industrial, sensores, MQTT/Modbus), consistente con la red de control separada ya definida en [9.3](#93-comunicaciones).
* Trayectoria troncal a lo largo de los 17 m de la nave, conectando el cuarto técnico con ambas cabeceras (motor de alimentación en un extremo, motor de banda de huevo/gallinaza en el otro) y con los ventiladores/entradas de aire en los muros de 4 m — la trayectoria exacta depende de la orientación final de la ventilación transversal, aún no confirmada (ver "Tablero" arriba).
* Registros de paso en cada cabecera, donde se concentra el equipo motriz.
* Tipo de canalización (conduit metálico vs. PVC) según exposición: intemperie en el tramo cuarto técnico → nave, interior en el resto — sin definir hasta que se confirme el tipo estructural de la nave ([Ficha técnica — pendiente #1](../investment-project/05-ficha-tecnica-nave.md#estado-de-la-ficha-técnica)).

#### Información necesaria para el cálculo definitivo

Antes de poder calcular la carga eléctrica total, dimensionar el servicio de CFE, la UPS, el generador y las protecciones, se requiere, en orden de bloqueo (cada punto depende del anterior o es prerrequisito de todo lo demás):

1. **Tipo de servicio eléctrico de CFE disponible en el predio** (San Francisco Acatepec): monofásico o trifásico, voltaje, capacidad contratada/disponible en kVA. Sin este dato no puede confirmarse si los motores trifásicos de 380V de la cotización FamTECH son viables sin transformador, ni si aplica el sobrecosto de "motores especiales" ya advertido en la cotización (punto 5, "Electricity situation") — sigue siendo información que debe levantar NidoSmart en el predio, no FamTECH.
2. Potencia, voltaje y tipo (trifásico/monofásico) del motor de la bomba principal y de la bomba de respaldo del sistema hidráulico — sin proveedor identificado todavía.
3. ~~Potencia del motor de la banda de retiro de gallinaza~~ — **Resuelto (2026-10-15):** 0.75 kW, 380V trifásico.
4. Consumo (W) de PLC/gateway propio, switch/router y equipo de enlace satelital — pendiente, depende del hardware a elegir, no de FamTECH. **Parcialmente resuelto del lado FamTECH:** sensores DMR (0.8W c/u) confirmados; controlador YB sigue sin dato.
5. Consumo real del lado AC del driver del controlador de dimming de iluminación (98W es el consumo DC nominal de los focos, no el consumo de red) — sigue sin dato. **Resuelto para los actuadores de entradas de aire (2026-10-15):** ≈43W pico c/u, DC 24V. **Resuelto para la cortina de blackout:** no es un ítem de FamTECH, se sourcea localmente (ver arriba).
6. ~~Corriente de arranque (LRA) de los 2 ventiladores de 1.1 kW~~ — **Resuelto (2026-10-15):** 13–15.4 A (ver tabla de "Cargas conocidas" arriba).
7. Tiempo de autonomía objetivo de la UPS (minutos hasta que el generador tome la carga) — decisión de diseño de NidoSmart, no depende de un proveedor.
8. Alcance final del respaldo de iluminación (si entra o no a UPS/generador) — decisión de diseño, ya no bloqueada por falta de dato de potencia (ver [Automatización](./08-automatizacion.md#iluminación)).

#### Lista de datos eléctricos que debe proporcionar FamTECH

1. ~~Potencia (kW/HP), voltaje y tipo de motor (trifásico/monofásico) del motor de la banda de retiro de gallinaza (ítem III.2/III.4 de la cotización).~~ — **Resuelto (2026-10-15):** 0.75 kW, 380V trifásico, motor de inducción, 1.4–1.7 A.
2. ~~Corriente nominal (A) y corriente de arranque (rotor bloqueado/LRA) de cada motor cotizado.~~ — **Resuelto (2026-10-15):** ver tabla de "Cargas conocidas" arriba (feeder 1.5A/LRA 9–10.5A, banda de huevo 1.3A/LRA 7.8–9.1A, ventiladores 2.2A/LRA 13–15.4A c/u, banda de gallinaza 1.5A/LRA 9–10.5A).
3. Confirmación por escrito (no solo por correo informal) de que todos los motores son compatibles con la red eléctrica mexicana de 60 Hz sin costo adicional, y qué motores específicos activarían el "extra cost of special motors" mencionado en el punto 5 de la cotización si el servicio del predio no es trifásico 380V/50Hz o monofásico 220V/50Hz. **Sigue abierto** — esta pregunta se retiró del Lote 3 realmente enviado (2026-10-15); queda la confirmación informal del 2026-07-21 ("no extra cost"), sin cubrir por escrito los equipos agregados después (ver [registro de cotizaciones](../../evidence/quotations/README.md#nuevos-pendientes-eléctricos-2026-09-18)).
4. ~~Especificación eléctrica (voltaje, corriente, tipo de conexión) de los 2 actuadores lineales eléctricos de las entradas de aire CJ01 y de sus 2 controladores de entrada de aire.~~ — **Resuelto (2026-10-15):** DC 24V, 1.8A máx a plena carga, ≈43W pico, 0.4–0.6A (10–15W) en reposo, ciclo corto.
5. Consumo eléctrico (W) del controlador YB (7″) y de los sensores DMR de temperatura/humedad. **Parcialmente resuelto (2026-10-15):** sensores DMR 0.8W c/u confirmado; **controlador YB sigue sin dato**, FamTECH lo confirmará por separado.
6. Curva de desempeño real de los 2 ventiladores de 50″/1.1 kW (cfm a 0″, 0.05″ y 0.10″ de columna de agua) — **parcialmente resuelto (2026-10-13):** solo el punto "at free air" (43,170 m³/h ≈25,404 CFM), ver [Automatización — Control ambiental](./08-automatizacion.md#control-ambiental); sigue sin el resto de la curva.
7. ~~Si el motorreductor + torno de la cortina de blackout es el mismo actuador CJ01 ya cotizado para las entradas de aire, o una unidad eléctrica aparte.~~ — **Resuelto, con corrección de supuesto (2026-10-15):** no existe tal actuador en el alcance de FamTECH; la "cortina" a la que se refirieron es la persiana manual del CJ01, sin motor. El motorreductor de la cortina de blackout de NidoSmart debe sourcearse localmente.
8. Si existe un diagrama unifilar o ficha eléctrica de referencia del fabricante para una instalación tipo de 5 sets/640 aves. **Diferido (2026-10-15):** FamTECH solo emite los planos eléctricos detallados **después de recibido el anticipo** — no disponible en esta etapa de diseño.
9. ~~Tensión y corriente de entrada AC del controlador de dimming del sistema de iluminación.~~ — sigue sin resolver explícitamente; FamTECH respondió la pregunta de iluminación confirmando el conteo de focos (ver [Automatización — Iluminación](./08-automatizacion.md#iluminación)) pero no dio el dato de consumo AC del controlador — de baja prioridad dado que la carga DC (98W) es trivial frente a los motores.

## 9.2 Sistema hidráulico

Se deberá instalar:

* Tanque pulmón.
* Bomba principal.
* Bomba o mecanismo de respaldo.
* Dos fuentes de agua independientes cuando el predio lo permita (p. ej. pozo + red municipal, o dos pozos) — la redundancia de bomba sobre una sola fuente no cubre el caso de falla de la fuente misma.
* Manifold con salida independiente para cada módulo.
* Medidor por módulo.
* Filtros, instalados antes de la línea de bebederos para excluir partículas.
* Reguladores de presión, con línea de bebederos nivelada para evitar bloqueos de aire.
* Válvulas de aislamiento.
* Puntos de muestreo.
* Drenajes y purgas.
* Sensor de presión.

**Dimensionamiento de referencia (revisión septiembre 2026, cálculo propio a partir de Bell & Weaver, cap. 22, tablas 22-3/22-4 — Universidad de California, 1997, 167 parvadas):** el consumo de agua de gallinas ponedoras en el rango de temperatura interior esperado del sitio (19.7–28°C) es de **18.7–21.4 L/100 aves/día**, equivalente a **≈120–140 L/día para las 640 aves** de la unidad actual.

**Redimensionado con margen para la segunda unidad (2026-09-23):** consistente con el mismo principio ya aplicado en el subtablero eléctrico ([9.1.1](#911-arquitectura-eléctrica-preliminar-revisión-septiembre-2026), que reserva espacio para 1,280 aves conforme a [DEC-010](../governance/registro-de-decisiones.md#dec-010--dimensionamiento-de-servicios-compartidos-para-300-aves-desde-el-módulo-piloto)), el tanque pulmón se dimensiona ahora para 1,280 aves, no solo para 640: **≈239–274 L/día** a 1,280 aves. Con al menos 2 días de reserva en sitio (práctica de la industria), el mínimo es **≈478–548 L**; con margen de limpieza y redundancia, el piso de diseño se actualiza a **≥1,000 L útiles** (antes ≥500 L, dimensionado solo para la unidad actual). El costo incremental de un tanque más grande es bajo frente al costo de sustituirlo o agregar un segundo tanque cuando se construya la segunda unidad. Esta cifra sigue siendo una estimación propia, no una cotización, y debe ajustarse cuando se confirme el ratio real de níples por ave con el proveedor.

**Parámetros de calidad de agua a verificar (revisión julio 2026; reconciliado septiembre 2026):** antes de construir, el agua del predio (pozo o red municipal) debe analizarse. Existen dos referencias con valores distintos, que deben citarse ambas:

* **NOM-127-SSA1-1994** (piso regulatorio oficial, usada por el Manual de Buenas Prácticas Pecuarias en la Producción de Huevo para Plato, `knowledge-base/regulations/buenas-practicas-huevo.pdf`, anexo): ausencia de coliformes totales y de E. coli/coliformes fecales; dureza total máxima 500 ppm (como CaCO₃); hierro máximo 0.3 ppm; nitratos máximo 10 ppm (como N); sodio máximo 200 ppm.
* **Bell & Weaver, capítulo 22** (objetivo de desempeño productivo, más estricto que el piso legal en varios parámetros): pH 6.5–8.0 (ideal 7.0–7.2), dureza máxima 100 ppm, hierro y manganeso máximo 0.3 ppm cada uno, nitratos máximo 20 ppm, sodio máximo 20 ppm, y **0 UFC/mL de bacterias coliformes** (cualquier presencia indica contaminación fecal y riesgo sanitario).

Las dos fuentes coinciden en hierro y en exigir ausencia de coliformes, pero difieren de forma importante en dureza (100 vs. 500 ppm), sodio (20 vs. 200 ppm) y en la base de medición de nitratos (NOM-127 mide como N). NOM-127 es el requisito legal aplicable; los valores de Bell & Weaver son un objetivo de calidad productiva (dureza y sodio afectan la incrustación de los níples y el desempeño de las aves, no solo la inocuidad), y se adoptan como meta de diseño cuando sea alcanzable, sin sustituir el cumplimiento de NOM-127. Pendiente: realizar un análisis de agua del predio y definir tratamiento si no cumple estos parámetros.

**Especificación del sistema de bebederos — resuelto por FamTECH (2026-10-13):**

* **Línea de bebederos:** tubería cuadrada de PVC, **22 × 22 mm**.
* **Presión de suministro a la caseta:** **0.25 MPa**.
* **Presión de operación recomendada por edad del ave** (ficha de FamTECH, en terminología de pollo de engorda — adaptar a las etapas de recría/postura de la ponedora, no copiar literalmente las edades): 1–7 días: 8–12 cm columna de agua; 8–14 días: 12–18 cm; 15–28 días: 18–25 cm; 29–42 días: 25–32 cm (máx. ~35 cm). Para la etapa de postura (ave adulta), usar el extremo alto de este rango como referencia de partida hasta tener una recomendación específica para ponedora.

Esto cierra el pendiente de selección precisa del regulador de presión (antes sin dato del fabricante de níples de FamTECH). Ver [registro de cotizaciones](../../evidence/quotations/README.md) y [correspondencia](../../evidence/correspondence/2026-10-13_FamTECH_email_respuesta-lote2-ventilacion-agua-gallinaza.rtfd/).

**Limpieza de la banda de gallinaza — no es una fuente de aguas residuales continua (resuelto 2026-10-13):** FamTECH confirmó que la limpieza normal de la banda no usa agua; el agua solo se usa para lavar el equipo **una vez por ciclo de parvada** (evento puntual, no continuo). No se agrega al dimensionamiento del tanque pulmón ni de la bomba (demanda diaria), pero sí debe considerarse como un evento de descarga puntual al diseñar el drenaje sanitario (ver [Diseño físico — 7.2.2](./07-diseno-fisico.md#722-drenaje-y-manejo-de-gallinaza-revisión-septiembre-2026)).

## 9.3 Comunicaciones

La arquitectura recomendada es:

* Ethernet industrial como medio principal.
* Wi-Fi sólo para dispositivos no críticos.
* MQTT para telemetría.
* Modbus TCP o RTU para equipos industriales.
* Red separada para control.
* Red separada para administración e internet.
* VPN para acceso remoto.
* Grabación local de cámaras.
* Red de control con operación local autónoma durante fallas de internet (agua, ventilación, alarmas).

### 9.3.1 Conectividad a internet como requisito permanente

La granja generará datos de forma continua para su análisis y operación asistida por Hermes Agent y, en etapas posteriores, por Paperclip. Por ello, la conectividad a internet deja de ser un elemento opcional y se convierte en un requisito permanente de la capa de datos e inteligencia:

* Enlace primario de banda ancha fija (fibra, cable o equivalente disponible en el predio).
* Enlace satelital de respaldo, como **Starlink u otra tecnología equivalente**, para garantizar continuidad cuando falle el enlace primario.
* En módulos o ubicaciones futuras instaladas en zonas remotas sin cobertura de banda ancha fija, Starlink u otra tecnología satelital podrá utilizarse como enlace principal.
* Monitoreo del estado del enlace de internet como una variable operativa más, con alerta cuando se pierda conectividad.
* Buffer local de datos en el gateway y la base de datos local durante interrupciones de internet, para sincronizar la información con Hermes Agent, Paperclip y los paneles remotos en cuanto se restablezca la conexión.

Esta dependencia de internet aplica a la capa de datos, análisis, IA y monitoreo remoto. **No aplica al control crítico**, que debe seguir funcionando de forma local y autónoma a través del PLC, conforme al principio establecido en [Arquitectura tecnológica — Principio fundamental](./10-arquitectura-tecnologica.md#101-principio-fundamental).

---

## Navegación

- [Índice general](./README.md)
- [Documento anterior: Sistema de automatización](./08-automatizacion.md)
- [Documento siguiente: Arquitectura tecnológica](./10-arquitectura-tecnologica.md)
