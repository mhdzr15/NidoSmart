---
title: "Presupuesto consolidado de inversión inicial — unidad de 640 aves"
project: "NidoSmart"
document_type: "investment-project"
status: "draft"
version: "1.0"
last_updated: "2026-09-14"
---

# Presupuesto consolidado de inversión inicial — unidad de 640 aves

Este documento reconstruye el monto total requerido para llevar la unidad de 640 aves ([DEC-012](../governance/registro-de-decisiones.md#dec-012--congelamiento-del-alcance-de-la-inversión-inicial-en-una-unidad-productiva-de-640-aves)) desde su estado actual hasta condiciones reales de producción y comercialización: infraestructura, equipamiento, logística, vehículo, y capital de arranque.

**Método:** cada partida se clasifica con un nivel de certeza — **Confirmado** (cotización o dato contractual real), **Cotizado** (existe cotización pero la partida está en pausa o fuera del alcance actual), **Estimado** (cálculo con método explícito, sin cotización formal) o **Pendiente** (sin dato, sin poder estimar de forma responsable). Esta clasificación extiende la ya usada para congelar el alcance en [Plan financiero — 17.1](../business-plan/17-plan-financiero.md#171-inversión-inicial) y [Proyecto de inversión — 3](./01-proyecto-de-inversion.md#3-inversión-inicial-capex). Ningún monto de este documento sustituye una cotización real; donde no existe, se dice explícitamente.

Tipo de cambio de referencia: **$18.50 MXN/USD** — supuesto de trabajo, no una tasa contratada (mismo usado en el resto del plan financiero).

## 1. Jaulas y automatización

| Concepto | Especificación | Proveedor/Fuente | Cantidad | Costo unitario | Costo total | Estado |
|---|---|---|---|---|---|---|
| Jaula automatizada tipo H + alimentación + bebederos + recolección de huevo + retiro de gallinaza | 5 sets, 4 niveles, 640 aves, entregado en almacén de ciudad de Puebla (CIP) | FamTECH, cotización v1/v2 (2026-07-21), No. BS04H072226 | 1 sistema | USD $17,747 | **$328,300 MXN** | **Confirmado** |

El desglose del costo puesto en sitio (flete, seguro, aranceles, IVA, despacho, transporte final) se reconstruye en la [sección 10](#10-importación-y-logística), no aquí, para no duplicar el monto del equipo.

## 2. Nave avícola / 3. Obra civil

Se presentan juntas porque, con la ficha técnica actual, **no es posible separar el costo de la estructura de la nave del costo de obra civil** — ver [Ficha técnica — Nave avícola, pendiente #1](./05-ficha-tecnica-nave.md#estado-de-la-ficha-técnica) (tipo estructural aún sin decidir).

| Concepto | Especificación | Fuente | Costo total (MXN) | Estado |
|---|---|---|---|---|
| Nave + obra civil (estructura, firme, drenaje, cercado) | Huella ≈68 m² (17×4×4.2 m) | Recalculado por huella vs. la referencia genérica anterior de 18–24 m²; sin cotización formal | **$227,000–$421,000** | **Estimado** |

Este rango **no debe tratarse como comparable entre contratistas** hasta cerrar los pendientes críticos de la ficha técnica (tipo estructural, materiales, altura libre, orientación, cubierta, muros, drenaje, resistencia a viento/granizo, piso, integración con la jaula). Ver [ficha técnica completa](./05-ficha-tecnica-nave.md).

## 4. Infraestructura eléctrica

| Concepto | Especificación | Fuente | Costo total (MXN) | Estado |
|---|---|---|---|---|
| Tablero principal, subtablero por módulo, protecciones, puesta a tierra, paros de emergencia | Ver [Arquitectura eléctrica — 9.1](../business-plan/09-arquitectura-electrica-hidraulica-comunicaciones.md#91-sistema-eléctrico) | Sin cotización; orden de magnitud para una instalación de esta escala | **$30,000–$70,000** | **Estimado** |

No incluye el UPS/respaldo energético (sección 8) ni el estudio de carga eléctrica, todavía pendiente (ver [Plan financiero — 17.1](../business-plan/17-plan-financiero.md#171-inversión-inicial)).

## 5. Infraestructura hidráulica

| Concepto | Especificación | Fuente | Costo total (MXN) | Estado |
|---|---|---|---|---|
| Tanque pulmón, bomba principal y de respaldo, manifold, medidor, filtros, válvulas | Ver [Arquitectura eléctrica/hidráulica — 9.2](../business-plan/09-arquitectura-electrica-hidraulica-comunicaciones.md#92-sistema-hidráulico) | Recalculado por mayor caudal de 5 sets; sin cotización formal | **$20,000–$45,000** | **Estimado** |

Pendiente: análisis de calidad de agua del predio (pH, dureza, coliformes) señalado en el mismo documento — puede agregar costo de tratamiento no incluido en este rango si el agua no cumple los parámetros.

## 5.1 Drenaje, aguas residuales y manejo de gallinaza

| Concepto | Especificación | Fuente | Costo total (MXN) | Estado |
|---|---|---|---|---|
| Zona de compostaje con bordos, sistema de tratamiento de aguas residuales (fosa séptica o biodigestor si no hay alcantarillado municipal) y canaletas/cárcamo de drenaje pluvial | Ver [Diseño físico — 7.2.1](../business-plan/07-diseno-fisico.md#721-drenaje-y-manejo-de-gallinaza-revisión-septiembre-2026) | Sin cotización; orden de magnitud — no desglosado antes de esta revisión (estaba disuelto sin partida propia dentro de "obra civil", sección 2/3) | **$40,000–$90,000** | **Estimado (genérico)** |

Este rango depende fuertemente de si existe alcantarillado sanitario municipal en San Francisco Acatepec (pendiente crítico, ver [Regulación y cumplimiento — 18.1](../business-plan/19-regulacion-y-cumplimiento.md#181-trámites-específicos-para-san-francisco-acatepec-san-andrés-cholula-puebla)): si no existe, el extremo alto del rango es más probable por el costo de un sistema de tratamiento propio.

## 6. Ventilación y control ambiental

| Concepto | Especificación | Fuente | Costo total (MXN) | Estado |
|---|---|---|---|---|
| Ventilación básica (entradas/salidas de aire pasivas, integradas a la nave) | Sin diseño de aberturas todavía — ver [ficha técnica](./05-ficha-tecnica-nave.md) | Incluido conceptualmente en la partida de obra civil (sección 2/3), sin desglose propio | Incluido arriba | **Pendiente** (sin diseño) |
| Paquete de control ambiental automatizado (ventiladores, cooling pads, ventanas motorizadas, controlador, sensores temp/humedad) | Adicional sobre la jaula base | FamTECH, cotización v3 (2026-07-22), No. BS04H072226 | USD $6,348 adicionales ≈ **$117,400 MXN** | **Cotizado, en pausa** — no incluido en el total (ver [decisión vigente](../../evidence/quotations/README.md#decisión-vigente-2026-07-22)) |

## 7. Iluminación

| Concepto | Especificación | Fuente | Costo total (MXN) | Estado |
|---|---|---|---|---|
| Luminarias para sistema de 4 niveles, con intensidad mínima garantizada en nivel inferior | Ver [Automatización — Iluminación](../business-plan/08-automatizacion.md#iluminación); diseño de luminarias aún no confirmado por el proveedor de jaula | Sin cotización; orden de magnitud para 68 m² | **$15,000–$35,000** | **Estimado** |

## 8. Respaldo energético

| Concepto | Especificación | Fuente | Costo total (MXN) | Estado |
|---|---|---|---|---|
| UPS y respaldo energético para cargas críticas (ventilación mínima, agua, controladores, comunicaciones, alarmas) | Ver [Arquitectura eléctrica — cargas críticas](../business-plan/09-arquitectura-electrica-hidraulica-comunicaciones.md#91-sistema-eléctrico) | Recalculado por mayor carga eléctrica de los motores de los 5 sets; sin estudio de carga formal | **$90,000–$220,000** | **Estimado** |

## 9. Sensores y control

| Concepto | Especificación | Fuente | Costo total (MXN) | Estado |
|---|---|---|---|---|
| Controlador (PLC/gateway), sensores adicionales, Node-RED | Capa NidoSmart, no depende directamente del número de aves. Incluye ahora, de forma explícita (2026-09-17): sensor de amoníaco (NH₃, obligatorio — dispara el umbral de ventilación de 30 ppm), sensor de CO₂ (obligatorio, umbral de alarma aún pendiente), y 4 sensores de lux (uno por nivel de jaula) — ninguno incluido en la cotización FamTECH. Ver [Automatización — Control ambiental](../business-plan/08-automatizacion.md#control-ambiental) e [Iluminación](../business-plan/08-automatizacion.md#iluminación) | Conservado de la versión anterior del plan financiero; monto sin verificar contra estas partidas ahora explícitas | **$25,000–$65,000** | **Estimado (conservado, pendiente re-verificar rango)** |
| Conectividad a internet y respaldo satelital (Starlink u otro, sólo equipo) | Ver [Arquitectura — 9.3.1](../business-plan/09-arquitectura-electrica-hidraulica-comunicaciones.md#931-conectividad-a-internet-como-requisito-permanente) | Conservado | **$8,000–$25,000** | **Estimado (conservado)** |
| **Subtotal sensores y control** | | | **$33,000–$90,000** | |

## 10. Importación y logística

Reconstrucción del costo total puesto en sitio del sistema de jaulas (equipo de la [sección 1](#1-jaulas-y-automatización)):

| Concepto | Base de cálculo | Monto (MXN) | Estado |
|---|---|---|---|
| Equipo (CIP ciudad de Puebla) | USD $17,747 × $18.50 | $328,300 | **Confirmado** (ya contado en sección 1, no se suma dos veces) |
| Flete internacional a Puebla | Incluido en el precio anterior | Incluido | **Confirmado** — término CIP lo incluye por definición |
| Seguro de transporte a Puebla | Incluido en el precio anterior | Incluido | **Confirmado** — "CIP" = *Carriage and Insurance Paid to*, incluye seguro por definición del incoterm; no es necesario preguntarlo al proveedor |
| Arancel de importación | 0–10% sobre valor CIF, sin clasificación arancelaria formal | $0–$32,800 | **Estimado (genérico)** — pendiente consultar agente aduanal para la fracción arancelaria real |
| IVA de importación (16%) | 16% sobre (CIF + arancel) | $52,500–$57,800 | **Estimado** — depende del arancel real |
| Despacho aduanal | Honorarios típicos de agente aduanal para un embarque de este valor | $8,000–$15,000 | **Estimado (genérico)** — sin cotización de agente aduanal |
| Transporte final: almacén Puebla → sitio del proyecto (San Francisco Acatepec) | Aclarado por el proveedor el 2026-08-03 que no está incluido en el precio | Sin cotizar | **Pendiente** |
| **Subtotal puesto en sitio (excluye transporte final, ya contado el equipo en sección 1)** | | **$60,500–$105,600** *(sin equipo)* | Mixto |

**Importante:** el subtotal de esta sección ($60,500–$105,600 MXN) es el monto **adicional** a los $328,300 MXN del equipo — no se suma dos veces en el consolidado. El transporte final Puebla→sitio queda fuera de todos los totales de este documento por no tener cotización.

## 11. Instalación y puesta en marcha

| Concepto | Especificación | Fuente | Costo total (MXN) | Estado |
|---|---|---|---|---|
| Instalación de la jaula, automatización y sistemas asociados en sitio | No especificado en la cotización ni en el hilo de correo revisado si el precio incluye supervisión/instalación o si es un costo aparte | — | Sin cotizar | **Pendiente** — nuevo punto a aclarar con el proveedor (ver [registro de cotizaciones](../../evidence/quotations/README.md)) |

## 12. Aves

| Concepto | Especificación | Fuente | Cantidad | Costo unitario | Costo total (MXN) | Estado |
|---|---|---|---|---|---|---|
| Pollitas de recría (punto de postura, ~16–18 semanas) | Sin proveedor identificado todavía (ver [Hoja de ruta, paso 8](../business-plan/23-hoja-de-ruta.md#próximos-pasos-inmediatos)) | Orden de magnitud de mercado, sin cotización | 640 | $120–$180 | **$76,800–$115,200** | **Estimado (genérico)** |

Comprar pollitas ya cercanas al punto de postura (en vez de pollito de un día) es el supuesto que sustenta el cálculo de [capital de trabajo](#17-capital-de-trabajo-inicial): reduce el periodo de arranque sin ingresos.

## 13. Bioseguridad

| Concepto | Especificación | Fuente | Costo total (MXN) | Estado |
|---|---|---|---|---|
| Perímetro controlado, entrada única, filtro sanitario, control de fauna | Ver [Bioseguridad — 19.1](../business-plan/20-bioseguridad.md#191-medidas-mínimas) | Conservado, ajuste menor por escala del predio | **$25,000–$70,000** | **Estimado (conservado)** |

Los insumos consumibles iniciales de bioseguridad (desinfectantes, ropa, tapetes) se cuentan en [inventarios mínimos](#19-costos-de-puesta-en-producción-preoperativos), no aquí, para no duplicar.

## 14. Almacenamiento y manejo de producto

| Concepto | Especificación | Fuente | Costo total (MXN) | Estado |
|---|---|---|---|---|
| Mesa de inspección, báscula, estantería para cartones, zona de almacenamiento temporal | Ver [Diseño físico — 7.2](../business-plan/07-diseno-fisico.md#72-áreas-generales-del-predio) | Sin cotización; orden de magnitud | **$20,000–$45,000** | **Estimado** |

El costo de empaque (cartones, consumible recurrente) se cuenta en [preoperativos](#19-costos-de-puesta-en-producción-preoperativos), no aquí, por ser un consumible y no un activo.

## 15. Vehículo de distribución

Desarrollo completo en [Vehículo de distribución](./06-vehiculo-de-distribucion.md). Conclusión: **no se recomienda comprar un vehículo dedicado para esta etapa** (volumen ≈32 kg/día no lo justifica); se recomienda cubrir la distribución con capital propio/vehículo existente.

| Concepto | Costo total (MXN) | Estado |
|---|---|---|
| Vehículo dedicado (no incluido en el total de este documento) | $0 *(decisión: usar capital propio)* — alternativa si se reconsidera: $180,000–$350,000 (seminuevo) | **Decidido** (no cotización) |

## 16. Permisos y trámites

| Concepto | Especificación | Fuente | Costo total (MXN) | Estado |
|---|---|---|---|---|
| Registro SENASICA, uso de suelo, licencia de construcción, permisos municipales, trámites de agua | Ver [Regulación y cumplimiento — 18.1](../business-plan/19-regulacion-y-cumplimiento.md#181-trámites-específicos-para-san-francisco-acatepec-san-andrés-cholula-puebla) | Sin tabulador municipal confirmado; orden de magnitud | **$20,000–$60,000** | **Estimado (genérico)** |

## 17. Capital de trabajo inicial

Cubre la brecha operativa mientras la parvada alcanza su pico de postura. Con pollitas de ~16 semanas (112 días, primer huevo) hasta pico a las 26 semanas (182 días) — ver [Producción y capacidad comercial](../business-plan/16-produccion-y-capacidad-comercial.md) —, se estima un colchón de 1 a 2 meses de OPEX.

| Concepto | Base de cálculo | Costo total (MXN) | Estado |
|---|---|---|---|
| Colchón operativo (1–2 meses de OPEX) | OPEX año 1 = $785,677 MXN ÷ 12 = $65,473/mes ([Plan financiero — 17.3](../business-plan/17-plan-financiero.md#173-proyección-preliminar--primera-unidad-640-aves)) | **$65,500–$131,000** | **Estimado** |

## 18. Contingencia

Contingencia diferenciada y justificada por área de riesgo, en vez de un porcentaje único arbitrario:

| Área de riesgo | Base sobre la que aplica | % | Monto (MXN) |
|---|---|---|---|
| Importación y tipo de cambio (equipo + costos de importación, sección 1+10) | $388,800–$433,900 | 10% | $38,900–$43,400 |
| Obra civil (sin cotización formal, sección 2/3 + resto de infraestructura, incluye 5.1) | $500,000–$1,086,000 | 15% | $75,000–$162,900 |
| Instalación y adecuaciones no previstas (logística restante + preoperativos + capital de trabajo) | $311,400–$577,200 | 10% | $31,100–$57,700 |
| **Contingencia total** | | **≈12–13% del subtotal** | **$145,000–$264,000** |

El componente de tipo de cambio no se cuenta aparte: queda incorporado en el 10% de importación, ya que el riesgo cambiario recae principalmente sobre la parte de la inversión cotizada en USD.

## Tabla consolidada

| Bloque | Rango (MXN) | Incluye |
|---|---:|---|
| CAPEX productivo | $328,300 | Jaula + automatización (sección 1) |
| CAPEX de infraestructura | $500,000–$1,086,000 | Nave/obra civil, eléctrica, hidráulica, drenaje/aguas residuales/gallinaza, iluminación, respaldo energético, sensores y control, bioseguridad (infraestructura), almacenamiento y manejo de producto (secciones 2–9, 5.1, 13, 14) |
| CAPEX logístico | $60,500–$105,600 | Aranceles, IVA, despacho aduanal (sección 10, sin equipo ni transporte final) |
| Costos preoperativos | $185,400–$340,600 | Aves, alimento inicial, veterinario, medicamentos, empaques, personal inicial, servicios, inventarios mínimos, permisos (secciones 12, 16, 19) |
| Capital de trabajo | $65,500–$131,000 | Colchón operativo 1–2 meses (sección 17) |
| Contingencia | $145,000–$264,000 | Diferenciada por área de riesgo (sección 18) |
| **Inversión total (estimada)** | **≈$1,285,000–$2,256,000** | |

**Explícitamente fuera de este total, por no tener cotización:**

* Transporte final almacén Puebla → sitio del proyecto (sección 10).
* Instalación de la jaula/automatización en sitio, si tiene costo aparte (sección 11).
* Paquete de control ambiental automatizado, en pausa (sección 6): +$117,400 MXN si se reactiva.
* Vehículo dedicado, si se reconsidera la recomendación de la sección 15: +$180,000–$350,000 MXN.
* Terreno (no forma parte de este alcance en ningún escenario).

## 19. Costos de puesta en producción (preoperativos)

Detalle de las partidas de arranque que no son activos fijos (ver [sección 12](#12-aves) para el costo de las aves, contado aparte):

| Concepto | Base de cálculo | Costo total (MXN) | Estado |
|---|---|---|---|
| Alimento inicial (30–60 días) | 640 aves × 0.115 kg/ave/día × $14.80/kg ([Plan financiero — 17.2](../business-plan/17-plan-financiero.md#172-supuestos-preliminares)) | $32,700–$65,400 | **Estimado** |
| Veterinario (consulta inicial, programa sanitario) | Sin cotización; orden de magnitud | $15,000–$30,000 | **Estimado (genérico)** |
| Medicamentos y vacunas iniciales | Sin cotización; orden de magnitud | $5,000–$10,000 | **Estimado (genérico)** |
| Empaques (cartones, ~1 mes de producción) | ≈1,230 docenas/mes × $4/docena | $4,900–$6,000 | **Estimado** |
| Personal inicial (capacitación/arranque, 1 mes) | Sin estructura salarial definida; orden de magnitud | $16,000–$24,000 | **Estimado (genérico)** |
| Servicios (luz/agua preoperativos) | Sin cotización; orden de magnitud | $5,000–$10,000 | **Estimado (genérico)** |
| Inventarios mínimos (bioseguridad consumible, refacciones básicas) | Sin cotización; orden de magnitud | $10,000–$20,000 | **Estimado (genérico)** |
| Permisos y trámites (sección 16) | Ver sección 16 | $20,000–$60,000 | **Estimado (genérico)** |
| Aves (sección 12) | Ver sección 12 | $76,800–$115,200 | **Estimado (genérico)** |
| **Total preoperativos** | | **$185,400–$340,600** | |

## Clasificación general de partidas

De las partidas de este presupuesto:

* **Confirmado** (cotización real): equipo de jaula y automatización, flete internacional a Puebla, seguro de transporte a Puebla — 3 partidas.
* **Cotizado, en pausa** (existe cotización pero no está en el alcance actual): paquete de control ambiental automatizado — 1 partida.
* **Decidido** (no requiere cotización porque se optó por no comprar): vehículo dedicado — 1 partida.
* **Estimado** (cálculo con método explícito, sin cotización formal): la gran mayoría de las partidas de infraestructura, preoperativos y capital de trabajo — ≈19 partidas.
* **Pendiente** (sin dato, no estimado): transporte final Puebla→sitio, instalación de la jaula en sitio, y todos los pendientes críticos de la [ficha técnica de la nave](./05-ficha-tecnica-nave.md#estado-de-la-ficha-técnica) que impiden cotizar formalmente la obra civil.

**Lectura honesta del resultado:** este presupuesto todavía **no** cumple el estándar de "presupuesto trazable y técnicamente sustentado" que exige el objetivo, porque la partida más grande de infraestructura (nave + obra civil, hasta $421,000 MXN) sigue siendo una estimación por huella, no una cotización comparable, y dos partidas de importación (transporte final, instalación) siguen sin cotizar. Lo mismo aplica a la partida de drenaje/aguas residuales/gallinaza (sección 5.1, agregada en la revisión de septiembre 2026), cuyo rango depende de un pendiente crítico aún sin resolver (disponibilidad de alcantarillado municipal). El rango de $1.29M–$2.26M MXN debe tratarse como el **piso de trabajo actual**, no como el monto de crédito a solicitar.

## Qué puede financiarse con crédito vs. capital propio

Orientación general (sujeta a confirmar con la institución específica — FIRA/FONAGA u otra, ver [`knowledge-base/financing/`](../../knowledge-base/)):

* **Crédito refaccionario** (activo fijo, plazo largo): CAPEX productivo (jaula/automatización) y CAPEX de infraestructura (nave, obra civil, instalaciones eléctricas/hidráulicas, respaldo energético, sensores) — son los rubros que típicamente califican como activo fijo productivo.
* **Crédito de avío** (insumos del ciclo productivo, plazo corto): costos preoperativos (aves, alimento inicial, veterinario, medicamentos) y capital de trabajo — son gasto corriente del ciclo, no activo fijo.
* **Capital propio (fuera del crédito):** vehículo (ver [sección 15](#15-vehículo-de-distribución)), permisos y trámites (con frecuencia no financiables), y la contingencia general, salvo que el programa específico indique lo contrario.

Esta distinción es orientativa y debe confirmarse con los requisitos reales del programa de financiamiento elegido antes de armar el expediente ([Proyecto de inversión — 6. Pendientes](./01-proyecto-de-inversion.md#6-pendientes-antes-de-formalizar-el-expediente)).

## Navegación

- [Índice de proyecto de inversión](./README.md)
- [Documento anterior: Vehículo de distribución](./06-vehiculo-de-distribucion.md)
- [Documento relacionado: Proyecto de inversión](./01-proyecto-de-inversion.md)
