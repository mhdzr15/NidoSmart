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

Graphify is the project's persistent knowledge graph and must be used to recover relevant context from previous work.

Repository source files remain the authoritative source of truth. Graphify is a retrieval and context layer used to locate relevant knowledge, relationships, and prior decisions; it does not replace the underlying files.

---

## Working principle

For every substantial task:

1. Understand the current objective.
2. Identify what prior project knowledge may affect it.
3. Query Graphify with one or more focused questions.
4. Use the graph results to identify the relevant source files.
5. Inspect those source files before making decisions or modifications.
6. Perform the task.
7. Validate the result against related decisions, documents, and dependencies.
8. Update the repository when required.

Expected workflow:

```text
objective
→ Graphify query
→ relevant context
→ source files
→ analysis
→ model
→ decision
→ document
```

Do not rely solely on conversation memory when relevant project context may already exist in Graphify.

Do not search the entire repository when Graphify can first narrow the relevant context.

Avoid duplicating authoritative information across multiple files when a reference or link is sufficient.

---

## Graphify usage

Graphify is read-only from Claude's workflow.

Claude may use Graphify to:

- retrieve prior project context,
- recover previous decisions,
- identify unresolved issues,
- locate relevant documents,
- understand relationships between project elements,
- identify dependencies,
- recover supporting evidence and bibliography.

Claude must not rebuild or update the Graphify graph.

### Query project memory

Before starting substantial work, formulate one or more focused questions based on the current objective.

```bash
graphify query "specific question"
```

Example:

```bash
graphify query "What unresolved issues remain in the poultry house specification?"
```

Queries must be specific to the current task.

Prefer multiple focused queries over a generic project-wide query.

### Explain a concept

```bash
graphify explain "concept"
```

Use this when additional context about a specific graph element is needed.

### Find relationships

```bash
graphify path "ElementA" "ElementB"
```

Use this when the task requires understanding the relationship between project elements.

---

## Source of truth

Graphify is a retrieval layer, not the authoritative project record.

When Graphify returns relevant information:

1. identify the underlying source file,
2. inspect the source file when the information affects a decision or modification,
3. use the repository file as authoritative.

If Graphify and a source file disagree:

```text
repository source file > Graphify
```

Do not overwrite newer repository information based on stale graph content.

If relevant information is missing from Graphify, search the repository directly rather than assuming that the topic has never been addressed.

---

## Graph maintenance

Claude does not update Graphify.

Graph maintenance and synchronization are handled separately by OpenCode according to `AGENTS.md`.

Claude may modify project source files normally.

The updated project knowledge will be incorporated into Graphify during the repository commit workflow.
