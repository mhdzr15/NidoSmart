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
* Dos fuentes de agua independientes cuando el predio lo permita (p. ej. pozo + red municipal, o dos pozos) — la redundancia de bomba sobre una sola fuente no cubre el caso de falla de la fuente misma.
* Manifold con salida independiente para cada módulo.
* Medidor por módulo.
* Filtros, instalados antes de la línea de bebederos para excluir partículas.
* Reguladores de presión, con línea de bebederos nivelada para evitar bloqueos de aire.
* Válvulas de aislamiento.
* Puntos de muestreo.
* Drenajes y purgas.
* Sensor de presión.

**Dimensionamiento de referencia (revisión septiembre 2026, cálculo propio a partir de Bell & Weaver, cap. 22, tablas 22-3/22-4 — Universidad de California, 1997, 167 parvadas):** el consumo de agua de gallinas ponedoras en el rango de temperatura interior esperado del sitio (19.7–28°C) es de **18.7–21.4 L/100 aves/día**, equivalente a **≈120–140 L/día para las 640 aves** de la unidad actual. Siguiendo la práctica de la industria de mantener al menos 2 días de reserva en sitio, el tanque pulmón debe cubrir como mínimo **≈250–280 L**; con margen de limpieza y redundancia se recomienda un piso de diseño de **≥500 L útiles**. Esta cifra es una estimación propia, no una cotización, y debe ajustarse cuando se confirme el ratio real de níples por ave con el proveedor.

**Parámetros de calidad de agua a verificar (revisión julio 2026; reconciliado septiembre 2026):** antes de construir, el agua del predio (pozo o red municipal) debe analizarse. Existen dos referencias con valores distintos, que deben citarse ambas:

* **NOM-127-SSA1-1994** (piso regulatorio oficial, usada por el Manual de Buenas Prácticas Pecuarias en la Producción de Huevo para Plato, `knowledge-base/regulations/buenas-practicas-huevo.pdf`, anexo): ausencia de coliformes totales y de E. coli/coliformes fecales; dureza total máxima 500 ppm (como CaCO₃); hierro máximo 0.3 ppm; nitratos máximo 10 ppm (como N); sodio máximo 200 ppm.
* **Bell & Weaver, capítulo 22** (objetivo de desempeño productivo, más estricto que el piso legal en varios parámetros): pH 6.5–8.0 (ideal 7.0–7.2), dureza máxima 100 ppm, hierro y manganeso máximo 0.3 ppm cada uno, nitratos máximo 20 ppm, sodio máximo 20 ppm, y **0 UFC/mL de bacterias coliformes** (cualquier presencia indica contaminación fecal y riesgo sanitario).

Las dos fuentes coinciden en hierro y en exigir ausencia de coliformes, pero difieren de forma importante en dureza (100 vs. 500 ppm), sodio (20 vs. 200 ppm) y en la base de medición de nitratos (NOM-127 mide como N). NOM-127 es el requisito legal aplicable; los valores de Bell & Weaver son un objetivo de calidad productiva (dureza y sodio afectan la incrustación de los níples y el desempeño de las aves, no solo la inocuidad), y se adoptan como meta de diseño cuando sea alcanzable, sin sustituir el cumplimiento de NOM-127. Pendiente: realizar un análisis de agua del predio y definir tratamiento si no cumple estos parámetros.

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
