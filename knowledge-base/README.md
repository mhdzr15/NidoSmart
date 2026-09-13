# Knowledge Base

Biblioteca técnica del proyecto: material que **otros produjeron** (libros, normas, manuales, papers, fichas técnicas de proveedores, documentos de programas de financiamiento) y que NidoSmart usa como fuente para tomar decisiones.

Esto se distingue de [`docs/`](../docs/), que contiene el conocimiento que **NidoSmart produce** a partir de estas fuentes.

## Por qué está dividido por tipo de autoridad

Un libro de producción avícola, una NOM y una ficha técnica de un proveedor no cumplen el mismo papel al momento de justificar una decisión: no tienen el mismo nivel de autoridad ni el mismo tipo de validez (académica, regulatoria, comercial). Por eso el material no vive todo junto en una sola carpeta genérica, sino separado por su naturaleza:

* [`books/`](./books/) — libros técnicos de referencia (por ejemplo, Bell & Weaver, *Commercial Chicken Meat and Egg Production*).
* [`genetics/`](./genetics/) — fichas técnicas de líneas genéticas (Hy-Line W-80, Ross 308, etc.).
* [`regulations/`](./regulations/) — normativa oficial y guías de buenas prácticas (NOM-159-SSA1-2016, manual de BPP, etc.).
* [`papers/`](./papers/) — artículos académicos, organizados por dominio de investigación (`plf/`, `computer-vision/`, `audio/`, `anomaly-detection/`, `optimization/`).
* [`financing/`](./financing/) — documentos de programas de financiamiento agropecuario (FIRA, FONAGA, NAFIN, programas estatales de Puebla).
* [`vendors/`](./vendors/) — cotizaciones técnicas, catálogos y especificaciones de proveedores, organizadas por categoría de producto (jaulas, sensores, controladores, control ambiental).

## Catálogo

Toda fuente relevante debe registrarse en [`bibliography.md`](./bibliography.md), con al menos: identificador, título, autor(es), año, tipo, áreas del proyecto donde se usa y estado de revisión. Esto evita citar de memoria y facilita que un agente de IA (o una persona nueva en el proyecto) sepa qué se ha consultado y dónde se usó.

## Uso esperado

Este material alimenta el análisis en [`research/`](../research/), que a su vez informa las decisiones registradas en [`docs/innovation/`](../docs/innovation/), [`docs/business-plan/`](../docs/business-plan/) y [`docs/governance/`](../docs/governance/). El conocimiento-base no debe copiarse ni resumirse dentro de los documentos de `docs/`; se enlaza desde ahí.
