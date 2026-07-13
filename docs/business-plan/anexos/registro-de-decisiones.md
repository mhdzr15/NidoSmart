---
title: "Registro de decisiones"
project: "NidoSmart"
document_type: "business-plan-annex"
status: "draft"
version: "1.0"
last_updated: "2026-07-12"
source: "NidoSmartBP.md"
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

- [Resumen ejecutivo](../01-resumen-ejecutivo.md)
- [Estrategia de desarrollo tecnológico](../22-desarrollo-tecnologico.md)

## DEC-002 — Inicio con gallinas ponedoras y no con pollo de engorda

**Estado:** Aprobada
**Fecha:** No especificada
**Decisión:** El negocio comenzará con gallinas ponedoras comerciales, preferentemente pollitas de prepostura de 16 a 18 semanas, y no con pollo de engorda.
**Justificación:** Las ponedoras ofrecen flujo de ingresos diario, curva de aprendizaje gradual, venta directa sencilla, menor necesidad de cadena sanitaria y sacrificio, y permiten corrección continua de errores comerciales, según la comparación de la sección 4.1.
**Consecuencias:** Define el modelo productivo, el ciclo comercial (venta diaria vs. por lote) y la ausencia inicial de procesamiento/sacrificio en la operación.
**Documentos relacionados:**

- [Selección del modelo productivo](../04-modelo-productivo.md)
- [Resumen ejecutivo](../01-resumen-ejecutivo.md)

## DEC-003 — Inicio controlado con una operación piloto de aproximadamente 100 gallinas

**Estado:** Aprobada
**Fecha:** No especificada
**Decisión:** El proyecto inicia con un módulo piloto de aproximadamente 100 gallinas (96 a 120 plazas), en lugar de una explotación de miles de aves.
**Justificación:** Permite adquirir experiencia técnica, sanitaria, operativa y comercial sin asumir el riesgo de una operación de gran escala.
**Consecuencias:** Establece la escala de diseño inicial, condiciona el objetivo financiero del piloto a la validación del modelo (no a la rentabilidad plena) y define el criterio de expansión hacia 200–300 aves.
**Documentos relacionados:**

- [Resumen ejecutivo](../01-resumen-ejecutivo.md)
- [Validación del piloto](../18-validacion-del-piloto.md)
- [Conclusiones y decisión recomendada](../27-conclusiones-y-decision.md)

## DEC-004 — Arquitectura modular de crecimiento

**Estado:** Aprobada
**Fecha:** No especificada
**Decisión:** La infraestructura se construye como una plataforma ampliable por módulos independientes, en lugar de rediseñarse por completo cada vez que aumente el número de aves.
**Justificación:** Evita rediseñar la granja en cada etapa de crecimiento y permite que el segundo y tercer módulo se conecten sin sustituir la infraestructura principal.
**Consecuencias:** Cada módulo mantiene alojamiento, línea de agua, alimentación, recolección de huevo y sensores propios, mientras que los servicios principales (almacenamiento, silo, agua, cuarto eléctrico, servidor, comunicaciones) se comparten entre módulos.
**Documentos relacionados:**

- [Modelo modular de crecimiento](../06-crecimiento-modular.md)
- [Hoja de ruta](../23-hoja-de-ruta.md)

## DEC-005 — Objetivo de cubrir el OPEX directo durante la validación del piloto, sin exigir recuperación del CAPEX

**Estado:** Aprobada
**Fecha:** No especificada
**Decisión:** El objetivo financiero del primer módulo (piloto) es cubrir el OPEX directo normalizado y validar el modelo productivo, tecnológico y comercial durante el primer ciclo, sin exigir la recuperación del CAPEX.
**Justificación:** Un módulo de 100 aves no tiene escala suficiente para absorber eficientemente una infraestructura altamente automatizada diseñada para crecer; exigir la recuperación total del CAPEX al piloto podría llevar a la conclusión errónea de que el negocio no es rentable.
**Consecuencias:** El piloto se evalúa mediante cuatro validaciones (productiva, tecnológica, comercial y económica) y una tabla de criterios de éxito antes de autorizar el segundo módulo.
**Documentos relacionados:**

- [Objetivos del proyecto](../05-objetivos.md)
- [Validación del piloto](../18-validacion-del-piloto.md)
- [Plan financiero preliminar](../17-plan-financiero.md)

## DEC-006 — Automatización intensiva de al menos 90% de las tareas repetitivas

**Estado:** Aprobada
**Fecha:** No especificada
**Decisión:** Automatizar más del 90% de las operaciones repetitivas: alimentación, agua, iluminación, ventilación, control ambiental, recolección de huevo, retiro de gallinaza, monitoreo y generación de alertas.
**Justificación:** Reduce la mano de obra repetitiva y mantiene condiciones ambientales estables, aunque el documento aclara que la automatización no elimina la necesidad de inspección diaria.
**Consecuencias:** Define el alcance del sistema de automatización y la prioridad de inversión hacia procesos donde una falla puede matar aves o reducir inmediatamente la producción (agua, ventilación, alarmas, energía de respaldo).
**Documentos relacionados:**

- [Sistema de automatización](../08-automatizacion.md)
- [Estrategia de inversión](../26-estrategia-de-inversion.md)

## DEC-007 — Uso de un PLC o controlador avícola como núcleo del control crítico

**Estado:** Aprobada
**Fecha:** No especificada
**Decisión:** El control crítico (agua, ventilación, alarmas y demás procesos de seguridad) se ejecuta mediante un PLC o controlador avícola operando de forma local y autónoma, sin depender de inteligencia artificial, servicios externos ni conexión a internet.
**Justificación:** El control físico y de seguridad debe seguir funcionando aunque falle el enlace de internet o el agente de IA, conforme al principio fundamental de la arquitectura tecnológica.
**Consecuencias:** Establece la jerarquía tecnológica del proyecto (control físico → PLC → gateway → base de datos → agente inteligente → sistemas administrativos) y limita el rol de Hermes Agent y Paperclip a la capa de datos e inteligencia.
**Documentos relacionados:**

- [Arquitectura tecnológica](../10-arquitectura-tecnologica.md)
- [Seguridad funcional y ciberseguridad](../13-seguridad-y-ciberseguridad.md)

## DEC-008 — Uso de agentes de IA como asistentes, no como controladores críticos

**Estado:** Aprobada
**Fecha:** No especificada
**Decisión:** La inteligencia artificial (Hermes Agent y, más adelante, Paperclip) se incorpora como asistente de operación y negocio, con una política de "lectura amplia y escritura restringida", sin entregarle el control crítico de las aves.
**Justificación:** Evita que un error del agente de IA pueda comprometer directamente la ventilación mínima, la disponibilidad de agua, el fotoperiodo, la dosificación veterinaria u otros parámetros de seguridad.
**Consecuencias:** El agente puede crear alertas, generar reportes, abrir órdenes de mantenimiento y proponer cambios dentro de bandas autorizadas, pero requiere aprobación humana para acciones fuera de esos límites; el PLC conserva la autoridad final.
**Documentos relacionados:**

- [Arquitectura tecnológica](../10-arquitectura-tecnologica.md)
- [Seguridad funcional y ciberseguridad](../13-seguridad-y-ciberseguridad.md)
- [Funciones del agente inteligente](../12-funciones-agente-inteligente.md)

## DEC-009 — Elección entre Hermes Agent y Paperclip

**Estado:** Aprobada
**Fecha:** No especificada
**Decisión:** Se adopta Hermes Agent como núcleo de inteligencia operativa desde la primera etapa, y se difiere Paperclip como sistema futuro de coordinación empresarial, a incorporarse cuando existan varias naves, múltiples responsables, más de una ubicación, agentes especializados, presupuestos por área o necesidad formal de auditoría multiagente.
**Justificación:** Hermes Agent es adecuado para operación local en un único sitio o una operación pequeña; Paperclip está orientado a gobernanza y coordinación multiagente, lo cual resulta prematuro para una granja inicial de 100 aves.
**Consecuencias:** Paperclip queda explícitamente en la lista de tecnología que debe aplazarse hasta contar con datos reales, y su incorporación se ubica en la Fase 5 de la hoja de ruta (2,500–5,000 aves).
**Documentos relacionados:**

- [Evaluación técnica de Hermes Agent y Paperclip](../11-hermes-agent-y-paperclip.md)
- [Estrategia de desarrollo tecnológico](../22-desarrollo-tecnologico.md)
- [Hoja de ruta](../23-hoja-de-ruta.md)

## DEC-010 — Dimensionamiento de servicios compartidos para 300 aves desde el módulo piloto

**Estado:** Aprobada
**Fecha:** No especificada
**Decisión:** Aunque el módulo piloto aloja entre 96 y 120 aves, los servicios compartidos (electricidad, agua, comunicaciones, control ambiental, almacenamiento, empaque y respaldo energético) se dimensionan para aproximadamente 300 aves.
**Justificación:** Permite que el segundo y tercer módulo se conecten sin sustituir la infraestructura principal, evitando rediseños costosos en etapas tempranas de crecimiento.
**Consecuencias:** Incrementa la inversión inicial en servicios compartidos respecto de lo estrictamente necesario para 100 aves, pero reduce el CAPEX incremental de los módulos 2 y 3.
**Documentos relacionados:**

- [Resumen ejecutivo](../01-resumen-ejecutivo.md)
- [Modelo modular de crecimiento](../06-crecimiento-modular.md)
- [Hoja de ruta](../23-hoja-de-ruta.md)

## DEC-011 — Desarrollo tecnológico previo al ingreso de las aves

**Estado:** Aprobada
**Fecha:** No especificada
**Decisión:** El núcleo tecnológico mínimo (control crítico, plataforma de datos e integración básica) debe desarrollarse, probarse en banco de pruebas e instalarse sin aves antes del ingreso de la parvada piloto, bajo un enfoque "technology-first, business-validated".
**Justificación:** Comenzar exclusivamente por la tecnología sin validación posterior arriesga automatizar supuestos incorrectos; por eso la secuencia correcta es definir requisitos → desarrollar el núcleo tecnológico → probarlo sin aves → instalar el módulo piloto → perfeccionarlo con datos reales, mientras el desarrollo comercial avanza en paralelo.
**Consecuencias:** Define la secuencia de cinco etapas de desarrollo tecnológico (especificación funcional, banco de pruebas, instalación sin aves, ingreso de la parvada piloto, inteligencia progresiva) dentro de la Fase 1 de la hoja de ruta.
**Documentos relacionados:**

- [Estrategia de desarrollo tecnológico](../22-desarrollo-tecnologico.md)
- [Hoja de ruta](../23-hoja-de-ruta.md)

## Decisiones candidatas no confirmadas en el documento fuente

Durante el análisis se evaluó si el plan original establece una decisión explícita sobre la **futura incorporación de pollo de engorda (broilers)** como línea adicional de negocio. El documento fuente compara ponedoras contra pollo de engorda únicamente para justificar el inicio con ponedoras (sección 4.1–4.2) y no contiene ninguna declaración explícita sobre incorporar broilers en una etapa posterior. Por lo tanto, **no se registra como decisión** para evitar inventar contenido no presente en el original. Se deja anotado como punto de revisión humana pendiente.

---

## Navegación

- [Índice general](../README.md)
- [Documento anterior: Conclusiones y decisión recomendada](../27-conclusiones-y-decision.md)
- [Documento siguiente: Fuentes técnicas de referencia](./fuentes-de-referencia.md)
