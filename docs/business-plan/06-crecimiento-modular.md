---
title: "Modelo modular de crecimiento"
project: "NidoSmart"
document_type: "business-plan"
status: "draft"
version: "1.5"
last_updated: "2026-09-28"
---

# Modelo modular de crecimiento

## 6.1 Principio de modularidad

Cada módulo deberá funcionar como una unidad productiva parcialmente independiente, con:

* Alojamiento.
* Línea de agua.
* Distribución de alimento.
* Recolección de huevo.
* Retiro de gallinaza.
* Sensores ambientales.
* Tablero secundario.
* Identificación digital.
* Contadores de consumo.
* Capacidad de aislamiento sanitario.

Los servicios principales deberán compartirse:

* Área de almacenamiento.
* Silo o tolva principal.
* Tratamiento y almacenamiento de agua.
* Cuarto eléctrico.
* Servidor local.
* Área de clasificación y empaque.
* Respaldo energético.
* Zona de compostaje.
* Filtro sanitario.
* Sistema de comunicaciones, incluyendo el enlace de internet primario y su respaldo satelital.

## 6.2 Escala recomendada

**Actualización (septiembre 2026):** la cotización vigente del proveedor de jaula automatizada (FamTECH — ver [registro de cotizaciones](../../evidence/quotations/README.md)) define una nave de 5 sets tipo H de 4 niveles, **640 aves**, como la unidad mínima real que se construye y se financia. Por eso el crecimiento ya no se modela en incrementos de decenas de aves (100, 200, 300…), sino en **unidades completas de 640 aves**. Las etapas "Validación" y "Microgranja comercial" de la tabla original (200–500 aves) quedan por debajo de esa unidad mínima y se retiran como escalones independientes; su contenido (mejorar margen, formalizar rutas e inventario) pasa a describir lo que ocurre *dentro* de la operación de la primera unidad, antes de construir la segunda.

| Etapa                          |         Capacidad | Objetivo                                            |
| ------------------------------- | ------------------: | --------------------------------------------------- |
| Primera unidad (piloto financiable) | 640 aves (1 unidad) | Aprendizaje, automatización y validación comercial  |
| Segunda unidad                 | 1,280 aves (2 unidades) | Mejorar margen y aprovechar servicios compartidos   |
| Operación pequeña              | 1,920–2,560 aves (3–4 unidades) | Incorporar personal y automatización administrativa |
| Operación mediana              | 2,560–3,840 aves (4–6 unidades) | Separar áreas funcionales y aumentar redundancia    |
| **Escala objetivo del plan**   | **≈5,120 aves (8 unidades)** | Operación profesional con gestión multiagente       |
| Techo declarado por el proveedor | **≈11,520 aves (90 grupos)** | Límite superior de la infraestructura compartida de alimentación y recolección de huevo ya cotizada — no es una meta del plan, es el techo de la inversión inicial |

**Dato importante:** la meta de este plan es llegar a 5,000 aves (≈8 unidades), pero según el proveedor (FamTECH), **la misma infraestructura compartida de alimentación y recolección de huevo que ya se está cotizando en la primera unidad admite hasta 90 "grupos de jaula" (≈11,520 aves)** sin necesitar un segundo sistema compartido completo — sólo agregando jaula y línea de bebederos por grupo adicional. Es decir, **la capacidad de la inversión inicial excede la meta del plan**: en principio no habría que duplicar el equipo de alimentación/recolección para llegar a 5,000 aves, sólo para superar ~11,520.

*(Confirmado por el proveedor por escrito el 2026-07-23: un "grupo de jaula" equivale a un "set" completo de 128 aves — el mismo "set" de la cotización (5 sets = 640 aves); 90 grupos × 128 aves = 11,520 aves.)*

**Discrepancia de densidad — resuelta (2026-09-28):** la advertencia que aquí figuraba (proporción del proveedor de 120 m/90 grupos ≈1.33 m/grupo, frente a los 17 m/5 sets ≈3.4 m/set de nuestra cotización) se debía a un error de método propio, no a una configuración distinta del proveedor. FamTECH aclaró por escrito (ver [correspondencia](../../evidence/correspondence/2026-09-28_FamTECH_email_respuesta-lote1-expansion-layout.rtfd)) que **no debe calcularse dividiendo los 17 m totales entre 5 sets**, porque esos 17 m incluyen además el equipo de cabecera (hopper/motorreductor en un extremo, máquina recolectora de huevo/unidad motriz en el otro) — equipo que se compra **una sola vez por fila**, sin importar si la fila tiene 5 o 90 sets. El valor que realmente se repite por set es el cuerpo de jaula, ya confirmado en 1.2×1.2 m — muy cercano a la proporción de referencia del proveedor (1.33 m/grupo), no 2.5× mayor como sugería el cálculo anterior. Esto hace mucho más plausible que el techo de 90 sets (~11,520 aves) sí aplique, en el orden de magnitud, a nuestra configuración específica — aunque la cifra exacta de cuántos sets admite la línea de nuestro pedido antes de requerir un segundo sistema compartido sigue pendiente con el ingeniero civil de FamTECH (ver [registro de cotizaciones](../../evidence/quotations/README.md#pendientes-con-este-proveedor)).

**Conciliación arquitectónica — corregida ([DEC-014](../governance/registro-de-decisiones.md#dec-014--expansión-lineal-de-la-nave-con-equipo-de-alimentaciónrecolección-compartido-hasta-el-techo-declarado-por-el-proveedor), 2026-09-17):** se confirmó que el crecimiento hacia el techo de 90 sets (~11,520 aves) ocurre **extendiendo linealmente esta misma nave**, con una sola unidad de arrastre de alimentación y recolección de huevo dando servicio a todos los sets — no construyendo naves independientes con equipo propio cada vez (esa conclusión, escrita el día anterior, fue un error corregido directamente por el usuario). Esto corrige la referencia a "alimentación, recolección de huevo... propios por módulo" en [DEC-004](../governance/registro-de-decisiones.md#dec-004--arquitectura-modular-de-crecimiento). Implicaciones: la ventilación debe planearse por etapas de crecimiento (transversal en las primeras etapas, migrando a modo túnel conforme la nave se alarga — ver [Automatización — Control ambiental](./08-automatizacion.md#control-ambiental)), y la cimentación/estructura civil debe diseñarse extensible desde ahora aunque solo se construyan los primeros 17 m. El footprint real por set ya está confirmado (1.2 m/set, ver arriba); sigue pendiente el footprint propio del equipo de cabecera y la longitud final exacta que implica el techo de 90 sets.

## 6.3 Criterios para agregar un módulo

No deberá añadirse un nuevo módulo sólo porque exista espacio físico. La expansión se autorizará cuando se cumplan simultáneamente las siguientes condiciones:

* Venta recurrente de al menos 85% de la producción.
* Cartera diversificada de clientes.
* Mortalidad dentro del rango objetivo.
* Datos confiables de consumo.
* Flujo suficiente para financiar parte de la ampliación.
* Procedimientos sanitarios estables.
* Capacidad de almacenamiento y reparto.
* Ausencia de fallas críticas recurrentes.
* Canal comercial probado durante varios meses.

Esta lista resume los criterios de expansión desde la perspectiva del crecimiento modular. La tabla detallada de criterios de éxito por área (comercial, financiera, producto, producción, sanidad, tecnología, operación, clientes y escalabilidad), utilizada para autorizar formalmente el segundo módulo, se encuentra en [Validación del piloto — Criterios de éxito antes de crecer](./18-validacion-del-piloto.md#1767-criterios-de-éxito-antes-de-crecer).

## 6.4 Requisitos de diseño de la primera nave para preservar la expansión (septiembre 2026)

**Objetivo de esta sección:** qué decisiones de diseño de la primera nave (640 aves) deben tomarse *ahora* para no bloquear ni sobrecostar la expansión hacia la segunda unidad (1,280 aves) y hacia el techo declarado por el proveedor (~90 sets, ~11,520 aves) — sin rediseñar el plan maestro completo, que sigue dependiendo del estudio de sitio pendiente ([Ficha técnica — Estado](../investment-project/05-ficha-tecnica-nave.md#estado-de-la-ficha-técnica)).

**Principio arquitectónico base ([DEC-014](../governance/registro-de-decisiones.md#dec-014--expansión-lineal-de-la-nave-con-equipo-de-alimentaciónrecolección-compartido-hasta-el-techo-declarado-por-el-proveedor)):** "segundo módulo" no significa una segunda nave independiente con equipo propio — significa **extender linealmente esta misma nave**, agregando jaula y bebederos por set, mientras una sola línea de arrastre sigue alimentando, recolectando huevo y retirando gallinaza para todos los sets hasta el límite técnico confirmado del equipo (skip-hoist feeder: recorrido de hasta 100 m). La segunda unidad (1,280 aves ≈ 10 sets) queda muy por debajo de ese límite.

| Área | Exclusivo de esta nave (no reservar de más) | Compartido (dimensionar con margen, no solo para 640) | Reserva a fijar ahora |
|---|---|---|---|
| **Agua** | Línea de níples de los 5 sets actuales (8 aves/níple, confirmado FamTECH) | Tanque pulmón, tratamiento, bomba principal + respaldo | Manifold con salidas de reserva no usadas; ver hallazgo 2 abajo |
| **Electricidad** | Motores y circuitos de esta nave (feeder, bandas, ventiladores, iluminación) | TGBT, cuarto técnico, UPS, generador, puesta a tierra | Subtablero con espacio físico reservado para la segunda unidad (ya decidido, [9.1.1](./09-arquitectura-electrica-hidraulica-comunicaciones.md#911-arquitectura-eléctrica-preliminar-revisión-septiembre-2026)) — no reducir el gabinete al justo de hoy |
| **Alimentación** | Silo/tolva de almacenamiento (capacidad a verificar) | Unidad de arrastre (skip-hoist feeder) — es el equipo compartido central, **no se duplica** al crecer dentro de su límite de 100 m | Confirmar con FamTECH cuántos sets admite ese mismo feeder antes de requerir una segunda línea (pendiente ya abierto en el [registro de cotizaciones](../../evidence/quotations/README.md#nuevos-pendientes-de-ventilación-y-control-ambiental-2026-09-16-identificados-al-definir-la-estrategia-de-ventilación-ver-automatización--control-ambiental)) |
| **Accesos** | Puertas y tapetes sanitarios de esta nave | Filtro sanitario único, cerco perimetral, vado/arco de desinfección — ver [Bioseguridad — 19.3](./20-bioseguridad.md#193-requisitos-constructivos-de-bioseguridad-especificación-para-proveedores) | Ver hallazgo 1 abajo (dirección de crecimiento) |
| **Gallinaza** | — (la banda de retiro es parte del sistema compartido, no exclusiva) | Banda de retiro (misma línea de arrastre, DEC-014), zona de compostaje, bordos, separación ≥30 m a pozo | Área de compostaje trazada con margen de volumen para la escala objetivo (≈5,120 aves), no solo para 640; ver hallazgo 4 abajo |
| **Vialidades** | Acceso inmediato a esta nave (descarga, retiro de gallinaza, recolección de producto) | Vialidad principal desde el filtro sanitario hacia almacén/empaque/compostaje | Corredor longitudinal libre en el sentido de crecimiento de la nave, para no romper vialidad ya construida — depende de la misma decisión que el hallazgo 1 |
| **Almacenamiento** | — | Almacén de alimento, área de clasificación/empaque, cámara de almacenamiento temporal | Ver hallazgo 3 abajo — no puede reservarse m² sin una cifra base |
| **Bioseguridad** | Mallas y tapetes de esta nave | Cerco perimetral, filtro sanitario, fosa de mortalidad, zona de gallinaza | Trazo del cerco pensado para el perímetro final del predio, no solo alrededor de 17×4 m — mismo bloqueo que el hallazgo 1 |

**Hallazgos — resueltos (2026-09-23):**

1. **Dirección de crecimiento — decidido.** Cabecera A (alimentación) queda fija: filtro sanitario, acceso principal y cuarto técnico se sitúan de forma permanente en ese extremo; la nave crece agregando sets junto a Cabecera B (huevo/gallinaza), que se desplaza hacia afuera. Ver [Diseño físico — 7.1.1](./07-diseno-fisico.md#711-layout-funcional-recomendado-dentro-de-la-nave-17×4×42-m).
2. **Tanque de agua — redimensionado.** Piso de diseño actualizado de ≥500 L a **≥1,000 L útiles**, aplicando el mismo margen de 1,280 aves ya usado en electricidad. Ver [Arquitectura eléctrica/hidráulica — 9.2](./09-arquitectura-electrica-hidraulica-comunicaciones.md#92-sistema-hidráulico).
3. **Espacios de servicio — dimensionados preliminarmente.** Almacén ≈12–18 m², empaque ≈8–12 m², sin cámara dedicada a esta escala — cálculo con datos ya existentes (consumo de alimento Hy-Line, producción de huevo), con margen para 1,280 aves. Ver [Diseño físico — 7.2.1](./07-diseno-fisico.md#721-dimensionamiento-preliminar-de-espacios-de-servicio-septiembre-2026).
4. **Capacidad de la banda de gallinaza — cifra objetivo calculada.** Se requiere que la banda (equipo compartido y lineal, no se duplica) soporte ≈1,000 kg/día (meta del plan, no el techo de 90 sets) sin acumulación; esta cifra se envía como pregunta concreta a FamTECH en lugar de preguntar en abierto. Ver [Automatización — Retiro de gallinaza](./08-automatizacion.md#retiro-de-gallinaza) y [registro de cotizaciones](../../evidence/quotations/README.md#nuevos-pendientes-de-agua-y-gallinaza-2026-09-18-identificados-al-definir-los-requisitos-físicos-de-agua-drenaje-y-manejo-de-gallinaza-ver-diseño-físico--722-y-arquitectura-eléctricahidráulica--92).

---

## Navegación

- [Índice general](./README.md)
- [Documento anterior: Objetivos del proyecto](./05-objetivos.md)
- [Documento siguiente: Diseño físico preliminar](./07-diseno-fisico.md)
