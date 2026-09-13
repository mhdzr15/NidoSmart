# Research

Puente entre las fuentes externas de [`knowledge-base/`](../knowledge-base/) y las decisiones de investigación y desarrollo de [`docs/innovation/`](../docs/innovation/).

Este directorio es donde se **analiza** el material recopilado, antes de convertirlo en una decisión. Sin este paso intermedio se corre el riesgo de saltar directamente de "encontramos un paper" a "decidimos algo", sin haber comparado alternativas ni verificado si el problema ya está resuelto — exactamente lo que se busca evitar.

## Estructura

* [`state-of-the-art/`](./state-of-the-art/) — un documento por dominio tecnológico, con el análisis comparativo de lo que ya existe (académica y comercialmente) frente a lo que NidoSmart necesita.
* `literature-notes/` — notas individuales por fuente (paper, informe, caso de estudio), antes de sintetizarlas en un documento de estado del arte.
* `hypotheses/` — hipótesis de investigación propias de NidoSmart, derivadas del estado del arte, pendientes de validación experimental.
* `experiments/` — diseño y resultados de experimentos o pilotos que ponen a prueba esas hipótesis.

## Flujo de trabajo

```
knowledge-base/papers/<dominio>/   (fuentes en bruto)
        ↓
research/literature-notes/          (notas por fuente)
        ↓
research/state-of-the-art/<NN>-<dominio>.md   (análisis comparativo)
        ↓
docs/innovation/03-lineas-de-investigacion.md  (decisión: adoptar / adaptar / investigar)
```

Ejemplo: 30 papers sobre detección de anomalías en gallinas se archivan en `knowledge-base/papers/anomaly-detection/`, cada uno con su nota en `research/literature-notes/`, se sintetizan en `research/state-of-the-art/05-anomaly-detection.md`, y la línea de investigación resultante se registra en `docs/innovation/03-lineas-de-investigacion.md`.

## Plantilla para documentos de `state-of-the-art/`

Cada documento de esta carpeta debería seguir la misma estructura:

1. Problema
2. Soluciones académicas existentes
3. Soluciones comerciales existentes
4. Nivel de madurez
5. Limitaciones actuales
6. Aplicabilidad a NidoSmart
7. Clasificación: **Adoptar / Adaptar / Investigar**
8. Oportunidad de propiedad intelectual

La clasificación **Adoptar / Adaptar / Investigar** es el criterio central de esta carpeta: sólo lo que cae en "Investigar" justifica esfuerzo propio de I+D (NidoSmart Technology); lo que ya existe comercialmente (por ejemplo, alimentación automática) se adopta, y lo que existe pero requiere integrarse a la arquitectura propia (por ejemplo, PLC + MQTT) se adapta.
