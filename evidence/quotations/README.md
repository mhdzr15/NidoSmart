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
