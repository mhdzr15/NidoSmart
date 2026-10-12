---
title: "Arquitectura eléctrica, hidráulica y de comunicaciones"
project: "NidoSmart"
document_type: "business-plan"
status: "draft"
version: "1.5"
last_updated: "2026-10-12"
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
| Motorreductor del skip-hoist feeder (alimentación) | **0.75 kW** | 380V trifásico o 220V monofásico (catálogo); compatible con red mexicana 60 Hz sin costo adicional (confirmado por correo, no reflejado aún por escrito en la cotización — ver [registro de cotizaciones](../../evidence/quotations/README.md#especificaciones-técnicas-base-v1v2)) | FamTECH v1/v2, ítem I.3 "Drive unit" | Normal (no crítico) |
| Motor de la banda recolectora de huevo | **0.55 kW** (motor Wanxin) | Igual que arriba, sin confirmar fase específica | FamTECH v1/v2, ítem IV.4 "drive unit" | Normal (no crítico) |
| Ventiladores/extractores (ventilación transversal) | **1.1 kW cada uno × 2 = 2.2 kW** ("50″ fan, domestic special power") | Sin especificar en la cotización | FamTECH v3, ítem V.1 "Fan" | **Crítico** (ventilación mínima) |
| Bombas sumergibles del sistema de cooling pad | 0.55 kW cada una × 2 | Sin especificar | FamTECH v3, ítem V.7 "Submersible pump" | **No aplica** — cooling pads descartados para este sitio (ver [Automatización — Control ambiental](./08-automatizacion.md#control-ambiental), "Cooling pads — no se justifican") |
| Sistema de iluminación de pasillo (14 focos DC48V-7W-3000K regulables, 1 controlador de dimming) | **14 × 7W = 98W** en el lado DC48V; consumo real del lado de red (AC) depende de la eficiencia del driver del controlador de dimming, **no especificada**. **Hipótesis de trabajo (2026-10-12, ver [Automatización — Iluminación](./08-automatizacion.md#iluminación)):** el arreglo cotizado probablemente cubre solo una cara del bloque "double-sided" — si se confirma que hace falta duplicarlo (28 focos), la carga DC sube a ≈196W, sigue siendo trivial frente a los motores (no cambia el orden de magnitud del cálculo de abajo). | DC48V (requiere driver/fuente AC→DC48V, presumiblemente integrado en el controlador de dimming) | FamTECH v4 (2026-09-21), ítem V "Lighting system" — ver [Automatización — Iluminación](./08-automatizacion.md#iluminación) | **Crítico** (iluminación básica) |

**Suma de potencia nominal conocida y necesaria para el alcance actual (excluye cooling pads, ya descartados): ≈3.6 kW** (0.75 + 0.55 + 2.2 + 0.098 kW). Esta cifra es la suma de placas de motor/equipo, **no** una demanda máxima calculada (no incluye factores de simultaneidad, arranque ni las cargas aún sin potencia — ver "Cargas pendientes" abajo); no debe usarse todavía para dimensionar el servicio de CFE, el generador ni el calibre de conductores. La iluminación (98W) es una carga eléctricamente trivial frente a los motores — no cambia el orden de magnitud del cálculo, pero sí introduce un requisito de diseño nuevo: un circuito a 48V DC (no 120/220V AC directo) para las luminarias, alimentado desde el controlador de dimming.

**Nota sobre continuidad del paquete de control ambiental:** el presupuesto consolidado ([sección 6](../investment-project/07-presupuesto-consolidado-inversion-inicial.md#6-ventilación-y-control-ambiental)) marca la cotización v3 como "Cotizado, en pausa" porque la decisión de 2026-07-22 pausó el paquete completo. Sin embargo, [Automatización — Control ambiental](./08-automatizacion.md#control-ambiental) ya aclaró que **los ventiladores, entradas de aire y controlador sí son necesarios** (la ventilación mínima no es opcional, [DEC-006](../governance/registro-de-decisiones.md#dec-006--automatización-intensiva-de-al-menos-90-de-las-tareas-repetitivas)) — lo que está descartado son específicamente los cooling pads. Esta arquitectura eléctrica asume que los 2 ventiladores de 1.1 kW y el sistema de entradas de aire motorizadas sí forman parte de la carga real de la nave, aunque su partida presupuestal siga etiquetada "en pausa".

**Arranque de motores (dato relevante para protecciones y generador):** el pendiente ya abierto en automatización ("Si el controlador YB permite programar ventilación escalonada... o solo operación on/off") implica que, si la respuesta es on/off, los 2 ventiladores arrancan a través de línea (sin variador), generando corriente de arranque varias veces la nominal — relevante para el dimensionamiento del generador y de las protecciones (ver abajo). Esto no se puede calcular sin la corriente de arranque real del motor (dato pendiente de FamTECH).

#### Cargas críticas — mapeo a equipo real

| Carga crítica (§9.1) | Equipo que la cubre | Potencia | Estado |
|---|---|---|---|
| Ventilación mínima | 2 ventiladores 1.1 kW + actuadores de las 12 entradas de aire CJ01 (2 "Electric linear actuator") | 2.2 kW + actuadores sin especificar | Parcial — falta potencia de actuadores |
| Agua | Bomba principal + bomba de respaldo ([9.2](#92-sistema-hidráulico)) + bomba dosificadora automática (FamTECH v1/v2, ítem II.1) | **Sin especificar ningún motor** | **Pendiente** |
| Controladores | PLC/controlador propio de NidoSmart + controlador YB (FamTECH v3) + gateway | Consumo de electrónica de control, típicamente bajo, sin dato de placa | **Pendiente** |
| Comunicaciones | Switch/router Ethernet industrial, equipo Starlink u otro enlace satelital de respaldo | Sin dimensionar | **Pendiente** |
| Alarmas | Smart alarm (FamTECH v3, sonido/luz) + sensores NH₃/CO₂/lux propios de NidoSmart | Consumo bajo, sin dato de placa | **Pendiente** |
| Iluminación básica | Sistema de pasillo FamTECH v4 (14 focos DC48V-7W, 1 controlador de dimming) — ver [Automatización — Iluminación](./08-automatizacion.md#iluminación) | **98W confirmado** (lado DC) | **Resuelto (2026-09-21)** en cuanto a potencia; sigue pendiente si el circuito entra al respaldo de UPS (decisión de diseño, no de datos — la carga es trivial) |

De las 6 cargas críticas declaradas en 9.1, **la ventilación y la iluminación básica ya tienen potencia de equipo confirmada** (fans e iluminación); las 4 restantes (agua, controladores, comunicaciones, alarmas) dependen de datos aún no proporcionados por ningún proveedor. Esto es la limitación central para pasar de esta arquitectura preliminar a un cálculo de carga definitivo.

#### Cargas pendientes (sin potencia de ningún proveedor)

* Motor(es) de la bomba principal y de la bomba de respaldo del sistema hidráulico ([9.2](#92-sistema-hidráulico)) — proveedor aún no identificado.
* Motor de la banda de retiro de gallinaza (FamTECH v1/v2, banda 1.0×1130 mm, ítem III.4) — la cotización no desglosa su potencia; podría estar incluida sin especificar en "Backend components and driver system" (ítem III.2, $1,880 USD), pero esto no está confirmado por el proveedor.
* Actuadores eléctricos lineales de las 12 entradas de aire CJ01 y sus 2 controladores de entrada de aire (FamTECH v3, ítems V.4–V.5) — potencia no especificada.
* Motorreductor + torno de la cortina de blackout ("del mismo tipo ya cotizado por FamTECH para las ventanas de entrada de aire", ver [Automatización — Iluminación](./08-automatizacion.md#iluminación)) — sin confirmar si es el mismo actuador CJ01 o una unidad aparte.
* Tira LED complementaria por nivel (condicional — solo si el comisionamiento de iluminación revela déficit de lux en algún nivel, ver [Automatización — Iluminación](./08-automatizacion.md#iluminación); ya no se asume necesaria por defecto tras la cotización de iluminación de FamTECH), sensores de lux (4), sensor de NH₃ y sensor de CO₂ — todos de proveedores locales aún no identificados (ver [Automatización](./08-automatizacion.md), "Proveedores locales a buscar").
* PLC/controlador propio de NidoSmart, gateway, switch/router y equipo de enlace satelital de respaldo (Starlink u otro) — consumo aún no dimensionado, dependiente del hardware específico a elegir.
* Consumo del controlador YB (7″) y de los sensores DMR de temperatura/humedad (FamTECH v3) — no especificado en la cotización.

#### Tablero

* **Tablero principal (TGBT):** ubicado en el **cuarto técnico**, adosado al exterior de la nave junto al extremo con mayor carga eléctrica (ver [Diseño físico — 7.1.1](./07-diseno-fisico.md#711-layout-funcional-recomendado-dentro-de-la-nave-17×4×42-m), "Cuarto técnico (PLC, UPS, tablero)"). **Pendiente:** confirmar cuál extremo concentra la mayor carga real (Cabecera A: motor de alimentación 0.75 kW; Cabecera B: motor de banda de huevo 0.55 kW + motor de banda de gallinaza sin especificar) una vez que se conozca la orientación final de ventiladores/entradas de aire — el sistema es transversal (ancho de 4 m), por lo que los ventiladores probablemente no se ubiquen en ninguna de las dos cabeceras longitudinales, sino en uno de los muros de 4 m.
* **Subtablero:** para el alcance actual (1 nave, 5 sets) se propone un único subtablero alimentado desde el TGBT, con espacio físico reservado (no solo eléctrico) para los interruptores derivados de una segunda unidad, conforme al principio de dimensionar servicios compartidos con margen para el siguiente módulo ([DEC-010](../governance/registro-de-decisiones.md#dec-010--dimensionamiento-de-servicios-compartidos-para-300-aves-desde-el-módulo-piloto), objetivo actualizado a 1,280 aves) y a la expansión lineal de la misma nave ([DEC-014](../governance/registro-de-decisiones.md#dec-014--expansión-lineal-de-la-nave-con-equipo-de-alimentaciónrecolección-compartido-hasta-el-techo-declarado-por-el-proveedor)).
* **Capacidad del interruptor principal:** no puede fijarse todavía — depende del tipo de servicio eléctrico de CFE disponible en el predio (monofásico/trifásico, voltaje, capacidad contratada), dato aún no solicitado (ver "Información necesaria" abajo).

#### Circuitos

Separación propuesta, siguiendo el listado ya definido en 9.1 y el mapeo de cargas críticas de arriba:

**Circuitos normales (sin respaldo UPS/generador):**
1. Motorreductor del skip-hoist feeder (0.75 kW).
2. Motor de la banda recolectora de huevo (0.55 kW).
3. Motor de la banda de retiro de gallinaza (potencia pendiente).
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
* **No puede dimensionarse en kVA/Ah todavía** — depende de: (a) el consumo real en watts de PLC/gateway/controlador YB/sensores/comunicaciones (ninguno especificado hoy), y (b) el tiempo de autonomía objetivo hasta que arranque el generador (no definido).

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

1. **Tipo de servicio eléctrico de CFE disponible en el predio** (San Francisco Acatepec): monofásico o trifásico, voltaje, capacidad contratada/disponible en kVA. Sin este dato no puede confirmarse si los motores trifásicos de 380V de la cotización FamTECH son viables sin transformador, ni si aplica el sobrecosto de "motores especiales" ya advertido en la cotización (punto 5, "Electricity situation").
2. Potencia, voltaje y tipo (trifásico/monofásico) del motor de la bomba principal y de la bomba de respaldo del sistema hidráulico — sin proveedor identificado todavía.
3. Potencia del motor de la banda de retiro de gallinaza — confirmar con FamTECH (ver lista de datos a solicitar abajo).
4. Consumo (W) de PLC/gateway propio, controlador YB, sensores (NH₃, CO₂, lux, DMR), switch/router y equipo de enlace satelital.
5. Consumo real del lado AC del driver del controlador de dimming de iluminación (98W es el consumo DC nominal de los focos, no el consumo de red) y de los actuadores de entradas de aire/cortina de blackout.
6. Corriente de arranque (LRA) de los 2 ventiladores de 1.1 kW, para dimensionar protecciones y generador.
7. Tiempo de autonomía objetivo de la UPS (minutos hasta que el generador tome la carga) — decisión de diseño de NidoSmart, no depende de un proveedor.
8. Alcance final del respaldo de iluminación (si entra o no a UPS/generador) — decisión de diseño, ya no bloqueada por falta de dato de potencia (ver [Automatización](./08-automatizacion.md#iluminación)).

#### Lista de datos eléctricos que debe proporcionar FamTECH

1. Potencia (kW/HP), voltaje y tipo de motor (trifásico/monofásico) del motor de la banda de retiro de gallinaza (ítem III.2/III.4 de la cotización) — no especificado en ninguna versión.
2. Corriente nominal (A) y corriente de arranque (rotor bloqueado/LRA) de cada motor cotizado: motorreductor del feeder (0.75 kW), motor de la banda de huevo (0.55 kW), ventiladores (1.1 kW c/u) — necesaria para calibre de conductor, protecciones y dimensionamiento del generador.
3. Confirmación por escrito (no solo por correo informal) de que todos los motores son compatibles con la red eléctrica mexicana de 60 Hz sin costo adicional, y qué motores específicos activarían el "extra cost of special motors" mencionado en el punto 5 de la cotización si el servicio del predio no es trifásico 380V/50Hz o monofásico 220V/50Hz.
4. Especificación eléctrica (voltaje, corriente, tipo de conexión) de los 2 actuadores lineales eléctricos de las entradas de aire CJ01 y de sus 2 controladores de entrada de aire (ítems V.4–V.5 de la cotización v3).
5. Consumo eléctrico (W) del controlador YB (7″) y de los sensores DMR de temperatura/humedad (ítems V.1–V.3 del bloque "Electrical Control System" de la cotización v3).
6. Curva de desempeño real de los 2 ventiladores de 50″/1.1 kW (cfm a 0″, 0.05″ y 0.10″ de columna de agua) — pendiente ya listado en [Automatización — Control ambiental](./08-automatizacion.md#control-ambiental), relevante también aquí porque cambia si se sustituye el modelo cotizado.
7. Si el motorreductor + torno de la cortina de blackout es el mismo actuador CJ01 ya cotizado para las entradas de aire, o una unidad eléctrica aparte con su propia especificación.
8. Si existe un diagrama unifilar o ficha eléctrica de referencia del fabricante para una instalación tipo de 5 sets/640 aves, para contrastarlo contra el diseño propio de NidoSmart.
9. **Nuevo (2026-09-21):** tensión y corriente de entrada AC del controlador de dimming del sistema de iluminación (ítem V.3 de la cotización v4) — los 98W conocidos son el consumo nominal DC de los 14 focos, no el consumo real del lado de red que debe dimensionarse en el tablero.

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
