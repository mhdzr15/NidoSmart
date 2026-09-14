---
title: "Índice general del plan de negocios"
project: "NidoSmart"
document_type: "business-plan"
status: "draft"
version: "1.2"
last_updated: "2026-09-13"
---

# NidoSmart — Plan de negocios

*Tecnología inteligente para producción avícola*

**Eslogan principal:** *Automatización que cuida, producción que crece.*

*Granja modular y automatizada de gallinas ponedoras en México*

**NidoSmart** es un proyecto de granja modular y automatizada de gallinas ponedoras en San Francisco Acatepec, municipio de San Andrés Cholula, Puebla, México. El plan propone iniciar con una primera unidad financiable de 640 aves —definida por la cotización vigente de jaula automatizada tipo H (ver [registro de cotizaciones](../../evidence/quotations/README.md))—, con automatización intensiva y una arquitectura modular que permita crecer progresivamente, por unidades completas de 640 aves, hasta 5,000 aves.

Este plan de negocios describe **cómo funciona el negocio**. Es complementario a otros dos conjuntos de documentos dentro de [`docs/`](../): el [proyecto de inversión](../investment-project/README.md), que describe cómo se financia la primera unidad, y la [estrategia de innovación](../innovation/README.md), que describe qué se investigará y desarrollará. Las decisiones estratégicas que afectan a más de uno de estos tres documentos se registran en [`docs/governance/registro-de-decisiones.md`](../governance/registro-de-decisiones.md).

## Propósito de esta documentación modular

Este directorio organiza el plan de negocios en documentos independientes agrupados por tema, para facilitar:

* Mantenimiento y actualización de cifras y supuestos sin editar todo el plan.
* Revisión y control de versiones por área (comercial, financiera, tecnológica, operativa).
* Navegación directa a un tema específico.
* Incorporación futura de nuevas etapas del negocio (por ejemplo, nuevas ubicaciones o líneas de producción) sin reestructurar el plan completo.
* Trabajo de agentes de IA sobre secciones concretas del plan.

La estructura documental se definió mediante análisis de contenido: no se partió de una plantilla genérica, sino de los temas, tablas, diagramas y decisiones propios del plan de negocios.

## Estado del documento

Borrador (`draft`), versión 1.2, actualizado el **2026-09-13**. Ver la sección [Revisión humana pendiente](#revisión-humana-pendiente) para los puntos señalados que aún requieren validación.

## Orden recomendado de lectura

1. [Resumen ejecutivo](./01-resumen-ejecutivo.md)
2. [Descripción del negocio](./02-descripcion-del-negocio.md)
3. [Justificación de la oportunidad](./03-mercado-y-oportunidad.md)
4. [Selección del modelo productivo](./04-modelo-productivo.md)
5. [Objetivos del proyecto](./05-objetivos.md)
6. [Modelo modular de crecimiento](./06-crecimiento-modular.md)
7. [Diseño físico preliminar](./07-diseno-fisico.md)
8. [Sistema de automatización](./08-automatizacion.md)
9. [Arquitectura eléctrica, hidráulica y de comunicaciones](./09-arquitectura-electrica-hidraulica-comunicaciones.md)
10. [Arquitectura tecnológica](./10-arquitectura-tecnologica.md)
11. [Evaluación técnica de Hermes Agent y Paperclip](./11-hermes-agent-y-paperclip.md)
12. [Funciones del agente inteligente](./12-funciones-agente-inteligente.md)
13. [Seguridad funcional y ciberseguridad](./13-seguridad-y-ciberseguridad.md)
14. [Modelo operativo](./14-modelo-operativo.md)
15. [Estrategia comercial](./15-estrategia-comercial.md)
16. [Producción y capacidad comercial](./16-produccion-y-capacidad-comercial.md)
17. [Plan financiero preliminar](./17-plan-financiero.md)
18. [Validación del piloto](./18-validacion-del-piloto.md)
19. [Regulación y cumplimiento](./19-regulacion-y-cumplimiento.md)
20. [Bioseguridad](./20-bioseguridad.md)
21. [Gestión de riesgos](./21-gestion-de-riesgos.md)
22. [Estrategia de desarrollo tecnológico](./22-desarrollo-tecnologico.md)
23. [Hoja de ruta](./23-hoja-de-ruta.md)
24. [Indicadores clave](./24-indicadores-clave.md)
25. [Organización inicial](./25-organizacion-inicial.md)
26. [Estrategia de inversión](./26-estrategia-de-inversion.md)
27. [Conclusiones y decisión recomendada](./27-conclusiones-y-decision.md)

### Documentos relacionados fuera de este directorio

* [Registro de decisiones](../governance/registro-de-decisiones.md) — decisiones estratégicas explícitas del plan, en formato DEC-XXX, con referencias cruzadas a los documentos donde se desarrollan.
* [Bibliografía](../../knowledge-base/bibliography.md) — instituciones, normas, marcas y desarrolladores considerados en la investigación.

## Descripción breve de cada documento

| # | Documento | Contenido |
| - | --- | --- |
| 1 | [Resumen ejecutivo](./01-resumen-ejecutivo.md) | Visión general del proyecto, principios rectores, cifras clave de inversión y arquitectura digital recomendada. |
| 2 | [Descripción del negocio](./02-descripcion-del-negocio.md) | Concepto del negocio, producto inicial, productos secundarios y propuesta de valor. |
| 3 | [Justificación de la oportunidad](./03-mercado-y-oportunidad.md) | Mercado mexicano del huevo, competencia industrial y canales comerciales prioritarios. |
| 4 | [Selección del modelo productivo](./04-modelo-productivo.md) | Comparación entre ponedoras y pollo de engorda, y decisión de iniciar con ponedoras. |
| 5 | [Objetivos del proyecto](./05-objetivos.md) | Objetivo general y objetivos específicos medibles del proyecto. |
| 6 | [Modelo modular de crecimiento](./06-crecimiento-modular.md) | Principio de modularidad, escala recomendada por etapas y criterios para agregar un módulo. |
| 7 | [Diseño físico preliminar](./07-diseno-fisico.md) | Dimensiones del módulo inicial, condiciones climáticas del sitio, áreas del predio y flujo operativo (diagrama Mermaid). |
| 8 | [Sistema de automatización](./08-automatizacion.md) | Procesos que deben automatizarse desde el inicio (alimentación, agua, iluminación, ambiente, huevo, gallinaza) y procesos que pueden permanecer manuales. |
| 9 | [Arquitectura eléctrica, hidráulica y de comunicaciones](./09-arquitectura-electrica-hidraulica-comunicaciones.md) | Sistema eléctrico, sistema hidráulico y arquitectura de comunicaciones, incluyendo conectividad a internet permanente. |
| 10 | [Arquitectura tecnológica](./10-arquitectura-tecnologica.md) | Principio de control crítico local, arquitectura propuesta (diagrama Mermaid), componentes de software, nota metodológica PLF y uso de Grafana. |
| 11 | [Evaluación técnica de Hermes Agent y Paperclip](./11-hermes-agent-y-paperclip.md) | Evaluación comparativa y decisión tecnológica entre Hermes Agent y Paperclip. |
| 12 | [Funciones del agente inteligente](./12-funciones-agente-inteligente.md) | Funciones de Hermes Agent en supervisión productiva, monitoreo ambiental, inventario, mantenimiento, comercialización y gestión documental. |
| 13 | [Seguridad funcional y ciberseguridad](./13-seguridad-y-ciberseguridad.md) | Regla de acceso, acciones permitidas y restringidas del agente, y controles de ciberseguridad requeridos. |
| 14 | [Modelo operativo](./14-modelo-operativo.md) | Rutinas diaria, semanal y mensual de operación. |
| 15 | [Estrategia comercial](./15-estrategia-comercial.md) | Posicionamiento de marca, modelo de venta, planes de suscripción y política de precios. |
| 16 | [Producción y capacidad comercial](./16-produccion-y-capacidad-comercial.md) | Estimación de producción anual, mensual, semanal y diaria, y su equivalencia en presentaciones comerciales. |
| 17 | [Plan financiero preliminar](./17-plan-financiero.md) | Inversión inicial, supuestos, proyección a tres años, interpretación y escenarios conservador/base/optimista. |
| 18 | [Validación del piloto](./18-validacion-del-piloto.md) | Objetivo financiero y de validación del piloto: razonamiento, alcance del OPEX, las cuatro validaciones, margen de contribución y criterios de éxito antes de crecer. |
| 19 | [Regulación y cumplimiento](./19-regulacion-y-cumplimiento.md) | Marco regulatorio general y trámites específicos para San Francisco Acatepec, San Andrés Cholula, Puebla. |
| 20 | [Bioseguridad](./20-bioseguridad.md) | Medidas mínimas de bioseguridad y respuesta ante anomalías. |
| 21 | [Gestión de riesgos](./21-gestion-de-riesgos.md) | Tabla de riesgos, impactos y mitigaciones del proyecto. |
| 22 | [Estrategia de desarrollo tecnológico](./22-desarrollo-tecnologico.md) | Enfoque technology-first business-validated, tecnología previa al ingreso de las aves, MVP tecnológico (NidoSmart Core) y secuencia de desarrollo en cinco etapas. |
| 23 | [Hoja de ruta](./23-hoja-de-ruta.md) | Fases 0 a 5 del proyecto, desde prefactibilidad hasta la escala de 2,500–5,000 aves, y próximos pasos inmediatos. |
| 24 | [Indicadores clave](./24-indicadores-clave.md) | Indicadores productivos, ambientales, comerciales, financieros y técnicos. |
| 25 | [Organización inicial](./25-organizacion-inicial.md) | Estructura ligera de dirección, operación, veterinario externo y soporte técnico durante la etapa de la primera unidad (640 aves). |
| 26 | [Estrategia de inversión](./26-estrategia-de-inversion.md) | Elementos que no deben sacrificarse, elementos que pueden aplazarse y prioridad de automatización por riesgo. |
| 27 | [Conclusiones y decisión recomendada](./27-conclusiones-y-decision.md) | Factores críticos de éxito, decisión recomendada de doce puntos y conclusión general del plan. |

## Convenciones para actualizar el plan

* Cada archivo mantiene un bloque de metadatos YAML al inicio (`title`, `project`, `document_type`, `status`, `version`, `last_updated`, `source`). Actualiza `last_updated` y, si corresponde, `version` al modificar un documento.
* Cada archivo tiene un único encabezado `#`, secciones principales con `##` y subsecciones con `###`, conservando la numeración original de subsecciones (por ejemplo, `## 17.6.3`) para mantener la trazabilidad con el archivo fuente.
* Cuando una cifra, tabla o criterio sea utilizado por más de un documento, colócalo en el documento más apropiado (su fuente única) y enlaza desde los demás en lugar de duplicarlo. Ejemplos ya aplicados: los criterios de éxito del piloto viven en [Validación del piloto](./18-validacion-del-piloto.md) y se enlazan desde [Modelo modular de crecimiento](./06-crecimiento-modular.md).
* Usa enlaces relativos explícitos (`[texto](./archivo.md#ancla)`) en lugar de referencias vagas como "véase más adelante".
* Cada documento termina con una sección `## Navegación` con enlaces al índice y, cuando existan, al documento anterior y siguiente en el orden de lectura.
* No dupliques contenido del [registro de decisiones](../governance/registro-de-decisiones.md); si tomas una nueva decisión estratégica, agrégala ahí con el formato `DEC-XXX` y enlázala desde el documento temático correspondiente.

## Instrucciones para agregar nuevos documentos

1. Usa nombres de archivo en `kebab-case`, con prefijo numérico de dos dígitos si el documento forma parte de la secuencia principal de lectura (por ejemplo, `28-nueva-seccion.md`). Si es material de referencia, técnico o de detalle que no pertenece a la secuencia principal, colócalo en [`docs/governance/`](../governance/) (decisiones, glosario, trazabilidad) o en [`knowledge-base/`](../../knowledge-base/) (bibliografía y fuentes técnicas) según corresponda.
2. Agrega el bloque de metadatos YAML al inicio, con `source` apuntando al documento o proceso del que proviene el contenido.
3. Añade el documento a la lista de "Orden recomendado de lectura" y a la tabla de "Descripción breve" de este README, en la posición que corresponda.
4. Actualiza la sección `## Navegación` del documento anterior y del documento siguiente en la secuencia para mantener los enlaces `anterior`/`siguiente` correctos.
5. Si el documento introduce una decisión estratégica nueva, regístrala en el [registro de decisiones](../governance/registro-de-decisiones.md).

## Fecha de reorganización

2026-07-12.

## Revisión humana pendiente

* **Futura incorporación de pollo de engorda (broilers):** el documento original no contiene una decisión explícita sobre incorporar broilers como línea futura; sólo compara ponedoras contra engorda para justificar el inicio con ponedoras. No se registró como decisión para evitar inventar contenido. Ver nota en el [registro de decisiones](../governance/registro-de-decisiones.md#decisiones-candidatas-no-confirmadas-en-el-documento-fuente).
* **Numeración de subsecciones corregida:** en el original, la sección 23 ("Indicadores clave") tenía subsecciones numeradas 22.1–22.5, y la sección 25 ("Estrategia de inversión") tenía subsecciones numeradas 24.1–24.3. Se trata de un desfase tipográfico evidente (probablemente por una inserción o eliminación de sección durante la edición del documento original) y se corrigió a 23.1–23.5 y 25.1–25.3 respectivamente en [Indicadores clave](./24-indicadores-clave.md) y [Estrategia de inversión](./26-estrategia-de-inversion.md). El contenido no fue alterado, sólo la numeración de los encabezados.
* **Precisión de la producción comercializable año 1:** el plan usa dos niveles de precisión para la misma cifra —un rango de 30,000–31,000 huevos/año en [Producción y capacidad comercial](./16-produccion-y-capacidad-comercial.md) y un valor puntual de 30,660 huevos en los supuestos y la proyección de [Plan financiero preliminar](./17-plan-financiero.md)—. El valor puntual cae dentro del rango, por lo que no se trata de una contradicción, pero ambos niveles de precisión se conservaron intactos y se anotaron para que una revisión financiera confirme cuál debe tratarse como cifra de referencia.
* **Fuentes técnicas de referencia:** la lista en [Fuentes técnicas de referencia](../../knowledge-base/bibliography.md) identifica instituciones, normas y marcas, pero no tiene formato de bibliografía con fecha de consulta o edición específica. Queda pendiente completarla si se requiere una bibliografía formal.
* **Cifras de inversión y financieras:** todas las cifras de CAPEX, OPEX, precios y proyecciones están marcadas en el plan original como estimaciones preliminares, no cotizaciones. Requieren validación con proveedores y con un modelo financiero detallado antes de tomar decisiones de inversión, tal como señala el propio plan en [Plan financiero preliminar](./17-plan-financiero.md).
* **Viabilidad regulatoria del predio:** [Regulación y cumplimiento](./19-regulacion-y-cumplimiento.md) señala que la viabilidad regulatoria del predio en San Francisco Acatepec debe confirmarse formalmente antes de iniciar cualquier obra; esto sigue pendiente de validación local.

---

## Navegación

- [Documento siguiente: Resumen ejecutivo](./01-resumen-ejecutivo.md)
