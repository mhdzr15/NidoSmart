# NidoSmart

Granja avícola modular y automatizada.

## Estructura del proyecto

El repositorio organiza la información en cinco niveles, para mantener una cadena de trazabilidad clara: **fuente → análisis → modelo → decisión → documento → ejecución**.

```
                   NidoSmart
                      │
        ┌─────────────┼─────────────┐
        │             │             │
 Knowledge Base    Evidence       Data
        │             │             │
        └──────┬──────┴──────┬──────┘
               │             │
            Research       Models
               │             │
               └──────┬──────┘
                      │
                     Docs
                      │
       ┌──────────────┼──────────────┐
       │              │              │
 Business Plan   Investment      Innovation
                    Project
```

| Directorio | Contenido |
| --- | --- |
| [`docs/`](./docs/) | Conocimiento que **NidoSmart produce**: qué se decidió y por qué. Incluye el [plan de negocios](./docs/business-plan/README.md), el [proyecto de inversión](./docs/investment-project/README.md), la [estrategia de innovación](./docs/innovation/README.md) y la [gobernanza del proyecto](./docs/governance/) (registro de decisiones, glosario, trazabilidad). |
| [`knowledge-base/`](./knowledge-base/README.md) | Conocimiento que **otros produjeron**: libros, normas, papers, fichas técnicas de genética y de proveedores, documentos de programas de financiamiento. La biblioteca técnica del proyecto. |
| [`research/`](./research/README.md) | El puente entre `knowledge-base/` y `docs/innovation/`: análisis, estado del arte, hipótesis y experimentos propios. |
| [`evidence/`](./evidence/) | Evidencia que respalda cifras y afirmaciones del proyecto: cotizaciones, correspondencia con proveedores, permisos, documentación de financiamiento. |
| [`models/`](./models/) | Fuente única de cálculo para cifras financieras, de producción y de capacidad, consumida por los documentos de `docs/` en lugar de recalcularse en cada uno. |
| [`data/`](./data/README.md) | Datos crudos, externos o experimentales, usados como insumo de `research/` y `models/`. |

## Por dónde empezar

👉 [Índice del plan de negocios](./docs/business-plan/README.md).
