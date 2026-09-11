---
title: "Plan financiero preliminar"
project: "NidoSmart"
document_type: "business-plan"
status: "draft"
version: "1.0"
last_updated: "2026-07-25"
---

# Plan financiero preliminar

## 17.1 Inversión inicial

| Concepto                                                                       |    Rango estimado MXN |
| -------------------------------------------------------------------------------- | ---------------------: |
| Obra civil ligera, firme, drenaje y cercado                                     |       $70,000–$130,000 |
| Alojamiento modular                                                              |       $60,000–$120,000 |
| Alimentación automática                                                          |        $18,000–$40,000 |
| Agua, filtrado y medición                                                        |        $15,000–$30,000 |
| Ventilación y control térmico                                                   |        $45,000–$95,000 |
| Controlador, sensores y comunicaciones                                          |        $25,000–$65,000 |
| Conectividad a internet y respaldo satelital (Starlink u otro, sólo equipo)      |         $8,000–$25,000 |
| Recolección automática de huevo                                                 |        $20,000–$55,000 |
| Retiro de gallinaza                                                              |        $18,000–$40,000 |
| UPS y respaldo energético                                                        |       $35,000–$110,000 |
| Bioseguridad y contingencias                                                     |        $20,000–$55,000 |
| **Total estimado**                                                               |  **$334,000–$765,000** |

*(Pendiente de cotización: los rangos anteriores son estimaciones preliminares sujetas a cotización formal con proveedores.)*

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

Para el escenario base:

* Precio promedio: $4.20 por huevo.
* Producción comercializable año 1: 30,660 huevos.
* Consumo: 110–120 gramos de alimento por ave al día.
* Precio preliminar del alimento: $14.80 por kilogramo.

*(Contraste julio 2026: la industria reporta un consumo pico de referencia de 98–110 g/ave/día y una conversión alimenticia de 1.46–1.62 kg de alimento por docena de huevo (Bell & Weaver, capítulo 18). El supuesto de 110–120 g/ave/día de este documento queda ligeramente por encima de ese rango, lo que aporta un margen conservador razonable para el modelo preliminar.)*
* Venta directa o semidirecta.
* Expansión anual de 100 aves durante los primeros tres años.

*(Supuesto de trabajo: la producción comercializable año 1 de 30,660 huevos es un valor puntual dentro del rango de 30,000–31,000 huevos indicado en [Producción y capacidad comercial](./16-produccion-y-capacidad-comercial.md); ambos valores se conservan porque provienen de niveles de precisión distintos del mismo ejercicio preliminar.)*

## 17.3 Proyección preliminar

| Año | Módulos | Huevos vendidos | Ingresos |     OPEX | Flujo antes de expansión | CAPEX de expansión | Flujo neto |
| ---- | -------: | ----------------: | --------: | --------: | -------------------------: | -------------------: | ----------: |
| 1    |        1 |             30,660 |  $128,772 |  $122,762 |                     $6,010 |                  $0 |     $6,010 |
| 2    |        2 |             59,130 |  $248,346 |  $212,211 |                    $36,135 |            $110,000 |   -$73,865 |
| 3    |        3 |             85,410 |  $358,722 |  $302,346 |                    $56,376 |            $110,000 |   -$53,624 |

Estas cifras son un ejercicio preliminar, no una cotización ni una garantía de rentabilidad.

## 17.4 Interpretación

El módulo de 100 aves puede sostener buena parte de su operación, pero no recuperará rápidamente una instalación industrial sobredimensionada.

**Referencia de economía de escala (julio 2026):** un complejo industrial de referencia de un millón de aves (Bell & Weaver, capítulo 50) reporta un costo de capital total de aproximadamente **$15 USD/ave** (terreno, nave, equipo, edificio de empaque, molino de alimento y transporte incluidos). En contraste, la cotización vigente de jaula y automatización para el piloto de NidoSmart (ver [registro de cotizaciones](../cotizaciones/README.md)) equivale a **$27.73 USD/ave** (solo jaula + automatización, sin control ambiental, empaque, molino ni terreno). Esta comparación cuantifica directamente por qué la automatización industrial completa no es económicamente accesible a la escala de 100–5,000 aves: el costo fijo de los equipos de manejo de huevo y clasificación (hasta 140,000 huevos/hora) solo se diluye lo suficiente a escala de cientos de miles o millones de aves.

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
