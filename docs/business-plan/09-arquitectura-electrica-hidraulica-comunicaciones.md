---
title: "Arquitectura eléctrica, hidráulica y de comunicaciones"
project: "NidoSmart"
document_type: "business-plan"
status: "draft"
version: "1.0"
last_updated: "2026-07-25"
---

# Arquitectura eléctrica, hidráulica y de comunicaciones

## 9.1 Sistema eléctrico

La instalación deberá contar con:

* Tablero eléctrico principal.
* Subtablero por módulo.
* Protección contra sobrecorriente.
* Protección contra descargas.
* Puesta a tierra.
* Medición energética por módulo.
* Circuitos separados para cargas críticas.
* Paros de emergencia.
* Contactores y relevadores industriales.
* Variadores para ventiladores cuando sea conveniente.
* UPS para controladores, comunicaciones y sensores.
* Generador o sistema de respaldo para cargas críticas.
* Posibilidad de integrar energía solar posteriormente.

Las cargas críticas son:

* Ventilación mínima.
* Agua.
* Controladores.
* Comunicaciones.
* Alarmas.
* Iluminación básica.

## 9.2 Sistema hidráulico

Se deberá instalar:

* Tanque pulmón.
* Bomba principal.
* Bomba o mecanismo de respaldo.
* Manifold con salida independiente para cada módulo.
* Medidor por módulo.
* Filtros.
* Reguladores.
* Válvulas de aislamiento.
* Puntos de muestreo.
* Drenajes y purgas.
* Sensor de presión.

**Parámetros de calidad de agua a verificar (revisión julio 2026):** antes de construir, el agua del predio (pozo o red municipal) debe analizarse contra los umbrales de referencia de la industria (Bell & Weaver, capítulo 22): pH 6.5–8.0 (ideal 7.0–7.2), dureza máxima 100 ppm, hierro y manganeso máximo 0.3 ppm cada uno, nitratos máximo 20 ppm, sodio máximo 20 ppm, y **0 UFC/mL de bacterias coliformes** (cualquier presencia indica contaminación fecal y riesgo sanitario). Pendiente: realizar un análisis de agua del predio y definir tratamiento si no cumple estos parámetros.

## 9.3 Comunicaciones

La arquitectura recomendada es:

* Ethernet industrial como medio principal.
* Wi-Fi sólo para dispositivos no críticos.
* MQTT para telemetría.
* Modbus TCP o RTU para equipos industriales.
* Red separada para control.
* Red separada para administración e internet.
* VPN para acceso remoto.
* Grabación local de cámaras.
* Red de control con operación local autónoma durante fallas de internet (agua, ventilación, alarmas).

### 9.3.1 Conectividad a internet como requisito permanente

La granja generará datos de forma continua para su análisis y operación asistida por Hermes Agent y, en etapas posteriores, por Paperclip. Por ello, la conectividad a internet deja de ser un elemento opcional y se convierte en un requisito permanente de la capa de datos e inteligencia:

* Enlace primario de banda ancha fija (fibra, cable o equivalente disponible en el predio).
* Enlace satelital de respaldo, como **Starlink u otra tecnología equivalente**, para garantizar continuidad cuando falle el enlace primario.
* En módulos o ubicaciones futuras instaladas en zonas remotas sin cobertura de banda ancha fija, Starlink u otra tecnología satelital podrá utilizarse como enlace principal.
* Monitoreo del estado del enlace de internet como una variable operativa más, con alerta cuando se pierda conectividad.
* Buffer local de datos en el gateway y la base de datos local durante interrupciones de internet, para sincronizar la información con Hermes Agent, Paperclip y los paneles remotos en cuanto se restablezca la conexión.

Esta dependencia de internet aplica a la capa de datos, análisis, IA y monitoreo remoto. **No aplica al control crítico**, que debe seguir funcionando de forma local y autónoma a través del PLC, conforme al principio establecido en [Arquitectura tecnológica — Principio fundamental](./10-arquitectura-tecnologica.md#101-principio-fundamental).

---

## Navegación

- [Índice general](./README.md)
- [Documento anterior: Sistema de automatización](./08-automatizacion.md)
- [Documento siguiente: Arquitectura tecnológica](./10-arquitectura-tecnologica.md)
