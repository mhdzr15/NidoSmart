---
title: "Ficha técnica — Nave avícola (unidad de 640 aves)"
project: "NidoSmart"
document_type: "investment-project"
status: "draft"
version: "1.0"
last_updated: "2026-09-14"
---

# Ficha técnica — Nave avícola (unidad de 640 aves)

Este documento existe para cumplir una condición explícita: **no deben solicitarse cotizaciones formales de obra civil para la nave hasta contar con una ficha técnica suficientemente estable** que permita comparar propuestas equivalentes entre distintos contratistas. Hoy esa condición **todavía no se cumple** — ver [Estado de la ficha](#estado-de-la-ficha-técnica) al final.

La nave aloja la unidad congelada de 640 aves ([DEC-012](../governance/registro-de-decisiones.md#dec-012--congelamiento-del-alcance-de-la-inversión-inicial-en-una-unidad-productiva-de-640-aves)): jaula automatizada tipo H, 5 sets, 4 niveles (ver [Diseño físico — 7.1](../business-plan/07-diseno-fisico.md#71-módulo-inicial)).

## Parámetros técnicos

| Parámetro | Especificación | Estado | Fuente / nota |
|---|---|---|---|
| Dimensiones finales | 17 × 4 × 4.2 m (≈68 m² de huella) | **Confirmado** | Cotización FamTECH v1/v2, texto literal: "Advised chicken coop size: 17m×4m×4.2m" |
| Capacidad productiva soportada | 640 aves (5 sets × 128 aves, 4 niveles) | **Confirmado** | Misma cotización; equivalencia set=grupo=128 aves confirmada por el proveedor por escrito (2026-07-23) |
| Tipo estructural | Sin definir | **Pendiente** | No hay decisión entre estructura metálica prefabricada, estructura regional (block/columna de concreto) o híbrida. Es una decisión de NidoSmart, no del proveedor de jaula. |
| Materiales (muros, marco) | Sin definir | **Pendiente** | Depende del tipo estructural anterior. |
| Altura libre | 4.2 m de altura total de nave; altura libre bajo estructura/techo para instalación de jaula de 4 niveles no verificada | **Pendiente** | La cotización da altura total, no altura libre útil descontando pendiente de techo, vigas o ductos. Debe confirmarse que 4.2 m es suficiente para el sistema de 4 niveles más espacio de mantenimiento superior. |
| Orientación | Sin definir | **Pendiente** | Debe definirse en función de asoleamiento y vientos dominantes del predio en San Francisco Acatepec; no hay estudio de sitio. |
| Aislamiento térmico requerido | R-20 techo / R-14 paredes (referencia para ΔT interior/exterior > 28 °C) | **Estimado** (estándar de industria, no cotización) | Bell & Weaver, *Commercial Chicken Meat and Egg Production*; ver [Diseño físico — Condiciones climáticas del sitio](../business-plan/07-diseno-fisico.md#condiciones-climáticas-del-sitio). Pendiente confirmar con el proveedor de obra civil qué aislamiento realmente ofrece su propuesta. |
| Ventilación (tasa mínima) | 1.5 cfm/libra de peso vivo en clima frío; hasta 0.5 cfm/libra con enfriamiento tipo túnel en verano | **Estimado** (estándar de industria) | Bell & Weaver, cap. 9; ver [Automatización — Control ambiental](../business-plan/08-automatizacion.md#control-ambiental). No hay cálculo de cfm real para 640 aves ni selección de equipo. |
| Entradas y salidas de aire | Sin definir | **Pendiente** | La cotización v3 (control ambiental, USD $24,095) incluye "ventanas de entrada de aire" pero esa partida está en pausa (ver [decisión vigente](../../evidence/quotations/README.md#decisión-vigente-2026-07-22)); no hay diseño de aberturas si se construye sin ese paquete. |
| Cubierta | Sin definir | **Pendiente** | Debe soportar granizo (ver clima del sitio) y alojar el aislamiento térmico anterior; no hay material ni calibre propuesto. |
| Muros o cerramientos | Sin definir | **Pendiente** | Depende del tipo estructural; debe permitir bioseguridad (barrera física, control de fauna) y ventilación controlada simultáneamente. |
| Drenaje | Sin definir | **Pendiente** | Solo existe el requisito general "buen drenaje pluvial" ([Diseño físico — Condiciones climáticas](../business-plan/07-diseno-fisico.md#condiciones-climáticas-del-sitio)); no hay pendientes, canaletas ni capacidad de desalojo calculadas. |
| Resistencia a viento y clima local | Sin definir | **Pendiente** | Requiere memoria de cálculo estructural conforme al reglamento de construcción aplicable en San Andrés Cholula, Puebla, con cargas de viento y granizo del sitio. No existe todavía; se requiere un ingeniero civil o DRO local. |
| Piso | Sin definir (se asume firme de concreto) | **Pendiente** | No hay espesor, resistencia ni acabado especificados; tampoco se ha confirmado la carga puntual de las patas de la jaula de 4 niveles sobre el firme. |
| Integración con jaulas tipo H | Parcial | **Pendiente** | Las dimensiones de la nave coinciden con las de la cotización de jaula, pero no hay plano de anclajes, cargas puntuales de la estructura de jaula sobre el firme, ni interfaz mecánica/eléctrica entre ambos proveedores (jaula vs. obra civil). |
| Espacios de servicio | Conceptual | **Pendiente** | [Diseño físico — 7.2](../business-plan/07-diseno-fisico.md#72-áreas-generales-del-predio) lista filtro sanitario, cuarto técnico, almacén de alimento, área de empaque, etc., pero sin metros cuadrados ni ubicación relativa a la nave de 640 aves. |
| Accesos | Sin definir | **Pendiente** | No hay definición de accesos vehiculares/peatonales ni su relación con el filtro sanitario. |
| Bioseguridad (perímetro físico) | Conceptual | **Pendiente** | [Bioseguridad — 19.1](../business-plan/20-bioseguridad.md#191-medidas-mínimas) lista requisitos, pero no hay layout físico del perímetro, cercado o entrada única aplicado a este predio y esta nave. |
| Expansión futura | Parcial, con advertencia | **Pendiente** | El proveedor declara headroom compartido de hasta 90 "grupos" (≈11,520 aves) en una nave de referencia de 120 m, proporción que no coincide con la nave de 17 m/5 sets de NidoSmart — ver [registro de cotizaciones — pendientes](../../evidence/quotations/README.md#pendientes-con-este-proveedor). La nave física debe diseñarse sabiendo si permite o no ampliarse linealmente sin reconstruir cimentación. |
| Instalaciones eléctricas e hidráulicas asociadas | Conceptual | **Pendiente** | [Arquitectura eléctrica/hidráulica — 9.1/9.2](../business-plan/09-arquitectura-electrica-hidraulica-comunicaciones.md) define requisitos funcionales, pero no hay estudio de carga eléctrica ni dimensionamiento hidráulico específico para esta nave (mismo pendiente ya señalado en [Plan financiero — 17.1](../business-plan/17-plan-financiero.md#171-inversión-inicial) para el UPS). |

## Estado de la ficha técnica

De 19 parámetros: **2 confirmados**, **2 estimados** (a partir de estándares de industria, no de cotización), **15 pendientes** sin dato ni decisión.

**Conclusión:** la ficha técnica de la nave *no* está lo suficientemente estable para solicitar cotizaciones formales de obra civil comparables entre sí. Antes de cotizar, deben cerrarse al menos estos pendientes críticos:

1. Definir tipo estructural y materiales (decisión propia de NidoSmart — no depende de terceros).
2. Contratar o consultar a un ingeniero civil/DRO local para las cargas de viento, granizo y la memoria estructural conforme al reglamento de San Andrés Cholula.
3. Levantar un estudio de sitio mínimo (orientación, vientos dominantes, drenaje pluvial) en el predio de San Francisco Acatepec.
4. Confirmar con el proveedor de jaula (FamTECH) la altura libre útil requerida por el sistema de 4 niveles y las cargas puntuales de la estructura de jaula sobre el firme.
5. Asignar metros cuadrados y ubicación relativa a los espacios de servicio ya listados conceptualmente (filtro sanitario, cuarto técnico, almacén, empaque).
6. Realizar el estudio de carga eléctrica pendiente (ya señalado en el plan financiero) para poder especificar la instalación eléctrica de la nave, no solo el respaldo (UPS).

Hasta que estos puntos se resuelvan, cualquier cifra de obra civil en el [presupuesto consolidado](./07-presupuesto-consolidado-inversion-inicial.md) sigue siendo una **estimación por huella** (m² × costo/m² de referencia), no una cotización comparable.

## Navegación

- [Índice de proyecto de inversión](./README.md)
- [Documento anterior: Proyecto de inversión](./01-proyecto-de-inversion.md)
- [Documento siguiente: Vehículo de distribución](./06-vehiculo-de-distribucion.md)
