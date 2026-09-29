---
title: "Sistema de automatización"
project: "NidoSmart"
document_type: "business-plan"
status: "draft"
version: "1.5"
last_updated: "2026-09-28"
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

**Especificación objetivo (revisión julio 2026):** la industria recomienda un espacio de comedero de referencia de **10 cm por ave** (mínimo según línea genética: 7.6–8.4 cm/ave), con jaulas más anchas y menos profundas mostrando consistentemente mejor desempeño que jaulas angostas y profundas (Bell & Weaver, tablas 52-1, 52-6 y 52-7).

**Resuelto (2026-09-28) — respuesta directa de FamTECH:** cada jaula aloja 32 aves con dos comederos que suman 2.4 m de longitud, equivalente a **≈7.5 cm/ave** (ver [correspondencia](../../evidence/correspondence/2026-09-28_FamTECH_email_respuesta-lote1-expansion-layout.rtfd)). Comparado contra la guía de manejo de la línea genética específica del proyecto (Hy-Line W-80, `knowledge-base/genetics/hy-line-w80.pdf`: **7–9 cm/ave** en etapa de producción) — referencia más precisa que la genérica de Bell & Weaver de arriba — el valor queda **dentro del rango de la línea, pero en el extremo bajo, sin margen adicional**, mismo patrón ya observado con la relación de níples por ave (8 aves/níple). No amerita renegociar el diseño, pero no hay margen para absorber competencia por el comedero si se observa durante el comisionamiento.

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

**Resuelto (2026-09-20) — respuesta directa de FamTECH:** 4 níples por nivel de 32 aves = **8 aves por níple**. Está en el extremo superior del rango recomendado por Bell & Weaver (6–8), no en el punto medio — aceptable, pero sin margen adicional; si se observa cola en el bebedero durante el comisionamiento, no hay forma de aumentar la densidad de níples sin modificar la jaula ya cotizada.

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

*Ubicación de luminarias — CORREGIDO Y RESUELTO (2026-09-20/21, respuesta directa de FamTECH en dos rondas, reemplaza la conclusión de la revisión de septiembre 2026 anterior):* el proveedor confirmó que su diseño real es un arreglo de luminarias en el **pasillo central**, **no** una tira LED integrada por nivel en el marco de la jaula — contradice la conclusión previa de este documento, que asumía (a partir de documentación pública de *otros* fabricantes de jaula tipo H, no de una confirmación directa de FamTECH) que la tira por nivel ya estaba resuelta por el diseño estructural del proveedor.

Al preguntar directamente por la justificación y por el riesgo de atenuación entre niveles, FamTECH consultó con su equipo de ingeniería y respondió con el razonamiento completo (correo [`2026-09-21_FamTECH_email_cotizacion-iluminacion-y-explicacion.rtfd`](../../evidence/correspondence/2026-09-21_FamTECH_email_cotizacion-iluminacion-y-explicacion.rtfd/)):

* Iluminación *dentro* de la jaula (tira LED) es propia de jaulas "furnished/welfare", no del sistema tipo H de alta densidad que se cotizó — la jaula tipo H prioriza densidad/costo, con estructura compacta y poca altura libre, sin espacio para luminaria interna.
* Riesgos de instalarla dentro de la jaula: picaje de las aves por aburrimiento contra la luminaria, y riesgo de conducción eléctrica si hay fuga de la línea de níples cerca de un componente eléctrico — un riesgo real dado el diseño hidráulico de níples ya definido en [9.2](./09-arquitectura-electrica-hidraulica-comunicaciones.md#92-sistema-hidráulico).
* Instalación en pasillo facilita mantenimiento e inspección.
* **Mitigación de la atenuación top/bottom (sí fue considerada por el proveedor, no ignorada):** arreglo de **2 lámparas por punto de suspensión** ("hanger rod" común), espaciados cada ~2.5 m a lo largo del pasillo — Lámpara 1 a **20 cm sobre la red superior** (cubre nivel 1) y Lámpara 2 colgando **1.2–1.5 m por debajo de la red superior**, ajustable (cubre los niveles inferiores). Diagrama del proveedor: [`2026-09-21_FamTECH_diagrama-altura-lamparas.jpeg`](../../evidence/quotations/2026-09-21_FamTECH_diagrama-altura-lamparas.jpeg).
* **Especificación del foco:** DC48V, 7W, 3000K, regulable (dimming).

**Cotización formal recibida (2026-09-21, v4):** 14 focos regulables + 134 m de cable impermeable + 1 controlador de dimming = **$945.65 USD EXW**, ya incluida en el precio total de la nave (ver [registro de cotizaciones](../../evidence/quotations/README.md)). 14 focos ÷ 2 por punto = 7 puntos, consistente con ~17 m de pasillo a 2.5 m de espaciamiento. El estimado previo del presupuesto ([sección 7](../../docs/investment-project/07-presupuesto-consolidado-inversion-inicial.md#7-iluminación), $15,000–$35,000 MXN) resultó razonable frente a este precio real.

**Lo que esto cambia respecto a la corrección del 2026-09-20:** ya no se trata de un vacío total que NidoSmart debe resolver desde cero — FamTECH sí diseñó una mitigación específica para el riesgo de atenuación entre niveles, y la cotiza como parte del equipo.

**Flujo luminoso — resuelto (2026-09-22):** FamTECH confirmó "Luminous flux: 7W × 120LM" — es decir, **120 lm/W de eficacia**, equivalente a **≈840 lúmenes por foco** (7W × 120 lm/W). Con 14 focos, el total instalado en la nave es **≈11,760 lúmenes**. Verificación cruzada con la referencia de mercado del 2026-09-22 (abajo): el dato real de FamTECH (120 lm/W) es más conservador que la cifra genérica que se había encontrado en búsqueda web (≈170 lm/W) — la cifra real del fabricante siempre reemplaza a la de mercado.

**Sanity check de orden de magnitud (no sustituye el comisionamiento):** repartiendo los ≈11,760 lúmenes totales sobre los ≈68 m² de la nave de forma uniforme (supuesto optimista, ignora pérdidas por distancia, obstrucción de la propia jaula entre niveles, y que la luz no se reparte uniformemente desde el pasillo hacia los costados), el promedio sería **≈173 lux** — muy por encima del objetivo de diseño (30 lux) y del mínimo aceptable (15–20 lux). Esto es una señal de que el sistema **probablemente tiene margen suficiente**, pero **no reemplaza la medición real**: el promedio de área no dice nada sobre el nivel inferior específicamente, que es el punto de mayor riesgo por la distancia a la Lámpara 1 (superior) y la obstrucción de los 3 niveles encima. FamTECH no proporcionó ángulo de haz ni curva fotométrica del foco, así que no puede calcularse el lux real en el canal de alimento del nivel 4 sin medir — el protocolo de comisionamiento (abajo) sigue siendo la única verificación confiable.

*Tragaluces y cortina de blackout (complemento de ahorro energético, materiales locales):* lámina traslúcida corrugada de fibra de vidrio o policarbonato (producto estándar de proveedores de materiales para naves industriales/agrícolas en México) en 2–5% del área de techo, distribuida a lo largo de los 17 m — estimación de práctica general de diseño, a validar. Cortina interior opaca tipo invernadero (lona/tela blackout), operada con motorreductor + torno del mismo tipo ya cotizado por FamTECH para las ventanas de entrada de aire. Blackout total obligatorio durante las horas oscuras del fotoperiodo, sincronizado con el mismo controlador — un "brown-out" mal sellado sigue siendo influenciado por luz exterior y arriesga el programa de fotoperiodo (Bell & Weaver).

*Control y monitoreo de iluminación (decisión de diseño, 2026-09-17; replanteada 2026-09-21 a la luz de la respuesta de FamTECH):* con el sistema de pasillo de FamTECH ya cotizado como base, el rol de NidoSmart se separa en dos capas:

1. **Monitoreo (siempre, bajo costo):** 4 sensores de lux (uno por nivel, medidos sobre el canal de alimento), conectados al **PLC/controlador propio de NidoSmart** (consistente con DEC-007 — control crítico local y autónomo). Sirven para el protocolo de comisionamiento (ver abajo) y para verificación continua de que cada nivel se mantiene dentro del rango objetivo, con alarma si un nivel cae por debajo del mínimo o supera el techo de 50 lux.
2. **Control activo desde el PLC propio de NidoSmart — resuelto favorablemente (2026-09-22):** FamTECH confirmó que el controlador de dimming **puede conectarse a un PLC externo por terminales 0–10V** para control enlazado (además de operar en modo independiente por su propio panel), soporta programación por horario y control individual, y puede integrarse a un sistema de control ambiental para gestión centralizada. Esto significa que el perfil de fotoperiodo (arranque ~10h, incremento gradual a 15–16h) **puede programarse y ejecutarse desde el PLC propio de NidoSmart** vía la señal analógica 0–10V, consistente con DEC-007 (control crítico local y autónomo) — no se depende del panel de fábrica de FamTECH para esta lógica. **Pendiente nuevo:** FamTECH aclaró que "the prices differ between the two" (modo independiente vs. enlazado a PLC) sin dar el monto — falta cotizar la diferencia de precio del controlador en modo 0–10V/PLC-linked frente al ya cotizado ($679.39 USD, presumiblemente el modo independiente).
3. **Mitigación física complementaria (fallback, solo si el comisionamiento lo exige):** si, a pesar de tener control de dimming desde el PLC, la medición real revela que el nivel inferior no alcanza el mínimo de 15–20 lux con la intensidad máxima del arreglo de FamTECH, la mitigación pasa a ser una tira LED complementaria solo en el/los niveles deficientes (no las 20 tiras completas asumidas en la corrección del 2026-09-20), dimensionada con el dato real de déficit medido — evita sobre-construir una solución completa sin saber todavía si se necesita.

Este enfoque evita tanto el error original (asumir que la tira por nivel ya venía resuelta) como el sobrecorrección del 2026-09-20 (asumir que había que comprar y montar 20 tiras completas sin haber verificado primero si el sistema de FamTECH, ya con su propia mitigación de 2 lámparas por punto, es suficiente).

*Protocolo de verificación (comisionamiento):* medir lux sobre el canal de alimento cada 25 cm entre luminarias, en cada uno de los 4 niveles (30–100 lecturas totales) — protocolo de Hy-Line, boletín técnico.

*Tipo de LED (solo aplica a la tira complementaria condicional, ver arriba — el sistema base de pasillo ya viene especificado por FamTECH: DC48V, 7W, 3000K, regulable):* si el comisionamiento exige una tira LED complementaria por nivel, esta debe ser categoría agrícola general (no la línea específica para avicultura, difícil de conseguir localmente — ver preferencia de materiales locales), regulable con driver compatible, espectro cálido 2700–3000K (para no crear una mezcla de tonalidades con el foco de FamTECH, ya en 3000K), material no vidrio (lavable/desinfectable), clasificado para operación continua de 16h/día.

*Respaldo eléctrico (hallazgo — gap identificado):* el presupuesto de UPS (ítem 8, `07-presupuesto-consolidado-inversion-inicial.md`) no incluye explícitamente iluminación entre sus cargas críticas. Pendiente decidir si el circuito de iluminación entra al respaldo; en cualquier caso el controlador requiere reloj de tiempo real (RTC) con respaldo de batería local, independiente de un corte de energía general. **Nota (2026-09-21):** con la potencia real ya conocida (14 × 7W = 98W, alimentados a DC48V por el controlador de dimming), el circuito de iluminación es una carga eléctricamente trivial para la UPS — la decisión pendiente ya no es de capacidad, sino de si vale la pena el punto adicional de cableado a la UPS para una carga tan pequeña.

**Pendientes que requería confirmar FamTECH — resueltos (2026-09-20/21):**

1. ~~Si la estructura de jaula de nuestro pedido incluye el riel/soporte para tira LED en cada uno de los 4 niveles.~~ — **Resuelto:** no lo incluye; el diseño de FamTECH usa luminarias de pasillo, no tira por nivel.
2. ~~Si la tira LED en sí está incluida en el precio del ítem "cage" (III.3) o es partida aparte.~~ — **Resuelto:** no está incluida bajo ningún ítem; no forma parte del diseño del proveedor.
3. ~~Especificación eléctrica del riel/conector.~~ — **Sin objeto:** no existe ese riel en el diseño de FamTECH.
4. ~~Espaciamiento y altura de montaje de las luminarias de pasillo.~~ — **Resuelto (2026-09-21):** 2 focos por punto de suspensión, cada 2.5 m — Lámpara 1 a 20 cm sobre la red superior, Lámpara 2 ajustable 1.2–1.5 m por debajo de la red superior (ver diagrama citado arriba).

**Pendientes de iluminación — resueltos (2026-09-22, respuesta final de FamTECH):**

1. ~~Flujo luminoso (lúmenes) del foco.~~ — **Resuelto:** 120 lm/W, ≈840 lm/foco, ≈11,760 lm totales (ver arriba).
2. ~~Si el controlador de dimming permite zonificar por tramo o control individual.~~ — **Resuelto:** sí — modo independiente por zona, o enlazado a PLC externo, con programación por horario y control individual; integrable a un sistema de control ambiental centralizado.
3. ~~Si el controlador puede integrarse a un PLC externo (0–10V o DALI).~~ — **Resuelto:** sí, por terminales **0–10V** (ver "Control activo" arriba).

**Resuelto (2026-09-23):** el precio del controlador **no cambia** en modo PLC-linked (0–10V) frente al modo independiente — sigue siendo $679.39 USD ya cotizado. Solo es necesario que el sistema de control ambiental propio de NidoSmart incorpore la señal PLC (0–10V) de su lado; no hay sobrecosto del lado de FamTECH. Con esto, la integración del fotoperiodo al PLC propio de NidoSmart queda cerrada sin impacto en el presupuesto de iluminación ya registrado ([sección 7](../../docs/investment-project/07-presupuesto-consolidado-inversion-inicial.md#7-iluminación)).

**Referencia de mercado, ya superada por el dato real de FamTECH (búsqueda web, 2026-09-22, conservada solo como registro):** antes de la respuesta final, se había encontrado que el foco DC48V/3000K de bajo voltaje para jaula/pasillo avícola es una categoría de producto real y común en proveedores chinos de equipo avícola (ej. qingdaoejoy.com, ydj-lighting.com, rainmin2020), con una eficacia genérica de mercado de ≈170 lm/W. El dato real de FamTECH (120 lm/W) es más conservador — la cifra de mercado no se usó para ningún cálculo de diseño, solo como verificación de plausibilidad antes de tener el dato confirmado.

**Proveedores locales a buscar (condicional — solo si el comisionamiento revela déficit de lux en algún nivel):** tiras LED agrícolas genéricas (2700–3000K, regulables) y su riel/soporte de montaje sobre el marco de jaula, dimensionadas al déficit real medido, no a las 20 tiras completas. Los proveedores de lámina traslúcida, cortina térmica/blackout con motorreductor y sensores de lux compatibles con el PLC siguen siendo necesarios sin condición (no dependen de este hallazgo).

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

**Escalamiento con el crecimiento — corregido ([DEC-014](../governance/registro-de-decisiones.md#dec-014--expansión-lineal-de-la-nave-con-equipo-de-alimentaciónrecolección-compartido-hasta-el-techo-declarado-por-el-proveedor), 2026-09-17):** el crecimiento hacia el techo de 90 sets (~11,520 aves) declarado por FamTECH ocurre **extendiendo linealmente esta misma nave**, con una sola unidad de arrastre de alimentación y recolección de huevo dando servicio a todos los sets. En consecuencia, **la tabla de escalamiento por set de arriba es la hoja de ruta real, no un ejercicio ilustrativo**: el sistema de ventilación de la unidad actual (transversal/presión negativa, 3,600–10,000 cfm, sin cooling pads) es correcto para 5 sets/17 m, pero debe migrarse a modo túnel conforme la nave se alargue hacia el techo declarado (a escala de ~120 m de referencia del proveedor, el túnel se vuelve la opción técnicamente correcta — ver evaluación de sistemas arriba).

**Footprint real por set — resuelto (2026-09-28):** FamTECH confirmó que el cuerpo de jaula (1.2×1.2 m) es el valor que se repite por set a lo largo de la fila, y que **no debe calcularse dividiendo los 17 m totales entre 5 sets** (esa división incluía por error el equipo de cabecera, que es único por fila, no por set) — ver [correspondencia](../../evidence/correspondence/2026-09-28_FamTECH_email_respuesta-lote1-expansion-layout.rtfd) y [Diseño físico — 7.1.1](./07-diseno-fisico.md#711-layout-funcional-recomendado-dentro-de-la-nave-17×4×42-m). Esto corrige la estimación anterior de 3.4 m/set (que sugería un techo real muy por debajo del declarado por el proveedor) — con 1.2 m/set, el límite de 100 m del feeder (ver abajo) permite del orden de ~80 sets, mucho más cercano al techo declarado de 90 sets. **Pendiente crítico restante:** el número exacto de sets que admite la línea de nuestro pedido antes de requerir un segundo sistema compartido, y en qué umbral conviene migrar la ventilación a modo túnel, siguen pendientes — FamTECH remitió estas preguntas a su ingeniero civil, ausente en visita de obra al momento de responder. La cimentación y estructura civil deben planearse extensibles desde el diseño inicial (ver [Ficha técnica — Nave avícola, fila "Expansión futura"](../investment-project/05-ficha-tecnica-nave.md)), aunque solo se construyan los primeros 17 m ahora.

**Pendientes que requieren respuesta de FamTECH:**

1. Curva de desempeño real de los 2 ventiladores de 50"/1.1 kW ya cotizados (cfm a 0", 0.05" y 0.10" de columna de agua) — sin esto no se puede confirmar si están sobrados o justos frente al rango calculado (3,600–10,000 cfm para 640 aves).
2. Si el paquete de control ambiental puede re-cotizarse separando ventiladores + entradas + controlador (de interés) de los cooling pads (no de interés por ahora).
3. Área efectiva de cada una de las 12 entradas de aire CJ01 (para verificar velocidad de entrada contra la Tabla 9-2 de Bell & Weaver).
4. Si el controlador YB permite programar ventilación escalonada (mínimo invierno → máximo verano) o solo operación on/off.
5. ~~Cuántos sets adicionales admite la MISMA unidad de arrastre de alimentación y recolección de huevo de nuestro pedido antes de requerir un segundo sistema compartido completo.~~ — **Parcialmente resuelto (2026-09-28):** metodología de cálculo corregida (ver arriba); el número exacto sigue pendiente con el ingeniero civil de FamTECH (ver [registro de cotizaciones](../../evidence/quotations/README.md#pendientes-con-este-proveedor)).

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
* Contenedor cerrado, techado/protegido de lluvia directa.
* Traslado a zona separada de compostaje.
* Registro de cada retiro.

**Objetivo de humedad y parámetros de compostaje (revisión septiembre 2026, Bell & Weaver, cap. 11):** la gallinaza fresca sale con 75–80% de humedad; el objetivo en almacenamiento es reducirla a **menos de 35%** para minimizar la reproducción de moscas (se logra con aireación de la pila, altura controlada y volteo — el contenedor cerrado por sí solo no es suficiente). Para el compostaje: relación carbono:nitrógeno de **20–25:1** (agregar material rico en carbono, p. ej. viruta o paja, si la gallinaza pura no la alcanza), humedad de la pila entre **35 y 50%**, con aireación por volteo periódico y monitoreo de temperatura. Antes de transportar la gallinaza fuera del predio se requiere tratamiento térmico de fermentación de al menos 48 h a ≥56°C, avalado por escrito por un MVZ (Manual de Buenas Prácticas Pecuarias, §8.4, cita NOM-024-ZOO-1995) — ver también [Diseño físico — 7.2.2](./07-diseno-fisico.md#722-drenaje-y-manejo-de-gallinaza-revisión-septiembre-2026).

**Capacidad objetivo de la banda ante el crecimiento (calculado 2026-09-23):** dado que, por [DEC-014](../governance/registro-de-decisiones.md#dec-014--expansión-lineal-de-la-nave-con-equipo-de-alimentaciónrecolección-compartido-hasta-el-techo-declarado-por-el-proveedor), la banda de retiro de gallinaza (1.0×1130 mm ya cotizada) es equipo **compartido y lineal** — no se duplica por cada set nuevo — su capacidad debe verificarse contra el volumen máximo futuro, no solo contra las 640 aves actuales. Escalando el volumen ya calculado (65–125 kg/día a 640 aves):

| Escala | Aves | Gallinaza fresca (kg/día) |
|---|---:|---:|
| Unidad actual | 640 | 65–125 |
| Segunda unidad | 1,280 | 130–250 |
| **Meta del plan** | **≈5,120** | **≈520–1,000** |
| Techo declarado por el proveedor | ≈11,520 | ≈1,170–2,250 |

El requisito prioritario es que la misma banda soporte, sin acumulación, el volumen de la **meta del plan (≈1,000 kg/día)** — el techo declarado de 90 sets es información de contexto, no el objetivo de diseño (mismo criterio ya aplicado en la tabla de ventilación por set, arriba). Este cálculo se envía como cifra concreta a FamTECH, en vez de solo preguntar el throughput en abierto — ver pendiente actualizado en el [registro de cotizaciones](../../evidence/quotations/README.md#nuevos-pendientes-de-agua-y-gallinaza-2026-09-18-identificados-al-definir-los-requisitos-físicos-de-agua-drenaje-y-manejo-de-gallinaza-ver-diseño-físico--722-y-arquitectura-eléctricahidráulica--92).

**Arquitectura de la banda ante el crecimiento — parcialmente resuelto (2026-09-28):** FamTECH confirmó que el sistema de retiro de gallinaza sigue la misma lógica que el de alimentación: la unidad motriz (drive unit) y las secciones de cabecera son equipo compartido, comprado una sola vez por fila, mientras que los tramos de banda en sí (consumibles, dependientes de la longitud) se agregan por cada sección nueva conforme la nave crece (ver [correspondencia](../../evidence/correspondence/2026-09-28_FamTECH_email_respuesta-lote1-expansion-layout.rtfd)). Esto confirma que la banda **sí escala con la nave** sin duplicar la unidad motriz — pero el throughput real (kg/h) de la banda sigue sin un número: FamTECH remitió esta pregunta, junto con las demás de obra civil, a su ingeniero, ausente en visita de sitio al momento de responder. La cifra objetivo de ≈1,000 kg/día (tabla arriba) sigue vigente como el requisito a verificar cuando llegue esa respuesta.

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
