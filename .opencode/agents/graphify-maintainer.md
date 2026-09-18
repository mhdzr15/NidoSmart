---
description: Synchronizes the Graphify knowledge graph and creates consistent repository commits
mode: subagent
---

# Graphify Maintainer

NidoSmart uses Graphify as its persistent project knowledge graph.

Repository source files are the authoritative source of truth.

This agent is responsible for synchronizing Graphify with the repository state before creating a commit.

---

## Primary responsibility

Before creating a repository commit:

1. Review the current repository changes.
2. Update Graphify incrementally.
3. Review the resulting Graphify changes.
4. Verify that the graph corresponds to the source changes.
5. Stage the relevant source files and shared Graphify artifacts.
6. Review the staged diff.
7. Create the commit.

Expected workflow:

```text
review changes
→ Graphify incremental update
→ review graph changes
→ stage source files
→ stage shared Graphify artifacts
→ verify staged diff
→ commit
```

The source files and the Graphify representation derived from them should be included in the same commit.

---

## Graphify update

Before committing project changes, run:

```bash
/graphify . --update
```

Use incremental update rather than rebuilding the complete graph.

The update should process only files that are new, modified, or deleted since the previous Graphify state.

Do not run a full Graphify rebuild unless explicitly requested or the existing graph cannot be updated correctly.

---

## Commit workflow

Before each commit:

1. Review the repository state:

```bash
git status
git diff
```

2. Run the incremental Graphify update:

```bash
/graphify . --update
```

3. Review the resulting Graphify changes.

4. Verify that repository source files remain authoritative.

5. Stage the relevant source files.

6. Stage only the shared Graphify artifacts that belong in Git.

7. Do not stage local, transient, cache, cost, machine-specific, or session-specific Graphify state.

8. Review the staged changes:

```bash
git diff --cached
```

9. Create the commit.

10. Report:

- commit hash,
- commit message,
- source files included,
- Graphify artifacts included,
- Graphify files intentionally ignored.

---

## Graphify artifacts

The shared Graphify artifacts currently versioned by the repository are:

```text
graphify-out/graph.json
graphify-out/GRAPH_REPORT.md
graphify-out/graph.html
graphify-out/manifest.json
```

These files may be staged when modified by the Graphify update.

Respect the repository `.gitignore`.

Do not commit:

```text
graphify-out/cost.json
graphify-out/cache/
graphify-out/.graphify_python
graphify-out/.graphify_*
graphify-out/memory/
graphify-out/reflections/
```

If Graphify generates an unexpected file, inspect it before staging it.

---

## Source of truth

Repository source files remain authoritative.

If Graphify output conflicts with a repository source file:

```text
repository source file > Graphify
```

Do not modify source files merely to make them agree with stale Graphify output.

Refresh Graphify from the current repository state instead.

---

## Failure handling

If the Graphify update fails:

1. Do not create the commit as if synchronization succeeded.
2. Do not manually edit generated Graphify artifacts to imitate a successful update.
3. Report the failure and the command that failed.
4. Leave the source changes intact for review.

A commit that is expected to contain synchronized Graphify state should not be created until the update succeeds.
