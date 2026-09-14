---
title: "Registro de decisiones"
project: "NidoSmart"
document_type: "business-plan-annex"
status: "draft"
version: "1.2"
last_updated: "2026-09-14"
---

# Registro de decisiones

Este registro centraliza las decisiones estratégicas explícitas identificadas en el plan de negocios original. Ninguna fecha ni justificación fue inventada: cuando el documento fuente no especifica una fecha, se indica "No especificada"; cuando no detalla una justificación más allá de la propia narrativa, se cita la sección de origen.

## DEC-001 — Nombre del proyecto: NidoSmart

**Estado:** Aprobada
**Fecha:** No especificada
**Decisión:** El proyecto y la marca se denominan "NidoSmart", con el eslogan "Automatización que cuida, producción que crece."
**Justificación:** No se documenta una justificación explícita del nombre en el archivo fuente; se presenta como dato ya definido desde el encabezado del plan.
**Consecuencias:** El nombre se utiliza consistentemente en toda la documentación, en la nomenclatura de componentes (por ejemplo, "NidoSmart Core") y en la identidad comercial.
**Documentos relacionados:**

- [Resumen ejecutivo](../business-plan/01-resumen-ejecutivo.md)
- [Estrategia de desarrollo tecnológico](../business-plan/22-desarrollo-tecnologico.md)

## DEC-002 — Inicio con gallinas ponedoras y no con pollo de engorda

**Estado:** Aprobada
**Fecha:** No especificada
**Decisión:** El negocio comenzará con gallinas ponedoras comerciales, preferentemente pollitas de prepostura de 16 a 18 semanas, y no con pollo de engorda.
**Justificación:** Las ponedoras ofrecen flujo de ingresos diario, curva de aprendizaje gradual, venta directa sencilla, menor necesidad de cadena sanitaria y sacrificio, y permiten corrección continua de errores comerciales, según la comparación de la sección 4.1.
**Consecuencias:** Define el modelo productivo, el ciclo comercial (venta diaria vs. por lote) y la ausencia inicial de procesamiento/sacrificio en la operación.
**Documentos relacionados:**

- [Selección del modelo productivo](../business-plan/04-modelo-productivo.md)
- [Resumen ejecutivo](../business-plan/01-resumen-ejecutivo.md)

## DEC-003 — Inicio controlado con una operación piloto de aproximadamente 100 gallinas

**Estado:** Superada por [DEC-012](#dec-012--congelamiento-del-alcance-de-la-inversión-inicial-en-una-unidad-productiva-de-640-aves)
**Fecha:** No especificada
**Decisión:** El proyecto inicia con un módulo piloto de aproximadamente 100 gallinas (96 a 120 plazas), en lugar de una explotación de miles de aves.
**Justificación:** Permite adquirir experiencia técnica, sanitaria, operativa y comercial sin asumir el riesgo de una operación de gran escala.
**Consecuencias:** Establece la escala de diseño inicial, condiciona el objetivo financiero del piloto a la validación del modelo (no a la rentabilidad plena) y define el criterio de expansión hacia 200–300 aves.
**Actualización (2026-09-13):** esta decisión se conserva como referencia histórica de la lógica original ("empezar pequeño, sin asumir el riesgo de miles de aves"). El número específico de 96–120 aves fue una estimación previa a contar con una cotización real. Al recibirse la cotización del proveedor de jaula automatizada, la escala real mínima que se construye y se financia resultó ser de 640 aves, no de 100. La lógica de fondo (inicio controlado, validación antes de escalar) sigue vigente y se traslada íntegra a [DEC-012](#dec-012--congelamiento-del-alcance-de-la-inversión-inicial-en-una-unidad-productiva-de-640-aves), que sustituye el número de aves y el criterio de expansión.
**Documentos relacionados:**

- [Resumen ejecutivo](../business-plan/01-resumen-ejecutivo.md)
- [Validación del piloto](../business-plan/18-validacion-del-piloto.md)
- [Conclusiones y decisión recomendada](../business-plan/27-conclusiones-y-decision.md)

## DEC-004 — Arquitectura modular de crecimiento

**Estado:** Aprobada
**Fecha:** No especificada
**Decisión:** La infraestructura se construye como una plataforma ampliable por módulos independientes, en lugar de rediseñarse por completo cada vez que aumente el número de aves.
**Justificación:** Evita rediseñar la granja en cada etapa de crecimiento y permite que el segundo y tercer módulo se conecten sin sustituir la infraestructura principal.
**Consecuencias:** Cada módulo mantiene alojamiento, línea de agua, alimentación, recolección de huevo y sensores propios, mientras que los servicios principales (almacenamiento, silo, agua, cuarto eléctrico, servidor, comunicaciones) se comparten entre módulos.
**Documentos relacionados:**

- [Modelo modular de crecimiento](../business-plan/06-crecimiento-modular.md)
- [Hoja de ruta](../business-plan/23-hoja-de-ruta.md)

## DEC-005 — Objetivo de cubrir el OPEX directo durante la validación del piloto, sin exigir recuperación del CAPEX

**Estado:** Aprobada
**Fecha:** No especificada
**Decisión:** El objetivo financiero del primer módulo (piloto) es cubrir el OPEX directo normalizado y validar el modelo productivo, tecnológico y comercial durante el primer ciclo, sin exigir la recuperación del CAPEX.
**Justificación:** Un módulo de escala reducida frente al crecimiento planeado (originalmente estimado en 100 aves, hoy en 640 tras [DEC-012](#dec-012--congelamiento-del-alcance-de-la-inversión-inicial-en-una-unidad-productiva-de-640-aves)) no tiene por sí solo la escala de una operación industrial; exigir la recuperación total del CAPEX al piloto podría llevar a la conclusión errónea de que el negocio no es rentable.
**Consecuencias:** El piloto se evalúa mediante cuatro validaciones (productiva, tecnológica, comercial y económica) y una tabla de criterios de éxito antes de autorizar el segundo módulo.
**Documentos relacionados:**

- [Objetivos del proyecto](../business-plan/05-objetivos.md)
- [Validación del piloto](../business-plan/18-validacion-del-piloto.md)
- [Plan financiero preliminar](../business-plan/17-plan-financiero.md)

## DEC-006 — Automatización intensiva de al menos 90% de las tareas repetitivas

**Estado:** Aprobada
**Fecha:** No especificada
**Decisión:** Automatizar más del 90% de las operaciones repetitivas: alimentación, agua, iluminación, ventilación, control ambiental, recolección de huevo, retiro de gallinaza, monitoreo y generación de alertas.
**Justificación:** Reduce la mano de obra repetitiva y mantiene condiciones ambientales estables, aunque el documento aclara que la automatización no elimina la necesidad de inspección diaria.
**Consecuencias:** Define el alcance del sistema de automatización y la prioridad de inversión hacia procesos donde una falla puede matar aves o reducir inmediatamente la producción (agua, ventilación, alarmas, energía de respaldo).
**Documentos relacionados:**

- [Sistema de automatización](../business-plan/08-automatizacion.md)
- [Estrategia de inversión](../business-plan/26-estrategia-de-inversion.md)

## DEC-007 — Uso de un PLC o controlador avícola como núcleo del control crítico

**Estado:** Aprobada
**Fecha:** No especificada
**Decisión:** El control crítico (agua, ventilación, alarmas y demás procesos de seguridad) se ejecuta mediante un PLC o controlador avícola operando de forma local y autónoma, sin depender de inteligencia artificial, servicios externos ni conexión a internet.
**Justificación:** El control físico y de seguridad debe seguir funcionando aunque falle el enlace de internet o el agente de IA, conforme al principio fundamental de la arquitectura tecnológica.
**Consecuencias:** Establece la jerarquía tecnológica del proyecto (control físico → PLC → gateway → base de datos → agente inteligente → sistemas administrativos) y limita el rol de Hermes Agent y Paperclip a la capa de datos e inteligencia.
**Documentos relacionados:**

- [Arquitectura tecnológica](../business-plan/10-arquitectura-tecnologica.md)
- [Seguridad funcional y ciberseguridad](../business-plan/13-seguridad-y-ciberseguridad.md)

## DEC-008 — Uso de agentes de IA como asistentes, no como controladores críticos

**Estado:** Aprobada
**Fecha:** No especificada
**Decisión:** La inteligencia artificial (Hermes Agent y, más adelante, Paperclip) se incorpora como asistente de operación y negocio, con una política de "lectura amplia y escritura restringida", sin entregarle el control crítico de las aves.
**Justificación:** Evita que un error del agente de IA pueda comprometer directamente la ventilación mínima, la disponibilidad de agua, el fotoperiodo, la dosificación veterinaria u otros parámetros de seguridad.
**Consecuencias:** El agente puede crear alertas, generar reportes, abrir órdenes de mantenimiento y proponer cambios dentro de bandas autorizadas, pero requiere aprobación humana para acciones fuera de esos límites; el PLC conserva la autoridad final.
**Documentos relacionados:**

- [Arquitectura tecnológica](../business-plan/10-arquitectura-tecnologica.md)
- [Seguridad funcional y ciberseguridad](../business-plan/13-seguridad-y-ciberseguridad.md)
- [Funciones del agente inteligente](../business-plan/12-funciones-agente-inteligente.md)

## DEC-009 — Elección entre Hermes Agent y Paperclip

**Estado:** Aprobada
**Fecha:** No especificada
**Decisión:** Se adopta Hermes Agent como núcleo de inteligencia operativa desde la primera etapa, y se difiere Paperclip como sistema futuro de coordinación empresarial, a incorporarse cuando existan varias naves, múltiples responsables, más de una ubicación, agentes especializados, presupuestos por área o necesidad formal de auditoría multiagente.
**Justificación:** Hermes Agent es adecuado para operación local en un único sitio o una operación pequeña; Paperclip está orientado a gobernanza y coordinación multiagente, lo cual resulta prematuro para una granja inicial de 640 aves.
**Consecuencias:** Paperclip queda explícitamente en la lista de tecnología que debe aplazarse hasta contar con datos reales, y su incorporación se ubica en la Fase 5 de la hoja de ruta (2,500–5,000 aves).
**Documentos relacionados:**

- [Evaluación técnica de Hermes Agent y Paperclip](../business-plan/11-hermes-agent-y-paperclip.md)
- [Estrategia de desarrollo tecnológico](../business-plan/22-desarrollo-tecnologico.md)
- [Hoja de ruta](../business-plan/23-hoja-de-ruta.md)

## DEC-010 — Dimensionamiento de servicios compartidos para 300 aves desde el módulo piloto

**Estado:** Actualizada por [DEC-012](#dec-012--congelamiento-del-alcance-de-la-inversión-inicial-en-una-unidad-productiva-de-640-aves)
**Fecha:** No especificada
**Decisión:** Aunque el módulo piloto aloja entre 96 y 120 aves, los servicios compartidos (electricidad, agua, comunicaciones, control ambiental, almacenamiento, empaque y respaldo energético) se dimensionan para aproximadamente 300 aves.
**Justificación:** Permite que el segundo y tercer módulo se conecten sin sustituir la infraestructura principal, evitando rediseños costosos en etapas tempranas de crecimiento.
**Consecuencias:** Incrementa la inversión inicial en servicios compartidos respecto de lo estrictamente necesario para 100 aves, pero reduce el CAPEX incremental de los módulos 2 y 3.
**Actualización (2026-09-13):** el objetivo de dimensionamiento de 300 aves quedó por debajo de la escala real del módulo piloto (640 aves, ya superior a 300). El principio (dimensionar los servicios compartidos con margen para el siguiente módulo, no sólo para el piloto) sigue vigente, pero el objetivo numérico se traslada a 1,280 aves (segunda unidad completa) en [DEC-012](#dec-012--congelamiento-del-alcance-de-la-inversión-inicial-en-una-unidad-productiva-de-640-aves).
**Documentos relacionados:**

- [Resumen ejecutivo](../business-plan/01-resumen-ejecutivo.md)
- [Modelo modular de crecimiento](../business-plan/06-crecimiento-modular.md)
- [Hoja de ruta](../business-plan/23-hoja-de-ruta.md)

## DEC-011 — Desarrollo tecnológico previo al ingreso de las aves

**Estado:** Aprobada
**Fecha:** No especificada
**Decisión:** El núcleo tecnológico mínimo (control crítico, plataforma de datos e integración básica) debe desarrollarse, probarse en banco de pruebas e instalarse sin aves antes del ingreso de la parvada piloto, bajo un enfoque "technology-first, business-validated".
**Justificación:** Comenzar exclusivamente por la tecnología sin validación posterior arriesga automatizar supuestos incorrectos; por eso la secuencia correcta es definir requisitos → desarrollar el núcleo tecnológico → probarlo sin aves → instalar el módulo piloto → perfeccionarlo con datos reales, mientras el desarrollo comercial avanza en paralelo.
**Consecuencias:** Define la secuencia de cinco etapas de desarrollo tecnológico (especificación funcional, banco de pruebas, instalación sin aves, ingreso de la parvada piloto, inteligencia progresiva) dentro de la Fase 1 de la hoja de ruta.
**Documentos relacionados:**

- [Estrategia de desarrollo tecnológico](../business-plan/22-desarrollo-tecnologico.md)
- [Hoja de ruta](../business-plan/23-hoja-de-ruta.md)

## DEC-012 — Congelamiento del alcance de la inversión inicial en una unidad productiva de 640 aves

**Estado:** Aprobada
**Fecha:** 2026-09-13
**Decisión:** El alcance de la inversión inicial de NidoSmart queda congelado en una **primera unidad productiva financiable de 640 aves** (nave de 17×4×4.2 m, jaula automatizada tipo H, 5 sets, 4 niveles), sustituyendo la referencia anterior de un módulo piloto genérico de 96–120 aves usada antes de contar con una cotización real. Esta decisión define exactamente qué se construirá con el crédito: no una cifra aproximada, sino la unidad completa especificada por la cotización vigente del proveedor.
**Justificación:** Al recibirse la cotización de FamTECH para el sistema de jaula automatizada (ver [registro de cotizaciones](../../evidence/quotations/README.md)), se hizo evidente que la unidad mínima real que el proveedor construye y que puede financiarse como proyecto formal no es un módulo arbitrario de ~100 aves, sino una nave completa de 5 sets tipo H (640 aves). Diseñar y presupuestar sobre una cifra hipotética distinta a la unidad real que se compra habría introducido inconsistencias entre el plan de negocios, el diseño físico y cualquier expediente de financiamiento.
**Consecuencias:**

- Todas las cifras dependientes de escala del plan de negocios (producción, CAPEX, OPEX, layout, automatización, personal, cronograma y capacidad) se recalcularon o se marcaron explícitamente como pendientes a partir de 640 aves, no de 100.
- La escalera de crecimiento modular se redefine en incrementos de unidades completas de 640 aves (640 → 1,280 → ... → ≈5,120), retirando los escalones intermedios (200–300, 500 aves) que quedaban por debajo de la unidad mínima real.
- El CAPEX de la primera unidad se recalculó en **$723,300–$1,174,300 MXN**, con la partida de jaula + automatización ($328,300 MXN ≈ USD $17,747) respaldada por cotización real; el resto permanece como estimación preliminar pendiente de cotización formal (ver [Plan financiero — 17.1](../business-plan/17-plan-financiero.md#171-inversión-inicial)).
- Se retira el supuesto de "expansión anual de 100 aves": una segunda unidad es una decisión de financiamiento independiente, no un calendario automático, ya que el flujo operativo de la primera unidad no alcanza a cubrir el CAPEX de una segunda (ver [Plan financiero — 17.3](../business-plan/17-plan-financiero.md#173-proyección-preliminar--primera-unidad-640-aves)).
- Esta decisión es la base del [proyecto de inversión](../investment-project/README.md), que desarrolla el expediente de financiamiento formal para esta unidad congelada.
- Supera parcialmente a [DEC-003](#dec-003--inicio-controlado-con-una-operación-piloto-de-aproximadamente-100-gallinas) (número de aves del piloto) y a [DEC-010](#dec-010--dimensionamiento-de-servicios-compartidos-para-300-aves-desde-el-módulo-piloto) (objetivo de dimensionamiento de servicios compartidos), conservando en ambos casos la lógica original y sustituyendo solo las cifras.

**Documentos relacionados:**

- [Diseño físico preliminar](../business-plan/07-diseno-fisico.md)
- [Modelo modular de crecimiento](../business-plan/06-crecimiento-modular.md)
- [Producción y capacidad comercial](../business-plan/16-produccion-y-capacidad-comercial.md)
- [Plan financiero preliminar](../business-plan/17-plan-financiero.md)
- [Validación del piloto](../business-plan/18-validacion-del-piloto.md)
- [Hoja de ruta](../business-plan/23-hoja-de-ruta.md)
- [Proyecto de inversión](../investment-project/README.md)
- [Registro de cotizaciones](../../evidence/quotations/README.md)

## DEC-013 — Presupuesto consolidado de inversión inicial, con vehículo de distribución fuera del crédito

**Estado:** Aprobada
**Fecha:** 2026-09-14
**Decisión:** Se construye un presupuesto consolidado y trazable para llevar la unidad de 640 aves ([DEC-012](#dec-012--congelamiento-del-alcance-de-la-inversión-inicial-en-una-unidad-productiva-de-640-aves)) a condiciones reales de producción y comercialización, cubriendo las 18 categorías de partidas (jaulas/automatización, nave, obra civil, infraestructura eléctrica/hidráulica, ventilación, iluminación, respaldo energético, sensores, importación/logística, instalación, aves, bioseguridad, almacenamiento, vehículo, permisos, capital de trabajo y contingencia). Se decide además que, para esta etapa, **no se incluye la compra de un vehículo de distribución dedicado dentro del CAPEX financiado por crédito**: el volumen a distribuir (≈32 kg/día) no lo justifica y se cubre con capital propio.
**Justificación:** Antes de cotizar formalmente la obra civil de la nave, el objetivo exige contar con una ficha técnica estable; al construirla se encontró que 15 de 19 parámetros técnicos de la nave siguen sin definir (tipo estructural, materiales, altura libre, orientación, cubierta, muros, drenaje, resistencia a viento/granizo, piso, integración con la jaula, espacios de servicio, accesos, bioseguridad física, expansión futura e instalaciones eléctricas/hidráulicas asociadas) — ver [Ficha técnica — Nave avícola](../investment-project/05-ficha-tecnica-nave.md). Por lo tanto, la partida de obra civil ($227,000–$421,000 MXN) sigue siendo una estimación por huella, no una cotización comparable. Sobre el vehículo, el volumen de producción de la unidad de 640 aves (≈526–543 huevos/día, ≈32 kg/día) es demasiado bajo para justificar inmovilizar capital de crédito en una unidad dedicada, consistente con que la [hoja de ruta](../business-plan/23-hoja-de-ruta.md#fase-4-expansión-a-19202560-aves-3-4-unidades) ya ubicaba el "vehículo de reparto" hasta la Fase 4 (1,920–2,560 aves) — ver [Vehículo de distribución](../investment-project/06-vehiculo-de-distribucion.md).
**Consecuencias:**

- La inversión total estimada para la unidad de 640 aves, sin vehículo dedicado, sin transporte final Puebla→sitio (sin cotizar) y sin instalación de la jaula en sitio (alcance no confirmado con el proveedor), es de **≈$1,239,000–$2,152,000 MXN** — ver [Presupuesto consolidado de inversión inicial](../investment-project/07-presupuesto-consolidado-inversion-inicial.md).
- No deben solicitarse cotizaciones formales de obra civil hasta cerrar los pendientes críticos de la ficha técnica de la nave (decisión de tipo estructural, estudio estructural local, estudio de sitio, altura libre confirmada con el proveedor de jaula, distribución de espacios de servicio, estudio de carga eléctrica).
- Se agrega un nuevo pendiente al [registro de cotizaciones](../../evidence/quotations/README.md): confirmar con el proveedor si el precio cotizado incluye instalación en sitio o si es una partida aparte.
- La decisión de no comprar vehículo se revisa cuando la [validación del piloto](../business-plan/18-validacion-del-piloto.md) confirme una cartera de clientes real con rutas y distancias conocidas.
- Se identifica orientación preliminar (sujeta a confirmar con la institución financiera) sobre qué partidas califican para crédito refaccionario (CAPEX productivo y de infraestructura) frente a crédito de avío (preoperativos y capital de trabajo), y cuáles quedan fuera del crédito (vehículo, permisos, contingencia).

**Documentos relacionados:**

- [Ficha técnica — Nave avícola](../investment-project/05-ficha-tecnica-nave.md)
- [Vehículo de distribución](../investment-project/06-vehiculo-de-distribucion.md)
- [Presupuesto consolidado de inversión inicial](../investment-project/07-presupuesto-consolidado-inversion-inicial.md)
- [Proyecto de inversión](../investment-project/01-proyecto-de-inversion.md)
- [Plan financiero preliminar](../business-plan/17-plan-financiero.md)
- [Registro de cotizaciones](../../evidence/quotations/README.md)

## Decisiones candidatas no confirmadas en el documento fuente

Durante el análisis se evaluó si el plan original establece una decisión explícita sobre la **futura incorporación de pollo de engorda (broilers)** como línea adicional de negocio. El documento fuente compara ponedoras contra pollo de engorda únicamente para justificar el inicio con ponedoras (sección 4.1–4.2) y no contiene ninguna declaración explícita sobre incorporar broilers en una etapa posterior. Por lo tanto, **no se registra como decisión** para evitar inventar contenido no presente en el original. Se deja anotado como punto de revisión humana pendiente.

Como parte de la investigación técnica de julio de 2026 (contraste del BP contra Bell & Weaver, *Commercial Chicken Meat and Egg Production*), se identificó que el plan tampoco establece una decisión explícita sobre **reemplazo total de la parvada vs. muda/reciclaje de parvada (flock recycling)**. La industria trata esto como una decisión de primer orden: reemplazo total tras un ciclo (~75–80 semanas) frente a inducir la muda para extender la vida productiva de la parvada a un segundo ciclo (92–110 semanas, con un pico de producción 7–10% menor) o incluso un tercer ciclo. La decisión [DEC-002](#dec-002--inicio-con-gallinas-ponedoras-y-no-con-pollo-de-engorda) (comprar siempre pollitas de prepostura de 16–18 semanas) sugiere de forma implícita un modelo de reemplazo total sin muda, pero el documento fuente no lo declara explícitamente. **No se registra como decisión formal** por la misma razón que el punto anterior; queda anotado como punto de revisión humana pendiente, relevante para el modelo operativo ([14-modelo-operativo.md](../business-plan/14-modelo-operativo.md)) y el plan financiero ([17-plan-financiero.md](../business-plan/17-plan-financiero.md)).

---

## Navegación

- [Índice general](../business-plan/README.md)
- [Documento anterior: Conclusiones y decisión recomendada](../business-plan/27-conclusiones-y-decision.md)
- [Documento siguiente: Bibliografía](../../knowledge-base/bibliography.md)
