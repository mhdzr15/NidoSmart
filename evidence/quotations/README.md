# Registro de cotizaciones — Sistema de jaula tipo H

Seguimiento de cotizaciones recibidas para el sistema de jaula automatizada tipo H (piloto de 640 aves). Proveedor único hasta ahora: **FamTECH / ABC Machinery / Anyang Best Complete Machinery Engineering Co., Ltd** (contacto: bh@gcmec.com / bh@famtechpoultry.com).

## Historial de versiones

| Archivo | Fecha | No. cotización | Alcance | Incoterm | Precio total (USD) |
|---|---|---|---|---|---|
| `2026-07-21_FamTECH_v1_Jaula-Automatizacion_CIF-Puebla_USD17747.pdf` | 2026-07-21 | BS04H072126 | Jaula + alimentación + bebederos + recolección de huevo (5 sets, 640 aves) | CIF "Puebla port" (error: Puebla no tiene puerto, aclarado en v2) | $17,747 |
| `2026-07-21_FamTECH_v2_Jaula-Automatizacion_DAP-Puebla_USD17747.pdf` | 2026-07-21 | BS04H072226 | Igual que v1 (solo se corrigió el término de precio) | DAP Puebla (no incluye aranceles ni IVA) | $17,747 |
| `2026-07-22_FamTECH_v3_Jaula-Automatizacion-ControlAmbiental_DAP-Puebla_USD24095.pdf` | 2026-07-22 | BS04H072226 | v2 + equipo de control ambiental (ventiladores, cooling pads, ventanas de entrada de aire, controlador, sensores temp/humedad) | DAP Puebla (no incluye aranceles ni IVA) | $24,095 |

## Decisión vigente (2026-07-22)

Se continúa **solo con el alcance de jaula + automatización** (v1/v2, $17,747) — el control ambiental (sensores y actuadores) queda en pausa hasta definir el diseño de la nave.

## Pendientes con este proveedor

- Cotización DDP (con aranceles + IVA incluidos) para el alcance de jaula + automatización.
- ~~Confirmar si "grupo de jaula" equivale a un "set" de la cotización~~ — **Resuelto (2026-07-23):** confirmado por escrito, un "grupo de jaula" equivale a un "set" completo de 128 aves (ver hilo de correo [`mail_famtechpoultry.rtfd`](../correspondence/mail_famtechpoultry.rtfd/)).
- **Nuevo pendiente:** el proveedor indicó que el sistema admite "hasta 90 grupos en una nave de 120 m" (≈11,520 aves) compartiendo alimentación y recolección de huevo, agregando sólo jaula y bebederos por grupo adicional. Esa proporción (120 m/90 grupos ≈ 1.33 m/grupo) no coincide con la de nuestra nave (17 m/5 sets = 3.4 m/set), por lo que no puede asumirse como el techo real de expansión de nuestra configuración específica. Pendiente: preguntar directamente cuántos sets adicionales admite la MISMA unidad de arrastre de alimentación y de recolección de huevo de nuestro pedido (5 sets, 640 aves) antes de requerir un segundo sistema compartido completo.
- **Nuevo pendiente (2026-09-14):** confirmar si el precio cotizado incluye instalación en sitio del equipo (jaula, automatización) o si es una partida aparte — no se especifica en la cotización ni en el hilo de correo revisado. Necesario para el [presupuesto consolidado de inversión inicial](../../docs/investment-project/07-presupuesto-consolidado-inversion-inicial.md#11-instalación-y-puesta-en-marcha).
- **Importante — aclarar alcance de entrega ($17,747):** el 3 de agosto de 2026 el proveedor aclaró que el precio de $17,747 (nombrado "DAP Puebla" en la v1/v2) en realidad corresponde a término **CIP entregado en la ciudad de Puebla**, no en el sitio del proyecto en San Francisco Acatepec. El tramo final (ciudad de Puebla → San Francisco Acatepec) no está incluido y aún no se ha cotizado. Esto afecta el CAPEX usado en el plan financiero y el proyecto de inversión — pendiente de decisión sobre si corregir esas cifras.

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

- Dimensiones internas por jaula individual (ancho × fondo × alto por nivel) — necesarias para verificar cm²/ave contra el estándar de industria (ver [Diseño físico — Densidad de jaula](../../docs/business-plan/07-diseno-fisico.md#densidad-de-jaula-pendiente-de-verificación-con-proveedor)).
- Espacio lineal de comedero por ave (cm/ave).
- Relación de aves por níple bebedero.
- Diseño de luminarias para el sistema de 4 niveles (garantizar intensidad mínima en el nivel inferior).
- Especificación de aislamiento térmico (valor R o equivalente) para techo y paredes de la nave de 17×4×4.2 m.

Estas cinco preguntas fueron redactadas por NidoSmart el 2026-07-25 pero, según el hilo de correo revisado, no llegaron a enviarse al proveedor (quedaron en un correo dirigido a una cuenta propia) — siguen sin respuesta del proveedor.

**Nuevos pendientes de layout (2026-09-16, identificados al resolver las especificaciones de layout de la nave — ver [Diseño físico — 7.1.1](../../docs/business-plan/07-diseno-fisico.md#711-layout-funcional-recomendado-dentro-de-la-nave-17×4×42-m)):**

- Altura libre real requerida por el sistema completo instalado (stack de 4 niveles + riel del skip-hoist feeder + máquina recolectora de huevo sobre el nivel superior) — para confirmar que 4.2 m de altura total son suficientes.
- Footprint longitudinal real de cada uno de los 5 sets, incluyendo "front-end components" y "backend components and driver system", para confirmar que caben en los 17 m con espacio de circulación en ambas cabeceras.
- Footprint transversal (profundidad de jaula + pasillo central) del arreglo "double-sided" de 4 niveles, para confirmar que los 4 m de ancho son suficientes.

**Nuevos pendientes de iluminación (2026-09-17, identificados al definir la especificación de iluminación — ver [Automatización — Iluminación](../../docs/business-plan/08-automatizacion.md#iluminación); reducidos respecto al análisis inicial aplicando el criterio de revisar primero documentación de industria ya publicada por otros fabricantes de jaula tipo H antes de generar preguntas a FamTECH):**

- Si la estructura de jaula de nuestro pedido incluye el riel/soporte para tira LED en cada uno de los 4 niveles.
- Si la tira LED en sí está incluida en el precio del ítem "cage" (III.3) o es partida aparte — no aparece en ninguna versión de la cotización.
- Especificación eléctrica del riel/conector (voltaje, tipo de conexión) para poder comprar tiras LED compatibles localmente.

(Luminarias, tragaluces, cortinas de blackout y sensores de lux son partidas de otros proveedores, no de FamTECH — su cotización solo cubre el equipo listado línea por línea.)

**Nuevos pendientes de ventilación y control ambiental (2026-09-16, identificados al definir la estrategia de ventilación — ver [Automatización — Control ambiental](../../docs/business-plan/08-automatizacion.md#control-ambiental)):**

- Curva de desempeño real de los 2 ventiladores de 50"/1.1 kW ya cotizados en v3 (cfm a 0", 0.05" y 0.10" de columna de agua) — necesario para confirmar si cubren el rango calculado de 3,600–10,000 cfm para 640 aves.
- Si el paquete de control ambiental (v3, USD $6,347.6) puede re-cotizarse separando ventiladores + entradas de aire + controlador (de interés) de los cooling pads (no de interés por ahora, ver justificación climática en el documento de automatización).
- Área efectiva de cada una de las 12 entradas de aire CJ01 cotizadas.
- Si el controlador YB (7") permite ventilación escalonada (mínimo invierno → máximo verano) o solo on/off.
- **Cuántos sets adicionales admite la MISMA unidad de arrastre de alimentación y recolección de huevo de nuestro pedido (5 sets, 640 aves) antes de requerir un segundo sistema compartido completo** — esta pregunta ya existía por el lado de inversión (ver arriba, "Duda de Escalabilidad"). **Actualización 2026-09-17 ([DEC-014](../../docs/governance/registro-de-decisiones.md#dec-014--expansión-lineal-de-la-nave-con-equipo-de-alimentaciónrecolección-compartido-hasta-el-techo-declarado-por-el-proveedor)):** se confirmó que la expansión es lineal — una sola unidad de arrastre da servicio hasta el techo declarado de 90 sets (~11,520 aves), extendiendo esta misma nave. Esta pregunta ahora es central (no secundaria) para la arquitectura: determina la longitud final real de la nave (nuestra proporción de 17 m/5 sets ≈ 3.4 m/set, si se mantiene, implicaría ≈306 m para 90 sets, muy distinto a los 120 m de referencia del proveedor) y en qué punto conviene migrar el sistema de ventilación de transversal a modo túnel.
- **Nuevo pendiente (2026-09-17):** confirmar la extensibilidad de la cimentación/estructura civil declarada por el proveedor — si el diseño de la nave permite ampliarse linealmente por tramos (agregando sets) sin reconstruir cimentación, y cada cuántos sets se requiere un refuerzo estructural o una junta constructiva.
- **Dato ya confirmado, relevante para lo anterior:** el "Skip hoist feeder" (cotización v1/v2, item I.1) especifica textualmente **"a travel path of up to 100 meters"** — un límite técnico real, no estimado, sobre cuánto puede extenderse la misma línea de alimentación desde un solo hopper. Pendiente confirmar si ese límite de 100 m aplica al equipo específico de nuestro pedido o es una cifra genérica del catálogo, y si al llegar a ese límite se requiere una segunda línea de alimentación (y por tanto un segundo sistema compartido) o el equipo puede especificarse desde ahora para un recorrido mayor.

**Nuevos pendientes de agua y gallinaza (2026-09-18, identificados al definir los requisitos físicos de agua, drenaje y manejo de gallinaza — ver [Diseño físico — 7.2.1](../../docs/business-plan/07-diseno-fisico.md#721-drenaje-y-manejo-de-gallinaza-revisión-septiembre-2026) y [Arquitectura eléctrica/hidráulica — 9.2](../../docs/business-plan/09-arquitectura-electrica-hidraulica-comunicaciones.md#92-sistema-hidráulico)):**

- Capacidad real de la banda de retiro de gallinaza (kg/ciclo, velocidad) — la cotización confirma dimensiones (1.0×1130 mm) pero no throughput.
- Si la banda de gallinaza requiere agua para su limpieza — posible fuente de agua residual adicional no contemplada en el diseño hidráulico actual.
- Punto y altura de descarga de la banda al contenedor — necesario para diseñar el contenedor cerrado y su protección contra lluvia.
- Presión de operación recomendada por el fabricante de níples que use FamTECH (no identificado en la cotización) — sin esto no puede seleccionarse el regulador de presión con precisión.
- Diámetro y material de tubería recomendado por FamTECH para su línea de bebederos — necesario para la compatibilidad con el manifold de NidoSmart.
- Si la instalación en sitio de la banda de gallinaza (tramo banda → contenedor externo → zona de compostaje) está incluida en el precio cotizado o es responsabilidad de la obra civil de NidoSmart (relacionado con el pendiente ya abierto de instalación en sitio, ver "Pendientes con este proveedor" arriba).
