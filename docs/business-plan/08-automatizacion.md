---
title: "Sistema de automatización"
project: "NidoSmart"
document_type: "business-plan"
status: "draft"
version: "1.0"
last_updated: "2026-07-25"
---

# Sistema de automatización

## 8.1 Procesos que deben automatizarse desde el inicio

### Alimentación

El sistema deberá incluir:

* Tolva o hopper.
* Línea de tornillo sinfín, cadena o mecanismo equivalente.
* Programación por horarios.
* Sensores de nivel.
* Medición del consumo del motor.
* Alarma por atasco o falta de alimento.
* Posibilidad de operación manual de emergencia.

**Especificación objetivo (revisión julio 2026):** la industria recomienda un espacio de comedero de referencia de **10 cm por ave** (mínimo según línea genética: 7.6–8.4 cm/ave), con jaulas más anchas y menos profundas mostrando consistentemente mejor desempeño que jaulas angostas y profundas (Bell & Weaver, tablas 52-1, 52-6 y 52-7). Pendiente confirmar con el proveedor de jaulas el espacio de comedero lineal por ave de su set tipo H.

### Agua

El sistema deberá incluir:

* Tanque de reserva.
* Filtrado.
* Regulador de presión.
* Medidor de caudal.
* Línea de bebederos tipo nipple.
* Sensor de nivel.
* Alarma por fuga.
* Alarma por ausencia de consumo.
* Válvula de corte.
* Punto de dosificación o medicación controlada.

**Especificación objetivo (revisión julio 2026):** la industria recomienda entre **6 y 8 aves por níple** según línea genética (Bell & Weaver, tabla 52-1). Pendiente confirmar con el proveedor el ratio de níples por ave de su sistema de bebederos automáticos. Los parámetros de calidad del agua a verificar en el predio se detallan en [Arquitectura eléctrica, hidráulica y de comunicaciones — Sistema hidráulico](./09-arquitectura-electrica-hidraulica-comunicaciones.md#92-sistema-hidráulico).

### Iluminación

El sistema deberá permitir:

* Programación de fotoperiodo.
* Encendido y apagado gradual.
* Regulación de intensidad.
* Respaldo ante interrupciones eléctricas.
* Registro de horas efectivas de iluminación.
* Operación manual local.

**Programa objetivo (revisión julio 2026):** la industria recomienda un fotoperiodo de pico de **14 horas de luz**, que durante la postura solo debe aumentar, nunca disminuir. En la etapa de pollita el programa típico es de escalón descendente (23 horas el día 1, reduciéndose gradualmente hasta ~8 horas en la madurez), seguido de un escalón ascendente hasta las 14 horas al alcanzar el peso de madurez sexual (Bell & Weaver, capítulo 10). La intensidad de referencia es de **0.5 candelas-pie (5 lux)**, suficiente para ponedoras, pero en sistemas de jaula de 4 niveles la iluminación puede variar 4–5 veces entre el nivel superior y el inferior — por lo que el nivel más bajo debe garantizar ese mínimo. Pendiente confirmar con el proveedor el diseño de luminarias (cantidad y distribución) para el sistema de 4 niveles cotizado.

### Control ambiental

Variables mínimas:

* Temperatura.
* Humedad relativa.
* Concentración de CO₂.
* Concentración de amoníaco.
* Estado de ventiladores.
* Flujo de aire cuando sea técnicamente viable.
* Consumo eléctrico.
* Estado de puertas.
* Presencia de humo o incendio.

Actuadores:

* Ventiladores.
* Entradas de aire.
* Extractores.
* Equipos de recirculación.
* Enfriamiento evaporativo cuando el clima lo requiera.
* Calefacción auxiliar cuando sea necesaria.
* Alarmas sonoras y remotas.

**Umbrales objetivo (revisión julio 2026):** ventilación mínima de referencia de **1.5 cfm por libra de peso vivo del ave** en clima frío (reducible a ~0.5 cfm/libra si existe sistema de enfriamiento tipo túnel para el verano), y disparo de mayor ventilación cuando el amoníaco supere **30 ppm** (Bell & Weaver, capítulo 9). Ver también la nota sobre aislamiento térmico vs. calefacción auxiliar en [Diseño físico preliminar — Condiciones climáticas del sitio](./07-diseno-fisico.md#condiciones-climáticas-del-sitio).

### Recolección de huevo

Para 100 aves se recomienda:

* Banda corta.
* Transporte hasta una mesa final.
* Sensor de operación.
* Conteo aproximado o cámara.
* Paro por obstrucción.
* Inspección y empaque manual.

No se recomienda comenzar con una clasificadora industrial de alta capacidad — este tipo de equipo (hasta 140,000 huevos/hora) solo se justifica económicamente a escala de aproximadamente un millón de aves (Bell & Weaver, capítulo 50), muy por encima de cualquier etapa de la [hoja de ruta de crecimiento](./06-crecimiento-modular.md#62-escala-recomendada) de NidoSmart.

**Frecuencia objetivo (revisión julio 2026):** recolectar el huevo **al menos dos veces al día**. La industria documenta que pasar de una a dos recolecciones diarias reduce el quiebre de huevo de aproximadamente 5.6% a 4.0% (Bell & Weaver, capítulo 56), al disminuir el tiempo de acumulación y las colisiones entre huevos en la banda.

### Retiro de gallinaza

El módulo deberá integrar:

* Banda o sistema mecanizado.
* Operación programada.
* Sensor de motor.
* Contenedor cerrado.
* Traslado a zona separada de compostaje.
* Registro de cada retiro.

## 8.2 Procesos que pueden permanecer manuales inicialmente

* Inspección visual de las aves.
* Retiro de mortalidades.
* Clasificación final del huevo.
* Empaque.
* Limpieza profunda.
* Mantenimiento físico.
* Aplicación veterinaria.
* Control de visitantes.
* Revisión de plagas.
* Reposición de consumibles.

La automatización no elimina la necesidad de inspección diaria. Una granja con 90% de automatización aún requiere presencia humana para bienestar, sanidad y mantenimiento.

---

## Navegación

- [Índice general](./README.md)
- [Documento anterior: Diseño físico preliminar](./07-diseno-fisico.md)
- [Documento siguiente: Arquitectura eléctrica, hidráulica y de comunicaciones](./09-arquitectura-electrica-hidraulica-comunicaciones.md)
