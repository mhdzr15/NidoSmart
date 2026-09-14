---
title: "Resumen ejecutivo"
project: "NidoSmart"
document_type: "business-plan"
status: "draft"
version: "1.3"
last_updated: "2026-09-14"
---

# Resumen ejecutivo

**Versión:** 1.1
**Fecha:** Julio de 2026
**Ubicación inicial:** San Francisco Acatepec, municipio de San Andrés Cholula, Puebla
**Etapa inicial:** 640 gallinas ponedoras (primera unidad productiva financiable)
**Escala de diseño inicial:** 640 aves construidas; servicios compartidos con margen para 1,280 aves (segunda unidad)
**Escala objetivo de largo plazo:** 5,000 aves (≈8 unidades de 640)
**Techo de capacidad declarado por el proveedor:** ≈11,520 aves (90 "grupos" de 128 aves), usando la misma infraestructura compartida de alimentación y recolección de huevo ya cotizada en la primera unidad — por encima de la meta de 5,000 aves del plan (ver [Modelo modular de crecimiento — 6.2](./06-crecimiento-modular.md#62-escala-recomendada); cifra declarada por el proveedor, no verificada aún punto por punto para nuestra nave específica)

El proyecto propone desarrollar una granja de gallinas ponedoras en **San Francisco Acatepec, municipio de San Andrés Cholula, Puebla**, basada en tres principios:

1. **Inicio controlado:** comenzar con una primera unidad productiva de 640 gallinas —el tamaño real definido por la cotización vigente de jaula automatizada tipo H (ver [Diseño físico](./07-diseno-fisico.md))— para adquirir experiencia técnica, sanitaria, operativa y comercial sin asumir el riesgo de una explotación de miles de aves.
2. **Automatización intensiva:** automatizar más del 90% de las operaciones repetitivas, incluyendo alimentación, agua, iluminación, ventilación, control ambiental, recolección de huevo, retiro de gallinaza, monitoreo y generación de alertas.
3. **Crecimiento modular:** construir la infraestructura como una plataforma que pueda ampliarse por módulos independientes, evitando rediseñar completamente la granja cada vez que aumente el número de aves.

La recomendación es comenzar con **gallinas ponedoras y no con pollo de engorda**. Las ponedoras ofrecen flujo de ingresos diario, permiten validar gradualmente el canal comercial y tienen menores necesidades de procesamiento y sacrificio. También permiten corregir rápidamente problemas de precio, calidad, empaque, distribución y productividad.

El módulo inicial (primera unidad financiable) aloja **640 aves** en una nave de 17×4×4.2 m con jaula automatizada tipo H de 4 niveles (5 sets), conforme a la cotización vigente del proveedor (ver [registro de cotizaciones](../../evidence/quotations/README.md)). Los servicios compartidos —electricidad, agua, comunicaciones, control ambiental, almacenamiento, empaque y respaldo energético— deberán dimensionarse con margen para una **segunda unidad de 640 aves (1,280 aves en total)**, de manera que el segundo módulo pueda conectarse sin sustituir la infraestructura principal.

La estrategia comercial no debe basarse en competir con productores industriales mediante precio y volumen. A una escala pequeña, el negocio depende de:

* Venta directa.
* Entrega a domicilio.
* Suscripciones semanales.
* Restaurantes y pequeños negocios.
* Tiendas especializadas.
* Diferenciación por frescura, trazabilidad y producción local.

La inversión preliminar para la primera unidad automatizada de 640 aves se estima entre **$723,300 y $1,174,300 MXN**, sin considerar terreno *(cifra recalculada julio–septiembre 2026 a partir de la cotización real de jaula y automatización; ver el desglose completo en [Plan financiero — 17.1 Inversión inicial](./17-plan-financiero.md#171-inversión-inicial))*. El rango depende principalmente del nivel de automatización, condiciones climáticas, obra civil, respaldo energético, conectividad a internet (incluyendo respaldo satelital) y origen de los equipos.

Una instalación altamente automatizada no tendrá una recuperación rápida si permanece indefinidamente en 640 gallinas. El primer módulo debe entenderse como una fase de validación que genera:

* Experiencia productiva.
* Información real de costos.
* Un canal comercial probado.
* Procedimientos operativos.
* Datos para ajustar la automatización.
* Infraestructura reutilizable para el crecimiento.

En la arquitectura digital, la recomendación es utilizar:

* **PLC o controlador avícola** para el control determinista y crítico.
* **Gateway industrial y Node-RED** para integrar sensores, equipos y comunicaciones.
* **Base de datos local de series de tiempo** para históricos de producción y ambiente.
* **Hermes Agent** como asistente inteligente local para análisis, alertas, documentación y operación asistida.
* **Paperclip** en una etapa posterior, cuando el negocio necesite coordinar varios agentes, módulos, áreas administrativas o ubicaciones.

---

## Navegación

- [Índice general](./README.md)
- [Documento siguiente: Descripción del negocio](./02-descripcion-del-negocio.md)
