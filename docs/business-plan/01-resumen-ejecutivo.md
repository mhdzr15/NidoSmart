---
title: "Resumen ejecutivo"
project: "NidoSmart"
document_type: "business-plan"
status: "draft"
version: "1.1"
last_updated: "2026-07-12"
source: "NidoSmartBP.md"
---

# Resumen ejecutivo

**Versión:** 1.1
**Fecha:** Julio de 2026
**Ubicación inicial:** San Francisco Acatepec, municipio de San Andrés Cholula, Puebla
**Etapa inicial:** 100 gallinas ponedoras
**Escala de diseño inicial:** 300 aves
**Escala objetivo de largo plazo:** 5,000 aves

El proyecto propone desarrollar una granja de gallinas ponedoras en **San Francisco Acatepec, municipio de San Andrés Cholula, Puebla**, basada en tres principios:

1. **Inicio controlado:** comenzar con aproximadamente 100 gallinas para adquirir experiencia técnica, sanitaria, operativa y comercial sin asumir el riesgo de una explotación de miles de aves.
2. **Automatización intensiva:** automatizar más del 90% de las operaciones repetitivas, incluyendo alimentación, agua, iluminación, ventilación, control ambiental, recolección de huevo, retiro de gallinaza, monitoreo y generación de alertas.
3. **Crecimiento modular:** construir la infraestructura como una plataforma que pueda ampliarse por módulos independientes, evitando rediseñar completamente la granja cada vez que aumente el número de aves.

La recomendación es comenzar con **gallinas ponedoras y no con pollo de engorda**. Las ponedoras ofrecen flujo de ingresos diario, permiten validar gradualmente el canal comercial y tienen menores necesidades de procesamiento y sacrificio. También permiten corregir rápidamente problemas de precio, calidad, empaque, distribución y productividad.

El módulo inicial deberá alojar entre **96 y 120 aves**, pero los servicios compartidos —electricidad, agua, comunicaciones, control ambiental, almacenamiento, empaque y respaldo energético— deberán dimensionarse para aproximadamente **300 aves**. De esta manera, el segundo y tercer módulo podrán conectarse sin sustituir la infraestructura principal.

La estrategia comercial no debe basarse en competir con productores industriales mediante precio y volumen. A una escala pequeña, el negocio depende de:

* Venta directa.
* Entrega a domicilio.
* Suscripciones semanales.
* Restaurantes y pequeños negocios.
* Tiendas especializadas.
* Diferenciación por frescura, trazabilidad y producción local.

La inversión preliminar para un módulo automatizado de 100 aves se estima entre **$334,000 y $765,000 MXN**, sin considerar terreno. El rango depende principalmente del nivel de automatización, condiciones climáticas, obra civil, respaldo energético, conectividad a internet (incluyendo respaldo satelital) y origen de los equipos.

Una instalación altamente automatizada no tendrá una recuperación rápida si permanece indefinidamente en 100 gallinas. El primer módulo debe entenderse como una fase de validación que genera:

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
