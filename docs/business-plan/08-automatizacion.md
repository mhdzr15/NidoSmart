---
title: "Sistema de automatización"
project: "NidoSmart"
document_type: "business-plan"
status: "draft"
version: "1.1"
last_updated: "2026-09-13"
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

**Especificación de iluminación (revisión septiembre 2026 — reemplaza la nota de julio 2026):** revisión completa con la guía de manejo Hy-Line W-80, el boletín técnico Hy-Line "Entendiendo la Luz en la Avicultura", Bell & Weaver (cap. 8, 9, 10, 52) y documentación pública de otros fabricantes de jaula tipo H (aplicado el criterio de revisar fuentes de industria ya documentadas antes de generar preguntas nuevas a FamTECH).

**Principio confirmado sobre el alcance de FamTECH:** la cotización cubre únicamente el equipo listado línea por línea. Luminarias, tragaluces, cortinas y sensores de luz son partidas separadas de otros proveedores, no de FamTECH.

*Fotoperiodo (confirmado, Hy-Line W-80 — reemplaza la cifra genérica de 14 h):* nave de tipo "brown-out" (Bell & Weaver) — cerrada por el aislamiento ya decidido, con tragaluces controlados (ver abajo). Programa de galpón de luz controlada: inicia ~10 h a la llegada del lote (16–18 semanas) y aumenta gradualmente hasta **15–16 horas** hacia la semana 25–35, sin disminuir nunca.

*Intensidad y espectro (confirmado, dos fuentes independientes coinciden):*

| Nivel | Valor | Fuente |
|---|---|---|
| Piso absoluto (nunca menos) | 5 lux (0.5 fc) | Bell & Weaver cap. 52 y boletín Hy-Line |
| Mínimo aceptable en el punto peor iluminado | 15–20 lux | Hy-Line W-80 (guía de manejo) y fabricantes de jaula tipo H |
| Objetivo de diseño (canal de alimento) | 30 lux (3 fc) | Hy-Line, boletín técnico; confirmado por fabricantes de jaula tipo H |
| Techo (evitar superar) | 50 lux (5 fc) — riesgo de nerviosismo/picaje | Hy-Line, boletín técnico |
| Espectro | Cálido, rico en rojo, 2700–3000 K | Hy-Line |

*Ubicación de luminarias — resuelto por el propio diseño de jaula tipo H:* tira LED montada en el marco de la jaula, **una por cada uno de los 4 niveles**, corriendo a lo largo de la fila. Es el diseño estándar de la industria para jaula tipo H (confirmado en el sistema de FamTECH y en documentación pública de otros fabricantes del mismo tipo de jaula) y resuelve por diseño estructural la variación de 4–5 veces entre nivel superior e inferior que documenta Bell & Weaver para sistemas sin tira por nivel — no requiere un arreglo adicional de luminarias en el pasillo.

*Tragaluces y cortina de blackout (complemento de ahorro energético, materiales locales — no corrige uniformidad, eso ya lo resuelve la tira por nivel):* lámina traslúcida corrugada de fibra de vidrio o policarbonato (producto estándar de proveedores de materiales para naves industriales/agrícolas en México) en 2–5% del área de techo, distribuida a lo largo de los 17 m — estimación de práctica general de diseño, a validar. Cortina interior opaca tipo invernadero (lona/tela blackout), operada con motorreductor + torno del mismo tipo ya cotizado por FamTECH para las ventanas de entrada de aire. Blackout total obligatorio durante las horas oscuras del fotoperiodo, sincronizado con el mismo controlador — un "brown-out" mal sellado sigue siendo influenciado por luz exterior y arriesga el programa de fotoperiodo (Bell & Weaver).

*Control adaptativo por nivel (decisión de diseño, 2026-09-17):* 4 sensores de lux (uno por nivel, medidos sobre el canal de alimento), con la lógica de control en el **PLC/controlador propio de NidoSmart** (consistente con DEC-007 — control crítico local y autónomo, no depende de revivir el paquete ambiental pausado de FamTECH). Cada sensor mide lux total (natural + LED combinado); si la lectura ya alcanza el objetivo solo con luz natural del tragaluz, el LED de ese nivel se apaga o atenúa; si cae por debajo del mínimo, el LED se enciende o sube hasta compensar. La cortina permanece abierta en horas de luz (salvo cierre parcial si el sensor del nivel superior detecta >50 lux, protegiendo contra nerviosismo/picaje y ganancia solar) y cerrada por completo en horas oscuras. Este control es adaptativo (responde a días nublados o muy soleados), no una regla fija por nivel.

*Protocolo de verificación (comisionamiento):* medir lux sobre el canal de alimento cada 25 cm entre luminarias, en cada uno de los 4 niveles (30–100 lecturas totales) — protocolo de Hy-Line, boletín técnico.

*Tipo de LED:* categoría agrícola general (no la línea específica para avicultura, difícil de conseguir localmente — ver preferencia de materiales locales), regulable con driver compatible, espectro cálido 2700–3000K, material no vidrio (lavable/desinfectable), clasificado para operación continua de 16h/día.

*Respaldo eléctrico (hallazgo — gap identificado):* el presupuesto de UPS (ítem 8, `07-presupuesto-consolidado-inversion-inicial.md`) no incluye explícitamente iluminación entre sus cargas críticas. Pendiente decidir si el circuito de iluminación entra al respaldo; en cualquier caso el controlador requiere reloj de tiempo real (RTC) con respaldo de batería local, independiente de un corte de energía general.

**Pendientes que requiere confirmar FamTECH (reducidos — ya no se pregunta lo que es estándar de industria):**

1. Si la estructura de jaula de nuestro pedido incluye el riel/soporte para tira LED en cada uno de los 4 niveles.
2. Si la tira LED en sí está incluida en el precio del ítem "cage" (III.3) o es partida aparte — no aparece en ninguna versión de la cotización.
3. Especificación eléctrica del riel/conector (voltaje, tipo de conexión) para poder comprar tiras LED compatibles localmente.

**Nuevos proveedores a buscar (locales, no FamTECH):** lámina traslúcida para naves industriales/agrícolas; cortina térmica/blackout de invernadero con motorreductor; tiras LED agrícolas genéricas (2700–3000K, regulables); 4 sensores de lux compatibles con el PLC del proyecto.

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

**Corrección (2026-09-17) — sensores de CO₂ y amoníaco faltantes en el PLC:** hasta ahora, CO₂ y amoníaco solo estaban listados como "variables mínimas" a monitorear, sin un sensor físico asignado. Se confirma que la cotización de FamTECH (v3, controlador YB) **tampoco los incluye** — su paquete de control ambiental trae únicamente 4 sensores de temperatura y 1 de humedad (DMR), ningún sensor de gases. Se agregan explícitamente al PLC propio de NidoSmart (mismo criterio que los sensores de lux — control crítico local, DEC-007; y mismo criterio de materiales locales — sensores de gas genéricos de proveedores de automatización industrial en México, no una línea específica de avicultura):

* **Sensor de amoníaco (NH₃):** obligatorio — es el que dispara el umbral de ventilación de 30 ppm ya establecido; sin sensor físico ese umbral no puede aplicarse.
* **Sensor de CO₂:** obligatorio para cumplir la variable mínima ya listada.

**Umbral de CO₂ — resuelto (2026-09-17, revisión externa):** no se encontró un umbral de CO₂ en la bibliografía local (la única mención en Bell & Weaver, "arriba de 50 ppm", es del capítulo de calidad de carne en el procesamiento de pollo de engorda, un contexto distinto, y el número es numéricamente inconsistente con el CO₂ atmosférico normal — no se usa). Se buscó en fuentes externas: **University of Georgia Cooperative Extension** (boletín "Importance of Adequate Ventilation on Air Quality During Cold Weather", 2003) documenta que una concentración de **12,000 ppm de CO₂ se asocia con reducción de peso corporal** (Reece & Lott, 1980) y que niveles de hasta 10,000 ppm se han observado en casetas de pollo de engorda mal ventiladas durante el precalentamiento — cifras específicas de pollo de engorda, no de ponedoras, pero es la tolerancia fisiológica aviar más citable encontrada. **Recomendación técnica (margen de seguridad, no una norma verificada para ponedoras):** fijar la alarma del sensor en **3,000–5,000 ppm**, muy por debajo del umbral de daño documentado (12,000 ppm), consistente con la práctica general de ingeniería de dejar un margen amplio. El mismo boletín también refina el umbral de amoníaco ya usado en este documento: recomienda mantener NH₃ **por debajo de 25 ppm** (no solo el disparo de ventilación a 30 ppm ya documentado) — se ajusta la alarma del sensor de NH₃ a 25 ppm como el nuevo umbral objetivo, manteniendo 30 ppm como el punto de disparo de ventilación adicional ya establecido por Bell & Weaver.

**Pendiente actualizado en el presupuesto:** el ítem 9 (`07-presupuesto-consolidado-inversion-inicial.md`, "Sensores y control") lista "sensores adicionales" de forma genérica ($25,000–$65,000 MXN, cifra conservada de una versión anterior del plan) — no desglosa NH₃/CO₂ explícitamente. Debe verificarse que el rango sigue siendo suficiente ahora que se confirman estos dos sensores como partidas concretas, no genéricas.

**Revisión septiembre 2026 — estrategia de ventilación (confirmado: no seleccionar modelos comerciales todavía, solo caudales y tipo de sistema):**

*Supuestos (recomendación técnica, no cotización):* ave adulta de 1.7 kg (Hy-Line W-80, rango 1.6–1.74 kg); producción de calor de 40–45 BTU/h/ave (Bell & Weaver, regla práctica); ΔT de diseño en verano de 3–5°F sobre temperatura exterior.

*Caudal mínimo y máximo, expresado como módulo por set (128 aves) para que escale con el crecimiento:*

| | Por set (128 aves) | 5 sets — unidad actual (640 aves) | 90 sets — techo declarado por FamTECH (≈11,520 aves, **no verificado** para nuestra configuración de 17 m/5 sets) |
|---|---|---|---|
| Mínimo (invierno, 1.5 cfm/lb, sistema único todo el año) | ≈720 cfm | ≈3,600 cfm (≈6,100 m³/h) | ≈64,800 cfm (≈110,000 m³/h) |
| Máximo (verano, calor sensible ÷ (1.08×ΔT)) | ≈1,600–1,800 cfm | ≈9,000–10,000 cfm | ≈144,000–162,000 cfm (≈245,000–275,000 m³/h) |

Humedad (Tabla 8-2 de Bell & Weaver, escalada a 640 aves): a 7°C exterior, el lote produce ≈6.9 kg/h de vapor de agua; a 27°C, ≈9.2 kg/h. El mínimo de invierno ya está dimensionado por el método de Bell para remover esta humedad junto con el amoníaco. CO₂ no tiene un umbral específico en la bibliografía local revisada para ponedoras — **pendiente** definirlo con una fuente publicada antes de fijarlo como criterio de diseño.

*Evaluación de sistemas (para la unidad actual de 640 aves / 17 m):*

| Sistema | Veredicto | Razón |
|---|---|---|
| Túnel | Descartado a esta escala | La fórmula de sección transversal × 450 fpm da ≈68,000 cfm, ~7 veces el máximo real necesario (9,000–10,000 cfm); la nave (17 m) es además demasiado corta para desarrollar el efecto de enfriamiento por viento. |
| Transversal / presión negativa | Recomendado — sistema principal | Proporcional al ancho de 4 m; es el diseño estándar de Bell & Weaver para el mínimo de invierno todo el año, y coincide con el manómetro de presión negativa ya incluido en la cotización FamTECH v3. |
| Natural asistida | Solo complemento, no sistema único | Geométricamente viable (4 m « 12 m límite de Poultry Hot Climates), pero ese mismo libro advierte que en sistemas de 4 niveles la ventilación natural se ve impedida cuando el espacio jaula-techo es menor a 1 m — justo el rango ajustado que resultó del análisis de layout (7.1.1). Tampoco da control fiable de humedad/amoníaco en invierno. |
| **Híbrida (recomendada)** | Ventilación mecánica transversal como base permanente todo el año, con las 12 entradas motorizadas ya cotizadas por FamTECH permitiendo aprovechar brisa natural en días templados para ahorrar energía de los extractores. Sin cooling pads (ver abajo) y sin modo túnel a esta escala. | |

**Cooling pads — no se justifican para el alcance inicial:** las máximas del sitio (San Francisco Acatepec) promedian solo ≈23°C en el mes más cálido y rara vez superan 29°C (dato externo, no está en la bibliografía local), lo que confirma la nota ya existente sobre "menor riesgo de estrés calórico" en [Diseño físico — Condiciones climáticas del sitio](./07-diseno-fisico.md#condiciones-climáticas-del-sitio). El enfriamiento evaporativo además pierde eficacia con humedad (temporada de lluvias). Esto refuerza la pausa ya decidida el 2026-07-22 sobre el paquete de control ambiental — pero aísla el problema específicamente en los cooling pads, no en los ventiladores/entradas de aire/controlador, que sí son necesarios (la ventilación mínima no es opcional, ver DEC-006).

**Escalamiento con el crecimiento — corregido ([DEC-014](../governance/registro-de-decisiones.md#dec-014--expansión-lineal-de-la-nave-con-equipo-de-alimentaciónrecolección-compartido-hasta-el-techo-declarado-por-el-proveedor), 2026-09-17):** el crecimiento hacia el techo de 90 sets (~11,520 aves) declarado por FamTECH ocurre **extendiendo linealmente esta misma nave**, con una sola unidad de arrastre de alimentación y recolección de huevo dando servicio a todos los sets. En consecuencia, **la tabla de escalamiento por set de arriba es la hoja de ruta real, no un ejercicio ilustrativo**: el sistema de ventilación de la unidad actual (transversal/presión negativa, 3,600–10,000 cfm, sin cooling pads) es correcto para 5 sets/17 m, pero debe migrarse a modo túnel conforme la nave se alargue hacia el techo declarado (a escala de ~120 m de referencia del proveedor, el túnel se vuelve la opción técnicamente correcta — ver evaluación de sistemas arriba). **Pendiente crítico:** definir en qué umbral de número de sets/longitud conviene hacer esa transición, y confirmar con el proveedor el footprint real por set para saber la longitud final real que implica el techo de 90 sets — sin ese dato no puede fijarse el punto de migración. La cimentación y estructura civil deben planearse extensibles desde el diseño inicial (ver [Ficha técnica — Nave avícola, fila "Expansión futura"](../investment-project/05-ficha-tecnica-nave.md)), aunque solo se construyan los primeros 17 m ahora.

**Pendientes que requieren respuesta de FamTECH:**

1. Curva de desempeño real de los 2 ventiladores de 50"/1.1 kW ya cotizados (cfm a 0", 0.05" y 0.10" de columna de agua) — sin esto no se puede confirmar si están sobrados o justos frente al rango calculado (3,600–10,000 cfm para 640 aves).
2. Si el paquete de control ambiental puede re-cotizarse separando ventiladores + entradas + controlador (de interés) de los cooling pads (no de interés por ahora).
3. Área efectiva de cada una de las 12 entradas de aire CJ01 (para verificar velocidad de entrada contra la Tabla 9-2 de Bell & Weaver).
4. Si el controlador YB permite programar ventilación escalonada (mínimo invierno → máximo verano) o solo operación on/off.
5. **Nuevo:** cuántos sets adicionales admite la MISMA unidad de arrastre de alimentación y recolección de huevo de nuestro pedido (5 sets, 640 aves) antes de requerir un segundo sistema compartido completo — determina si el crecimiento hacia el techo de 90 sets ocurre extendiendo esta misma nave o construyendo naves independientes, lo cual cambia la arquitectura de ventilación de cada etapa (ver pendiente relacionado en el [registro de cotizaciones](../../evidence/quotations/README.md#pendientes-con-este-proveedor)).

### Recolección de huevo

Para la primera unidad de 640 aves se recomienda:

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
