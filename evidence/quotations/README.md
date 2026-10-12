# Registro de cotizaciones — Sistema de jaula tipo H

Seguimiento de cotizaciones recibidas para el sistema de jaula automatizada tipo H (piloto de 640 aves). Proveedor único hasta ahora: **FamTECH / ABC Machinery / Anyang Best Complete Machinery Engineering Co., Ltd** (contacto: bh@gcmec.com / bh@famtechpoultry.com).

## Historial de versiones

| Archivo | Fecha | No. cotización | Alcance | Incoterm | Precio total (USD) |
|---|---|---|---|---|---|
| `2026-07-21_FamTECH_v1_Jaula-Automatizacion_CIF-Puebla_USD17747.pdf` | 2026-07-21 | BS04H072126 | Jaula + alimentación + bebederos + recolección de huevo (5 sets, 640 aves) | CIF "Puebla port" (error: Puebla no tiene puerto, aclarado en v2) | $17,747 |
| `2026-07-21_FamTECH_v2_Jaula-Automatizacion_DAP-Puebla_USD17747.pdf` | 2026-07-21 | BS04H072226 | Igual que v1 (solo se corrigió el término de precio) | DAP Puebla (no incluye aranceles ni IVA) | $17,747 |
| `2026-07-22_FamTECH_v3_Jaula-Automatizacion-ControlAmbiental_DAP-Puebla_USD24095.pdf` | 2026-07-22 | BS04H072226 | v2 + equipo de control ambiental (ventiladores, cooling pads, ventanas de entrada de aire, controlador, sensores temp/humedad) | DAP Puebla (no incluye aranceles ni IVA) | $24,095 |
| `2026-09-21_FamTECH_v4_Jaula-Automatizacion-Iluminacion_DDU-SanFranciscoAcatepec_USD22644.21.pdf` | 2026-09-21 | BS04H092126 | v1/v2 (jaula + alimentación + bebederos + recolección de huevo) + **sistema de iluminación de pasillo** (nuevo, ver detalle abajo). **No incluye control ambiental** (ese alcance sigue solo en v3, en pausa). | **DDU San Francisco Acatepec, Puebla** — primera cotización con destino final al sitio del proyecto, no solo a la ciudad de Puebla (no incluye aranceles ni IVA de importación) | $22,644.21 |

## Decisión vigente (2026-07-22, base de costo actualizada 2026-09-21)

Se continúa **con el alcance de jaula + automatización + iluminación** (v4, $22,644.21, DDU sitio) — el control ambiental (sensores y actuadores de ventilación/cooling pads) queda en pausa hasta definir el diseño de la nave, aunque ver la nota en [Automatización — Control ambiental](../../docs/business-plan/08-automatizacion.md#control-ambiental) sobre qué partes de ese paquete sí son necesarias.

**⚠️ Vigencia de precios (advertencia de FamTECH, 2026-09-23):** el precio de v4 ($22,644.21 USD) tiene un periodo de validez y es de referencia, no garantizado. FamTECH indicó explícitamente que si el pedido se coloca en 2027 (o más adelante), **actualizarán la cotización antes de la orden de compra**. Todos los montos de este documento y del [presupuesto consolidado](../../docs/investment-project/07-presupuesto-consolidado-inversion-inicial.md) basados en v4 son el **piso de referencia vigente para 2026** — se requiere una cotización actualizada de FamTECH inmediatamente antes de confirmar cualquier compra, sin importar cuánto tiempo haya transcurrido desde esta ronda.

## Pendientes con este proveedor

- ~~Cotización DDP (con aranceles + IVA incluidos) para el alcance de jaula + automatización.~~ — **Parcialmente resuelto (2026-09-21):** v4 cotiza en término **DDU** (Delivered Duty Unpaid) directamente al sitio del proyecto — resuelve el transporte físico hasta San Francisco Acatepec, pero **sigue sin incluir aranceles ni IVA de importación** (ver nota de reconciliación de cifras abajo). Sigue pendiente una cotización DDP completa si se quiere el desglose de aranceles/IVA por parte del proveedor en vez de estimarlo internamente (ver [presupuesto — sección 10](../../docs/investment-project/07-presupuesto-consolidado-inversion-inicial.md#10-importación-y-logística)).
- ~~Confirmar si "grupo de jaula" equivale a un "set" de la cotización~~ — **Resuelto (2026-07-23):** confirmado por escrito, un "grupo de jaula" equivale a un "set" completo de 128 aves (ver hilo de correo [`mail_famtechpoultry.rtfd`](../correspondence/mail_famtechpoultry.rtfd/)).
- El proveedor indicó que el sistema admite "hasta 90 grupos en una nave de 120 m" (≈11,520 aves) compartiendo alimentación y recolección de huevo, agregando sólo jaula y bebederos por grupo adicional. Esa proporción (120 m/90 grupos ≈ 1.33 m/grupo) no coincidía con la de nuestra nave calculada como 17 m/5 sets = 3.4 m/set. **Aclarado (2026-09-28):** la discrepancia era un error de método propio, no una configuración distinta del proveedor — no debe dividirse 17 m entre 5 sets, porque esos 17 m incluyen equipo de cabecera compartido (único por fila). El valor real por set es el cuerpo de jaula (1.2×1.2 m, ya confirmado), muy cercano a la proporción del proveedor. Ver [correspondencia](../correspondence/2026-09-28_FamTECH_email_respuesta-lote1-expansion-layout.rtfd/) y [Modelo modular — 6.2](../../docs/business-plan/06-crecimiento-modular.md#62-escala-recomendada). **Resuelto (2026-10-11):** FamTECH confirmó, ya con su ingeniero civil, que **90 grupos en 120 m es el límite recomendado** (no solo una referencia genérica): "We do not recommend a poultry-house length exceeding 120 m. If a longer length is required, an additional unit should be added accordingly." Es decir, al llegar a ese límite no se agrega una segunda línea de arrastre a la misma nave — se construye una unidad adicional completa. Ver [correspondencia](../correspondence/2026-10-11_FamTECH_email_respuesta-civil-expansion-foundation.rtfd/).
- ~~Confirmar si el precio cotizado incluye instalación en sitio del equipo (jaula, automatización) o si es una partida aparte.~~ — **Resuelto (ya estaba en la cotización del 2026-09-28, no detectado hasta el 2026-10-12):** la sección "6) Installation conditions" de la cotización anotada ([`2026-09-28_FamTECH_v4-anotado_partes-compartidas-vs-repetibles.pdf`](./2026-09-28_FamTECH_v4-anotado_partes-compartidas-vs-repetibles.pdf)) especifica que **la instalación la hace NidoSmart con su propia mano de obra** ("the buyer need arrange several workers"); FamTECH **no instala el equipo**, solo ofrece, de forma opcional ("if necessary"), enviar 2-3 técnicos a guiar/entrenar a los trabajadores de NidoSmart durante 20-30 días, a **USD $100/persona/día** (+USD $50/persona/día extra si el retraso es por falta de preparación de NidoSmart — agua, electricidad o personal no listos), con vuelos redondos, visa, hospedaje y alimentación a cargo de NidoSmart. No es "instalación incluida en el precio" ni "responsabilidad del contratista de obra civil" — es guía técnica opcional y facturable aparte. Ver [presupuesto — sección 11](../../docs/investment-project/07-presupuesto-consolidado-inversion-inicial.md#11-instalación-y-puesta-en-marcha) para el costo estimado.
- ~~Aclarar alcance de entrega ($17,747)~~ — **Resuelto (2026-09-21):** el 3 de agosto de 2026 el proveedor había aclarado que el precio de $17,747 (v1/v2) correspondía a término CIP entregado solo en la ciudad de Puebla, sin el tramo final al sitio. La nueva cotización v4 (2026-09-21) ya cotiza **DDU directo a San Francisco Acatepec** ($22,644.21, ver tabla arriba), cerrando ese vacío. **Nota de reconciliación (no resuelta con precisión):** el salto de v1/v2 a v4 combina tres cosas a la vez — el sistema de iluminación nuevo (+$945.65 EXW, aislable con precisión), y un incremento de "Sea freight & Inland freight" de $6,330 a $10,281 (+$3,951) que mezcla el tramo Puebla→sitio (antes no cotizado) con "Port charges" ahora desglosados aparte — el proveedor no separó cuánto de ese incremento es cada concepto. Ver [presupuesto — sección 10](../../docs/investment-project/07-presupuesto-consolidado-inversion-inicial.md#10-importación-y-logística) para cómo se trata esta ambigüedad en el CAPEX.

## Qué se compra una sola vez por fila vs. qué se repite por set (aclarado 2026-09-28)

FamTECH respondió el Lote 1 de preguntas con dos documentos: el correo [`2026-09-28_FamTECH_email_respuesta-lote1-expansion-layout.rtfd`](../correspondence/2026-09-28_FamTECH_email_respuesta-lote1-expansion-layout.rtfd/) y una copia anotada de la cotización v4 con los ítems que se repiten por set marcados en rojo — [`2026-09-28_FamTECH_v4-anotado_partes-compartidas-vs-repetibles.pdf`](./2026-09-28_FamTECH_v4-anotado_partes-compartidas-vs-repetibles.pdf). Precios idénticos a v4 ($22,644.21 DDU) — es la misma cotización, no una versión nueva de precio.

**Equipo compartido — se compra una sola vez por fila, sin importar si son 5 o 90 sets (ítems marcados en negro en el documento):**

| Sección | Ítem | Precio (USD EXW) |
|---|---|---:|
| I.1 | Skip hoist feeder (máquina alimentadora, hopper + hoist) | 1,498 |
| II.1–4 | Bomba dosificadora, sistema frontal de línea de agua, tubería principal de entrada, conexión de válvula reguladora | 370 + 4 + 92 + 18.4 |
| III.1 | Front-end components | 810 |
| III.2 | Backend components and driver system (huevo/gallinaza) | 1,880 |
| IV.1 | Egg collecting machine main body | 2,650 |
| V.3 | Dimming controller | 679.39 |
| **Total equipo compartido (aprox.)** | | **≈8,002** |

**Equipo consumible — se repite/compra de nuevo por cada set o metro adicional (ítems marcados en rojo):**

| Sección | Ítem | Precio unitario (USD EXW) | Unidad |
|---|---|---:|---|
| I.2 | Traveling square tube | 3.5 | por metro |
| I.3 | Drive unit (reductor, 0.75 kW) | 248 | por set — **verificar visualmente, ver nota abajo** |
| II.5–7 | Cage pressure regulating valve, 12-nipple square tube waterline, hanging cup | 2.3 / 0.8 / 53 | por pieza |
| III.3 | Cage (jaula) | 215 | por set |
| III.4 | Manure collection belt (1.0×1130 mm) | 2.6 | por unidad (81.6 unidades cotizadas para 5 sets) |
| III.5 | Manger (comedero) | 53 | por metro |
| III.6 | NSM100 manure curtain | 11 | por unidad |
| IV.2 | Egg collection belt (PP 92 mm) | 0.5 | por metro |
| IV.3 | Egg collection cards | 0.3 | por pieza |
| IV.4 | Drive unit (huevo) | 529 | por set — **verificar con FamTECH, ver nota abajo** |
| V.1 | Light (bulb) DC48V-7W-3000K | 4.47 | por pieza |
| V.2 | Wire (cable impermeable) | 1.52 | por metro |

**Nota de verificación:** la lectura de qué números aparecen en rojo se hizo visualmente sobre el PDF. Los ítems I.3 (drive unit del feeder) y IV.4 (drive unit de huevo) aparecen marcados en rojo, pero que ambos se repitan por set parece contradecir la explicación escrita de FamTECH sobre compartir una sola cabecera/cola y máquina recolectora por fila. La tabla conserva la clasificación visual del anexo; antes de usarla para presupuestar la segunda unidad, confirmar directamente con FamTECH si ambos drive units son realmente repetibles o si la marca roja tiene otro alcance.

**Uso de este hallazgo:** esta tabla es la base para estimar el CAPEX incremental de la segunda unidad (1,280 aves) y de expansiones posteriores — el costo de equipo compartido (~$8,531 USD) no se repite, mientras que el costo por set adicional (jaula $215 + comedero $53/m + banda de huevo/gallinaza por metro + bebederos + focos) sí. No se ha recalculado todavía el presupuesto de la segunda unidad con este desglose — pendiente para cuando se autorice formalmente esa expansión (ver [criterios de expansión — 6.3](../../docs/business-plan/06-crecimiento-modular.md#63-criterios-para-agregar-un-módulo)).

## Especificaciones técnicas base (v1/v2)

- Nave sugerida: **17m × 4m × 4.2m** — confirmado textualmente en la cotización ("Advised chicken coop size: 17m*4m*4.2m / Total number: 640 birds"), no es una estimación propia.
- 5 sets tipo H, 4 niveles ("four-layer double-sided"), **640 aves totales** — confirmado en la misma línea de la cotización.
- 1 set = 1 "grupo de jaula" = **128 aves** (confirmado por el proveedor por escrito, 2026-07-23).
- Incluye: alimentación automática (skip hoist feeder), bebederos automáticos tipo níple, banda de recolección de huevo (163.2 m de banda, material PP de 92 mm), banda de retiro de gallinaza/estiércol (banda 1.0×1130 mm)
- Motores confirmados por correo (no reflejado aún por escrito en el PDF): compatibles con red eléctrica mexicana 60Hz, sin costo adicional
- Garantía: 13 meses desde envío/entrega
- Tiempo de entrega: ~40 días después del anticipo
- Pago: 30% anticipo, 70% antes de entrega

## Lo que NO especifica todavía el proveedor (pendiente real, no resuelto por este hilo)

- ~~Dimensiones internas por jaula individual (ancho × fondo × alto por nivel)~~ — **Resuelto parcialmente (2026-09-20):** FamTECH confirmó 1.2m × 1.2m por nivel (ancho × fondo); **sigue pendiente la altura por nivel**.
- ~~Espacio lineal de comedero por ave (cm/ave).~~ — **Resuelto (2026-09-28):** 32 aves/jaula, 2 comederos que suman 2.4 m ⇒ ≈7.5 cm/ave — dentro del rango específico de la línea Hy-Line W-80 (7–9 cm/ave en producción), pero en el extremo bajo, sin margen adicional. Ver [Automatización — Alimentación](../../docs/business-plan/08-automatizacion.md#alimentación) y [correspondencia](../correspondence/2026-09-28_FamTECH_email_respuesta-lote1-expansion-layout.rtfd/).
- ~~Relación de aves por níple bebedero.~~ — **Resuelto (2026-09-20):** FamTECH confirmó 32 aves y 4 níples por nivel = 8 aves/níple (extremo superior del rango recomendado, ver [Automatización — Agua](../../docs/business-plan/08-automatizacion.md#agua)).
- ~~Diseño de luminarias para el sistema de 4 niveles~~ — **Resuelto (2026-09-20/21):** FamTECH confirmó luminarias de pasillo, espaciadas aproximadamente 2.5 m, y cotizó el sistema con dos alturas de montaje — **no** hay tira LED integrada por nivel. El sistema de pasillo es la solución base; NidoSmart solo deberá abastecer iluminación complementaria si las mediciones de comisionamiento revelan déficit de lux en algún nivel. Los sensores de lux siguen siendo necesarios para verificarlo. Ver [Automatización — Iluminación](../../docs/business-plan/08-automatizacion.md#iluminación) y el detalle de las dos rondas de respuesta abajo.
- Especificación de aislamiento térmico (valor R o equivalente) para techo y paredes de la nave de 17×4×4.2 m — sigue sin respuesta; incluida en el Lote 4 enviado a FamTECH (ver [borrador de correspondencia](../correspondence/2026-09-27_NidoSmart_borrador-preguntas-famtech.md)).

Estas cinco preguntas fueron redactadas por NidoSmart el 2026-07-25 pero, según el hilo de correo revisado, no llegaron a enviarse al proveedor (quedaron en un correo dirigido a una cuenta propia). Cuatro de las cinco (dimensiones, níples, luminarias, comedero) ya están resueltas — solo queda pendiente el aislamiento térmico.

**Nuevos pendientes de layout (2026-09-16, identificados al resolver las especificaciones de layout de la nave — ver [Diseño físico — 7.1.1](../../docs/business-plan/07-diseno-fisico.md#711-layout-funcional-recomendado-dentro-de-la-nave-17×4×42-m)):**

- ~~Altura libre real requerida por el sistema completo instalado.~~ — **Resuelto (2026-09-28):** 4.2 m es la altura libre interior de la nave, confirmada por escrito por FamTECH; su equipo técnico ya validó el diseño completo contra esa altura. Ver [correspondencia](../correspondence/2026-09-28_FamTECH_email_respuesta-lote1-expansion-layout.rtfd/).
- Footprint longitudinal real de cada uno de los 5 sets — **parcialmente resuelto (2026-09-28):** el cuerpo de jaula (1.2×1.2 m) es el valor que se repite por set, y el espacio de circulación en cada cabecera es de 1 m (confirmado, menos que la recomendación interna de ≥1.5 m). Sigue pendiente el footprint propio del equipo de cabecera ("front-end components" y "backend components and driver system").
- ~~Footprint transversal (profundidad de jaula + pasillo central) del arreglo "double-sided" de 4 niveles.~~ — **Resuelto (2026-10-11):** FamTECH respondió "If only one row is installed, with a walkway on each side, the total width is 4 m" — el arreglo es un bloque de jaula espalda con espalda al centro (línea mecánica compartida: comedero, bebedero, bandas, riel del feeder), con pasillos de circulación humana a los costados — no el pasillo central único que asumía el corte transversal anterior. Corroborado por una confirmación independiente de tres semanas antes, por el hilo de iluminación: "Lights are located in **the aisles**" (plural). Diagrama corregido en [Diseño físico — 7.1.1](../../docs/business-plan/07-diseno-fisico.md#711-layout-funcional-recomendado-dentro-de-la-nave-17×4×42-m).

**Pendientes de iluminación (2026-09-17) — resueltos por FamTECH en dos rondas (2026-09-20 y 2026-09-21):**

- ~~Si la estructura de jaula de nuestro pedido incluye el riel/soporte para tira LED en cada uno de los 4 niveles.~~ — **No.**
- ~~Si la tira LED en sí está incluida en el precio del ítem "cage" (III.3) o es partida aparte.~~ — **No está incluida bajo ningún ítem.**
- ~~Especificación eléctrica del riel/conector.~~ — **Sin objeto**, no existe ese riel en el diseño de FamTECH.

**Ronda 1 (2026-09-20, WhatsApp):** "Lights are located in the aisles, spaced 2.5 meters apart" — el sistema de FamTECH ilumina desde el pasillo, no con tira por nivel. Esto revierte la conclusión previa de este proyecto (basada en documentación pública de *otros* fabricantes de jaula tipo H, no en una confirmación directa de FamTECH) de que la tira LED por nivel ya venía resuelta por el diseño de la jaula.

**Ronda 2 (2026-09-21, WhatsApp + correo [`2026-09-21_FamTECH_email_cotizacion-iluminacion-y-explicacion.rtfd`](../correspondence/2026-09-21_FamTECH_email_cotizacion-iluminacion-y-explicacion.rtfd/)) — respuesta completa del ingeniero de FamTECH y cotización formal:**

1. **Justificación técnica de por qué solo hay luz en el pasillo** (consultada por FamTECH con su propio ingeniero, cita textual del proveedor):
   - Iluminación dentro de la jaula (tira LED) es específica de jaulas "furnished/welfare", no del sistema tipo H de alta densidad que NidoSmart cotizó.
   - Jaula tipo H prioriza densidad/costo sobre bienestar: estructura compacta, poca altura libre, sin espacio para luminaria interna.
   - Riesgos si se instalara dentro de la jaula: picaje de las aves por aburrimiento contra la luminaria, y riesgo de conducción eléctrica si hay fuga de la línea de níples cerca de un componente eléctrico.
   - Instalación en pasillo facilita mantenimiento e inspección.
2. **Diseño de mitigación de la variación top/bottom** (la preocupación por la atenuación de 4–5× entre nivel superior e inferior, documentada en Bell & Weaver, **sí fue considerada por FamTECH**): arreglo de 2 lámparas por punto en un mismo tubo/barra de suspensión ("hanger rod"), espaciados cada ~2.5 m a lo largo del pasillo — Lámpara 1 a **20 cm sobre la red superior** (nivel 1) y Lámpara 2 colgando **1.2–1.5 m por debajo de la red superior** (ajustable, cubriendo los niveles inferiores). Diagrama del proveedor: [`2026-09-21_FamTECH_diagrama-altura-lamparas.jpeg`](./2026-09-21_FamTECH_diagrama-altura-lamparas.jpeg).
3. **Especificación del foco:** **DC48V, 7W, 3000K, regulable (dimming)**.
4. **Cotización formal recibida** (v4, ver tabla de versiones arriba): 14 focos regulables ($62.58), 134 m de cable impermeable ($203.68), 1 controlador de dimming ($679.39) — subtotal **$945.65 USD EXW**, dentro del rango ya estimado en el presupuesto ([sección 7](../../docs/investment-project/07-presupuesto-consolidado-inversion-inicial.md#7-iluminación), $15,000–$35,000 MXN ≈ $811–$1,892 USD) — el estimado previo resultó razonable. 14 focos ÷ 2 por punto = 7 puntos de suspensión, consistente con ~17 m de pasillo a 2.5 m de espaciamiento.

**Pendiente del 2026-09-21 — resuelto (2026-09-22, respuesta final de FamTECH):**

* **Flujo luminoso:** "Luminous flux: 7W × 120LM" = 120 lm/W ⇒ ≈840 lm/foco, ≈11,760 lm totales (14 focos). Detalle y sanity check de intensidad en [Automatización — Iluminación](../../docs/business-plan/08-automatizacion.md#iluminación).
* **Zonificación/canales del controlador:** sí permite zona independiente o enlace a PLC externo, con programación por horario y control individual; integrable a un sistema de control ambiental centralizado.
* **Integración con PLC:** sí, por terminales **0–10V** — el fotoperiodo puede programarse desde el PLC propio de NidoSmart, no depende del panel de fábrica de FamTECH.

**Resuelto (2026-09-23):** el precio del controlador **no cambia** en modo PLC-linked (0–10V) — sigue siendo el mismo $679.39 USD ya cotizado en v4. FamTECH aclaró que solo es necesario que el sistema de control ambiental propio de NidoSmart incorpore esta señal PLC (0–10V), sin costo adicional del lado del controlador de dimming.

(Ver advertencia de vigencia de precios de FamTECH en ["Decisión vigente"](#decisión-vigente-2026-07-22-base-de-costo-actualizada-2026-09-21) arriba — aplica a toda la cotización v4, incluido este controlador.)

(Las luminarias de pasillo, su cableado y el controlador de dimming están incluidos en la cotización v4 de FamTECH. Tragaluces, cortinas de blackout, sensores de lux y cualquier iluminación complementaria condicional son partidas de otros proveedores — la cotización de FamTECH solo cubre el equipo listado línea por línea.)

**Nuevo pendiente — reabierto por la confirmación de layout (2026-10-12, hipótesis de trabajo de confianza alta):** con el arreglo "double-sided" ya confirmado como jaula espalda con espalda con pasillos a los dos lados (ver [Diseño físico — 7.1.1](../../docs/business-plan/07-diseno-fisico.md#711-layout-funcional-recomendado-dentro-de-la-nave-17×4×42-m)), los 14 focos/7 puntos ya cotizados probablemente cubren **una sola cara** del bloque (patrón esperado en sistema tipo H: cada cara tiene su propio frente de alimentación y su propia línea de iluminación) — ver análisis completo y la pregunta concreta a enviarle a FamTECH en [Automatización — Iluminación](../../docs/business-plan/08-automatizacion.md#iluminación). Impacto en presupuesto si se confirma: duplicar focos y cable (≈+$266 USD / ~$4,930 MXN), el controlador probablemente no necesita duplicarse — el nuevo subtotal (~$1,212 USD ≈ $22,420 MXN) sigue dentro del rango ya presupuestado.

**Nuevos pendientes de ventilación y control ambiental (2026-09-16, identificados al definir la estrategia de ventilación — ver [Automatización — Control ambiental](../../docs/business-plan/08-automatizacion.md#control-ambiental)):**

- Curva de desempeño real de los 2 ventiladores de 50"/1.1 kW ya cotizados en v3 (cfm a 0", 0.05" y 0.10" de columna de agua) — necesario para confirmar si cubren el rango calculado de 3,600–10,000 cfm para 640 aves.
- Si el paquete de control ambiental (v3, USD $6,347.6) puede re-cotizarse separando ventiladores + entradas de aire + controlador (de interés) de los cooling pads (no de interés por ahora, ver justificación climática en el documento de automatización).
- Área efectiva de cada una de las 12 entradas de aire CJ01 cotizadas.
- Si el controlador YB (7") permite ventilación escalonada (mínimo invierno → máximo verano) o solo on/off.
- **Cuántos sets adicionales admite la MISMA unidad de arrastre de alimentación y recolección de huevo de nuestro pedido (5 sets, 640 aves) antes de requerir un segundo sistema compartido completo** — **Resuelto (2026-10-11):** FamTECH, ya con su ingeniero civil, confirmó el límite práctico: **90 grupos / 120 m es el máximo recomendado por nave**; más allá de eso no se extiende la misma línea, se agrega una unidad adicional completa. Esto fija también el umbral de migración de ventilación transversal a modo túnel (al acercarse a los 120 m). Ver [correspondencia](../correspondence/2026-10-11_FamTECH_email_respuesta-civil-expansion-foundation.rtfd/).
- ~~Confirmar la extensibilidad de la cimentación/estructura civil declarada por el proveedor — si el diseño de la nave permite ampliarse linealmente por tramos (agregando sets) sin reconstruir cimentación, y cada cuántos sets se requiere un refuerzo estructural o una junta constructiva.~~ — **Resuelto (2026-10-11):** FamTECH confirmó que la expansión por fases es posible; **juntas de expansión cada ≈6 m** (a confirmar el requisito exacto con el ingeniero civil local), y que los cimientos de cada fase deben quedar al mismo nivel entre sí para evitar diferencias de altura entre unidades que afecten la operación. Techo de longitud recomendado: 120 m por nave (ver punto anterior). Ver [correspondencia](../correspondence/2026-10-11_FamTECH_email_respuesta-civil-expansion-foundation.rtfd/).
- ~~El "Skip hoist feeder" (cotización v1/v2, item I.1) especifica textualmente "a travel path of up to 100 meters" — confirmar si aplica al equipo específico de nuestro pedido o es cifra genérica, y qué pasa al llegar a ese límite.~~ — **Resuelto (2026-09-28):** FamTECH confirmó que el límite de 100 m es real y aplica a la máquina de alimentación — si la nave futura se construye a 100 m o menos, la misma máquina sirve; si excede 100 m, se requiere una segunda máquina de alimentación. Ver [correspondencia](../correspondence/2026-09-28_FamTECH_email_respuesta-lote1-expansion-layout.rtfd/).

**Nuevos pendientes de agua y gallinaza (2026-09-18, identificados al definir los requisitos físicos de agua, drenaje y manejo de gallinaza — ver [Diseño físico — 7.2.2](../../docs/business-plan/07-diseno-fisico.md#722-drenaje-y-manejo-de-gallinaza-revisión-septiembre-2026) y [Arquitectura eléctrica/hidráulica — 9.2](../../docs/business-plan/09-arquitectura-electrica-hidraulica-comunicaciones.md#92-sistema-hidráulico)):**

- **Capacidad real de la banda de retiro de gallinaza (kg/ciclo, velocidad)** — la cotización confirma dimensiones (1.0×1130 mm) pero no throughput. **Cifra objetivo calculada (2026-09-23, ver [Automatización — Retiro de gallinaza](../../docs/business-plan/08-automatizacion.md#retiro-de-gallinaza)):** dado que esta banda es equipo compartido y lineal ([DEC-014](../../docs/governance/registro-de-decisiones.md#dec-014--expansión-lineal-de-la-nave-con-equipo-de-alimentaciónrecolección-compartido-hasta-el-techo-declarado-por-el-proveedor)) que no se duplica al agregar sets, se necesita que soporte sin acumulación **≈1,000 kg/día** (meta del plan, ≈5,120 aves) — muy por encima de los 65–125 kg/día de la unidad actual (640 aves). **Parcialmente resuelto (2026-09-28, ampliado 2026-10-11):** FamTECH confirmó que la banda sigue la misma lógica que la alimentación — unidad motriz y cabeceras son equipo compartido (una vez por fila), mientras que los tramos de banda (consumibles) se agregan por sección nueva. Respuesta del 2026-10-11, más explícita: "its current cleaning capacity is matched to your current flock size, and when you add units later, only certain components need to be added" — confirma que la capacidad instalada hoy está dimensionada para 640 aves, no con margen para 1,280. **El throughput real en kg/h sigue sin número** — esto ya no se trata como una pregunta de ingeniería civil pendiente de su ingeniero, sino como un dato de producto que habría que volver a pedir explícitamente si se necesita antes de expandir. Ver [correspondencia](../correspondence/2026-10-11_FamTECH_email_respuesta-civil-expansion-foundation.rtfd/).
- Si la banda de gallinaza requiere agua para su limpieza — posible fuente de agua residual adicional no contemplada en el diseño hidráulico actual.
- Punto y altura de descarga de la banda al contenedor — necesario para diseñar el contenedor cerrado y su protección contra lluvia.
- Presión de operación recomendada por el fabricante de níples que use FamTECH (no identificado en la cotización) — sin esto no puede seleccionarse el regulador de presión con precisión.
- Diámetro y material de tubería recomendado por FamTECH para su línea de bebederos — necesario para la compatibilidad con el manifold de NidoSmart.
- ~~Si la instalación en sitio de la banda de gallinaza está incluida en el precio cotizado o es responsabilidad de la obra civil de NidoSmart.~~ — **Sin objeto (resuelto 2026-10-12):** toda la instalación la hace NidoSmart con su propia mano de obra, con guía técnica opcional de FamTECH (ver pendiente de instalación resuelto arriba) — no aplica la distinción "incluido vs. responsabilidad del contratista", porque no hay un contratista de obra civil distinto instalando el equipo de FamTECH. Sigue abierto, eso sí, si la guía/entrenamiento de FamTECH cubre específicamente el tramo banda → contenedor externo → compostaje, o si ese tramo (al ser la interfaz con la obra civil) queda fuera de su alcance de capacitación.

**Nuevos pendientes eléctricos (2026-09-18, identificados al definir la arquitectura eléctrica preliminar — ver [Arquitectura eléctrica, hidráulica y de comunicaciones — 9.1.1](../../docs/business-plan/09-arquitectura-electrica-hidraulica-comunicaciones.md#911-arquitectura-eléctrica-preliminar-revisión-septiembre-2026)):**

1. Potencia (kW/HP), voltaje y tipo de motor (trifásico/monofásico) del motor de la banda de retiro de gallinaza (ítem III.2/III.4) — no especificado en ninguna versión de la cotización.
2. Corriente nominal (A) y corriente de arranque (rotor bloqueado/LRA) de cada motor cotizado: motorreductor del feeder (0.75 kW), motor de la banda de huevo (0.55 kW), ventiladores (1.1 kW c/u).
3. Confirmación por escrito (no solo por correo informal) de compatibilidad de todos los motores con la red mexicana de 60 Hz sin costo adicional, y qué motores activarían el "extra cost of special motors" si el servicio eléctrico del predio no es trifásico 380V/50Hz ni monofásico 220V/50Hz.
4. Especificación eléctrica (voltaje, corriente, tipo de conexión) de los 2 actuadores lineales eléctricos de las entradas de aire CJ01 y de sus 2 controladores de entrada de aire (v3, ítems V.4–V.5).
5. Consumo eléctrico (W) del controlador YB (7″) y de los sensores DMR de temperatura/humedad (v3, bloque "Electrical Control System").
6. Si el motorreductor + torno de la cortina de blackout es el mismo actuador CJ01 ya cotizado para las entradas de aire, o una unidad eléctrica aparte.
7. Si existe un diagrama unifilar o ficha eléctrica de referencia del fabricante para una instalación tipo de 5 sets/640 aves.
