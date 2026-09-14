---
title: "Proyecto de inversión"
project: "NidoSmart"
document_type: "investment-project"
status: "draft"
version: "1.2"
last_updated: "2026-09-14"
---

# Proyecto de inversión

## 1. Alcance congelado

El proyecto financiable real de NidoSmart es una **primera unidad productiva de 640 gallinas ponedoras**, no el módulo genérico de ~100 aves usado en versiones anteriores del plan de negocios. Esta decisión quedó formalizada en [DEC-012](../governance/registro-de-decisiones.md#dec-012--congelamiento-del-alcance-de-la-inversión-inicial-en-una-unidad-productiva-de-640-aves) del registro de decisiones.

El alcance queda definido por la cotización vigente del proveedor de jaula automatizada (FamTECH — ver [registro de cotizaciones](../../evidence/quotations/README.md)):

* Nave de **17 × 4 × 4.2 m** (≈68 m² de huella).
* Jaula automatizada tipo H, **4 niveles, 5 sets** (128 aves por set).
* **640 aves totales.**
* Incluye: alimentación automática (skip hoist feeder), bebederos automáticos tipo níple, banda de recolección de huevo, banda de retiro de gallinaza.

Este es exactamente lo que se construirá con el crédito: una unidad completa, no una fracción ni un múltiplo hipotético.

**Importante:** la cotización de $17,747 USD entrega el equipo hasta un almacén en la **ciudad de Puebla**, no hasta el sitio del proyecto en San Francisco Acatepec (aclarado por el proveedor el 2026-08-03; ver sección 3). El flete final aún no está cotizado.

**La inversión inicial compra más capacidad de la que exige la meta del plan.** El plan de negocios fija como meta de largo plazo 5,000 aves (ver [Resumen ejecutivo](../business-plan/01-resumen-ejecutivo.md)). Según el proveedor, la infraestructura compartida de alimentación y recolección de huevo de esta misma cotización admite hasta **90 "grupos de jaula" (≈11,520 aves)** sin necesitar un segundo sistema compartido completo. Es decir: el crédito de esta primera unidad no sólo cubre el punto de partida (640 aves), sino que compra headroom de infraestructura compartida por encima de la meta completa de 5,000 aves — un argumento a favor de la eficiencia de esta inversión frente a un financiador. (Cifra declarada por el proveedor para una nave de referencia de 120 m; no verificada aún para nuestra nave específica de 17 m/5 sets — ver [Modelo modular de crecimiento — 6.2](../business-plan/06-crecimiento-modular.md#62-escala-recomendada) y el pendiente en el [registro de cotizaciones](../../evidence/quotations/README.md#pendientes-con-este-proveedor).)

## 2. Por qué 640 y no 100

Las primeras versiones del plan de negocios ([Resumen ejecutivo](../business-plan/01-resumen-ejecutivo.md), [DEC-003](../governance/registro-de-decisiones.md#dec-003--inicio-controlado-con-una-operación-piloto-de-aproximadamente-100-gallinas)) usaban una cifra de referencia de 96–120 aves, estimada antes de tener una cotización real de proveedor. Al recibir la cotización de FamTECH, quedó claro que la unidad mínima que realmente se construye y se financia —la nave completa de 5 sets tipo H— aloja 640 aves, no ~100. Diseñar el expediente de financiamiento sobre una cifra hipotética distinta a lo que efectivamente se compra habría generado inconsistencias entre este documento, el plan de negocios y el diseño físico.

La lógica original (empezar con una escala controlada, validar antes de crecer, no exigir recuperación inmediata del CAPEX) se conserva íntegra; solo cambia el número de aves. Ver [Validación del piloto](../business-plan/18-validacion-del-piloto.md) para el desarrollo completo de esa lógica a la escala ya congelada de 640 aves.

## 3. Inversión inicial (CAPEX)

**Corrección (2026-09-14):** el proveedor aclaró el 2026-08-03 que los $17,747 USD entregan sólo hasta un almacén en la ciudad de Puebla, no hasta el sitio del proyecto. El flete final (Puebla → San Francisco Acatepec) es una partida aparte, todavía sin cotizar.

| Concepto | Estado | Rango estimado MXN |
| --- | --- | ---: |
| Jaula automatizada tipo H (5 sets, 4 niveles) + alimentación + bebederos + recolección de huevo + retiro de gallinaza, entregado en ciudad de Puebla | Sustituido por cotización real (FamTECH v1/v2, USD $17,747) | $328,300 *(fijo)* |
| Flete final: ciudad de Puebla → sitio del proyecto | Pendiente — no incluido en la cotización, sin cotizar | Sin cotizar |
| Obra civil (nave 17×4×4.2 m) | Recalculado por huella de la nave; sin cotización formal | $227,000–$421,000 |
| Agua: tanque, tratamiento y medición adicional | Recalculado; sin cotización formal | $20,000–$45,000 |
| Controlador, sensores y comunicaciones (capa NidoSmart) | Conservado — no escala con el número de aves | $25,000–$65,000 |
| Conectividad a internet y respaldo satelital | Conservado — no depende de la escala de aves | $8,000–$25,000 |
| UPS y respaldo energético | Recalculado por mayor carga eléctrica; sin estudio de carga formal | $90,000–$220,000 |
| Bioseguridad y contingencias | Conservado, ajuste menor | $25,000–$70,000 |
| **Total (piso; excluye flete final, aún sin cotizar)** | | **$723,300–$1,174,300 + flete final pendiente** |

Desarrollo completo, metodología y tipo de cambio de referencia en [Plan financiero — 17.1 Inversión inicial](../business-plan/17-plan-financiero.md#171-inversión-inicial).

**Partida opcional en pausa:** control ambiental (ventiladores, cooling pads, sensores) — cotización FamTECH v3, USD $6,348 adicionales (≈$117,400 MXN) sobre la jaula base. Se decidió no incluirla hasta definir el diseño de la nave (ver [decisión vigente](../../evidence/quotations/README.md#decisión-vigente-2026-07-22)).

## 4. Lo que el crédito NO cubre

Terreno, vehículo, impuestos, permisos locales, estudios ambientales, obra mayor, conexión eléctrica especial, pozo y mano de obra permanente quedan fuera del alcance de esta inversión (ver [Plan financiero](../business-plan/17-plan-financiero.md#171-inversión-inicial)).

## 5. Operación esperada de la unidad congelada

* Producción: ≈192,000–198,400 huevos/año (300–310 huevos/ave/año × 640 aves). Ver [Producción y capacidad comercial](../business-plan/16-produccion-y-capacidad-comercial.md).
* Ingresos año 1 estimados: ≈$824,040 MXN. OPEX año 1 estimado: ≈$785,677 MXN. Flujo antes de CAPEX: ≈$38,363 MXN. Ver [Plan financiero — 17.3](../business-plan/17-plan-financiero.md#173-proyección-preliminar--primera-unidad-640-aves).
* El flujo operativo de la primera unidad **no alcanza a cubrir el CAPEX de una segunda unidad** ($723,300–$1,174,300 MXN, sin contar el flete final). Una segunda unidad es, por diseño, una decisión de financiamiento separada y futura, no una expansión autofinanciada — este es precisamente el motivo de ser de este documento.

## 6. Pendientes antes de formalizar el expediente

* **Cotizar el flete final** de la ciudad de Puebla al sitio del proyecto en San Francisco Acatepec — no incluido en los $17,747 USD ya cotizados (aclarado por el proveedor el 2026-08-03).
* Cotización formal de obra civil para la nave específica (17×4×4.2 m).
* Estudio de carga eléctrica para dimensionar UPS y respaldo energético.
* Confirmación del tipo de cambio vigente al momento de contratar (se usó $18.50 MXN/USD como referencia de trabajo).
* Definir si se incluye o no el paquete de control ambiental antes de solicitar el crédito.
* Identificar el programa de financiamiento aplicable (FIRA, FONAGA u otro — ver [`knowledge-base/financing/`](../../knowledge-base/)) y sus requisitos específicos de expediente.

## Navegación

- [Índice de proyecto de inversión](./README.md)
- [Documento siguiente: Estructura financiera](./02-estructura-financiera.md)
