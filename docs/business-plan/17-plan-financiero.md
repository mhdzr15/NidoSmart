---
title: "Plan financiero preliminar"
project: "NidoSmart"
document_type: "business-plan"
status: "draft"
version: "1.2"
last_updated: "2026-09-14"
---

# Plan financiero preliminar

## 17.1 Inversión inicial

**Actualización (septiembre 2026):** el alcance de la inversión inicial quedó congelado en una **primera unidad financiable de 640 aves** (nave 17×4×4.2 m, jaula tipo H, 5 sets, 4 niveles — ver [Diseño físico](./07-diseno-fisico.md#71-módulo-inicial)). La tabla se recalculó a esa escala y ya no a la referencia anterior de 100 aves. La columna **Estado** indica cómo se obtuvo cada cifra, siguiendo la clasificación usada para congelar el alcance: *sustituido* (dato real de cotización), *recalculado* (estimación con una base de cálculo explícita) o *conservado* (no depende directamente del número de aves).

**Corrección (2026-09-14):** el 2026-08-03 el proveedor aclaró que el precio de $17,747 USD (etiquetado "DAP Puebla" en la cotización v1/v2) en realidad entrega **sólo hasta un almacén en la ciudad de Puebla** — no hasta el sitio del proyecto en San Francisco Acatepec. El tramo final (ciudad de Puebla → sitio) no está incluido en ese precio y todavía no se ha cotizado. La tabla siguiente separa ambos conceptos en vez de tratarlos como un solo monto confirmado.

| Concepto                                                                    | Estado | Rango estimado MXN |
| ----------------------------------------------------------------------------- | ------- | ---------------------: |
| Jaula automatizada tipo H (5 sets, 4 niveles) + alimentación automática + bebederos automáticos + banda de recolección de huevo + banda de retiro de gallinaza — 640 aves, entregado en almacén de la ciudad de Puebla | **Sustituido** — cotización FamTECH v1/v2, sin aranceles ni IVA (USD $17,747) | $328,300 *(fijo)* |
| Flete final: almacén en ciudad de Puebla → sitio del proyecto (San Francisco Acatepec) | **Pendiente** — aclarado por el proveedor el 2026-08-03 que no está incluido en el precio anterior; sin cotizar | Sin cotizar |
| Obra civil (nave 17×4×4.2 m, firme, drenaje, cercado)                        | **Recalculado** — por huella de la nave cotizada (≈68 m²) frente a la referencia genérica anterior de 18–24 m²; sin cotización formal de obra | $227,000–$421,000 |
| Agua: tanque pulmón, tratamiento y medición adicional (fuera de lo incluido en los bebederos) | **Recalculado** — mayor caudal por 5 sets; sin cotización formal | $20,000–$45,000 |
| Controlador, sensores y comunicaciones (capa NidoSmart: PLC/gateway, Node-RED, sensores adicionales) | **Conservado** — depende del número de naves/módulos, no directamente del número de aves | $25,000–$65,000 |
| Conectividad a internet y respaldo satelital (Starlink u otro, sólo equipo) | **Conservado** — no depende de la escala de aves | $8,000–$25,000 |
| UPS y respaldo energético                                                   | **Recalculado** — mayor carga eléctrica instalada (motores de los 5 sets tipo H); sin estudio de carga formal | $90,000–$220,000 |
| Bioseguridad y contingencias                                                | **Conservado**, ajuste menor por escala del predio | $25,000–$70,000 |
| **Total estimado (piso; excluye flete final Puebla→sitio, aún sin cotizar)** | | **$723,300–$1,174,300 + flete final pendiente** |

*(Partida opcional, en pausa — no incluida en el total: control ambiental (ventiladores, cooling pads, ventanas de entrada de aire, controlador, sensores temp/humedad), cotización FamTECH v3 = USD $24,095 total, es decir **USD $6,348 adicionales sobre v1/v2** (≈$117,400 MXN). Ver [Decisión vigente](../../evidence/quotations/README.md#decisión-vigente-2026-07-22): queda en pausa hasta definir el diseño de la nave.)*

*(Tipo de cambio de referencia usado para convertir la cotización en USD: $18.50 MXN/USD — un supuesto de trabajo, no una tasa contratada; debe actualizarse con el tipo de cambio vigente al momento de contratar. Los rangos "recalculado" y "conservado" son estimaciones preliminares sujetas a cotización formal con proveedores.)*

**Comparación con la referencia anterior:** la tabla previa (basada en un módulo genérico de 100 aves) estimaba $334,000–$765,000 MXN, es decir $180–$414 USD/ave equivalente. La tabla recalculada para 640 aves equivale a **≈$61–$99 USD/ave** (sin contar el flete final pendiente) — sensiblemente menor gracias a la mayor densidad de la jaula de 4 niveles y al precio unitario de la automatización ya cotizada ($27.73 USD/ave sólo en jaula + automatización entregada en ciudad de Puebla, ver [17.4 Interpretación](#174-interpretación)). Es decir, multiplicar por 6.4 el número de aves no multiplica por 6.4 la inversión: la inversión total, sin el flete final, sólo crece entre 1.5× y 2.2×.

No se incluyen:

* Terreno.
* Vehículo.
* Financiamiento.
* Impuestos.
* Permisos locales.
* Estudios ambientales.
* Obra mayor.
* Conexión eléctrica especial.
* Pozo.
* Mano de obra permanente.

## 17.2 Supuestos preliminares

Para el escenario base (primera unidad, 640 aves):

* Precio promedio: $4.20 por huevo.
* Producción comercializable año 1: ≈196,200 huevos.
* Consumo: 110–120 gramos de alimento por ave al día.
* Precio preliminar del alimento: $14.80 por kilogramo.

*(Contraste julio 2026: la industria reporta un consumo pico de referencia de 98–110 g/ave/día y una conversión alimenticia de 1.46–1.62 kg de alimento por docena de huevo (Bell & Weaver, capítulo 18). El supuesto de 110–120 g/ave/día de este documento queda ligeramente por encima de ese rango, lo que aporta un margen conservador razonable para el modelo preliminar.)*
* Venta directa o semidirecta.

**Actualización (septiembre 2026) — retiro del supuesto de expansión anual:** las versiones anteriores de este documento asumían una "expansión anual de 100 aves durante los primeros tres años". Ese supuesto queda retirado: la unidad mínima que realmente se construye y se financia es de 640 aves (no incrementos de 100), y el ritmo al que se agregue una segunda unidad depende de los resultados de la [validación del piloto](./18-validacion-del-piloto.md) y de conseguir financiamiento adicional (ver [proyecto de inversión](../investment-project/README.md)), no de un calendario fijo. Por eso la proyección siguiente cubre únicamente la primera unidad (640 aves); una segunda unidad es una decisión de financiamiento separada, fuera del alcance ya congelado.

*(Supuesto de trabajo: la producción comercializable año 1 de ≈196,200 huevos se obtiene escalando linealmente el valor puntual de 30,660 huevos usado en versiones anteriores del plan (100 aves) por el factor 6.4 —relación entre 640 y 100 aves—, manteniendo el mismo supuesto de 300–310 huevos/ave/año; es consistente con el rango de 192,000–198,400 huevos indicado en [Producción y capacidad comercial](./16-produccion-y-capacidad-comercial.md).)*

## 17.3 Proyección preliminar — primera unidad (640 aves)

| Concepto                    |      Año 1 |
| ----------------------------- | ----------: |
| Aves                         |        640 |
| Huevos vendidos              |    196,200 |
| Ingresos                     |   $824,040 |
| OPEX                         |   $785,677 |
| Flujo antes de CAPEX         |    $38,363 |

*(OPEX recalculado escalando linealmente por 6.4× el valor de $122,762 usado en la versión anterior del plan (100 aves). Esta escala uniforme es conservadora: no descuenta componentes de OPEX que no crecen proporcionalmente con el número de aves —por ejemplo, la conectividad a internet o parte de la administración—, por lo que el OPEX real por ave a 640 aves probablemente sea algo menor al aquí estimado.)*

Estas cifras son un ejercicio preliminar, no una cotización ni una garantía de rentabilidad. La tabla ya no proyecta un tercer año con expansión automática de módulos: como muestra la comparación anterior, el CAPEX de una segunda unidad (**$723,300–$1,174,300 MXN**, ver [17.1](#171-inversión-inicial)) supera ampliamente el flujo que la primera unidad puede generar en un año (**$38,363 MXN**), por lo que una segunda unidad requiere financiamiento externo y no puede autofinanciarse únicamente con el flujo operativo del piloto — precisamente la pregunta que atiende el [proyecto de inversión](../investment-project/README.md).

## 17.4 Interpretación

La primera unidad de 640 aves puede sostener buena parte de su operación, pero no recuperará rápidamente una instalación industrial sobredimensionada, y su flujo operativo por sí solo no financia una segunda unidad.

**Referencia de economía de escala (julio 2026):** un complejo industrial de referencia de un millón de aves (Bell & Weaver, capítulo 50) reporta un costo de capital total de aproximadamente **$15 USD/ave** (terreno, nave, equipo, edificio de empaque, molino de alimento y transporte incluidos). En contraste, la cotización vigente de jaula y automatización para la primera unidad de NidoSmart (ver [registro de cotizaciones](../../evidence/quotations/README.md)) equivale a **$27.73 USD/ave** ($17,747 USD / 640 aves; solo jaula + automatización entregada en un almacén de la ciudad de Puebla, sin control ambiental, empaque, molino, terreno **ni el flete final hasta el sitio del proyecto en San Francisco Acatepec, que aún no está cotizado**). Esta comparación cuantifica directamente por qué la automatización industrial completa no es económicamente accesible a la escala de 640–5,000 aves: el costo fijo de los equipos de manejo de huevo y clasificación (hasta 140,000 huevos/hora) solo se diluye lo suficiente a escala de cientos de miles o millones de aves.

La inversión mejora cuando:

* Los servicios compartidos atienden varios módulos.
* Aumenta la utilización de equipos.
* Se vende directamente.
* Se reduce el costo de alimento.
* Se optimizan rutas.
* Se disminuye la mano de obra por ave.
* Se mantiene alta productividad.
* La infraestructura inicial no tiene que reemplazarse.

## 17.5 Punto estratégico

Antes de invertir deberá prepararse un modelo financiero con tres escenarios:

### Conservador

* Menor postura.
* Precio de venta bajo.
* Alimento caro.
* Mayor mortalidad.
* Pérdidas comerciales.
* Crecimiento detenido.

### Base

* Productividad cercana a la guía genética.
* Venta directa estable.
* Costos controlados.
* Expansión gradual.

### Optimista

* Precio premium.
* Suscripciones completas.
* Mortalidad baja.
* Alto aprovechamiento de equipos.
* Venta de gallinaza.
* Crecimiento acelerado.

El objetivo financiero específico para la etapa piloto —incluyendo qué debe cubrir el módulo inicial y qué criterios validan el modelo antes de crecer— se desarrolla en [Validación del piloto](./18-validacion-del-piloto.md).

---

## Navegación

- [Índice general](./README.md)
- [Documento anterior: Producción y capacidad comercial](./16-produccion-y-capacidad-comercial.md)
- [Documento siguiente: Validación del piloto](./18-validacion-del-piloto.md)
