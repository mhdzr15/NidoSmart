# Project

NidoSmart is a growing technical, business, investment, and R&D project.

The repository contains:

- business planning,
- investment project documentation,
- technical specifications,
- quotations and supporting evidence,
- bibliography and regulations,
- research,
- innovation and R&D planning,
- governance and project decisions.

Because the project is large and continuously evolving, conversation context alone must not be treated as reliable project memory.

Graphify is the project's persistent knowledge graph and should be used to recover relevant context from previous work.

Repository source files remain the authoritative source of truth. Graphify is a retrieval and context layer used to locate relevant knowledge, relationships, and prior decisions; it does not replace the underlying files.

---

## Core working principle

For every substantial task:

1. Understand the current objective.
2. Identify what prior project knowledge may affect it.
3. Query Graphify with one or more focused questions.
4. Use the graph results to identify the relevant source files.
5. Inspect those source files before making decisions or modifications.
6. Perform the task.
7. Validate the result against related decisions, documents, and dependencies.
8. Update the repository when required.
9. If project knowledge changed, update Graphify.
10. Verify that the graph reflects the new project state before moving to the next substantial task.

The expected workflow is:

```text
objective
→ Graphify query
→ relevant context
→ source files
→ analysis
→ model
→ decision
→ document
→ Graphify update
→ next objective

```

---

## Graphify commands

- **Build the graph initially**
```bash
/graphify .
```
Generates `graphify-out/graph.json`, `GRAPH_REPORT.md`, and the visualization.

- **Update only what has changed**
```bash
/graphify . --update
```
or from the terminal:
```bash
graphify update .
```

- **Query the project memory**
```bash
graphify query "specific question"
```
Example:
```bash
graphify query "What unresolved issues remain in the poultry house specification?"
```

- **Explain a node or concept**
```bash
graphify explain "concept"
```

- **Find the relationship between two elements**
```bash
graphify path "ElementA" "ElementB"
```

- **Keep the graph automatically updated for code**
```bash
graphify hook install
```
and check it with:
```bash
graphify hook status
```
Note: the post-commit hook updates code changes but **ignores docs/images**, so for NidoSmart you still need to run `/graphify . --update` when modifying documentation.
