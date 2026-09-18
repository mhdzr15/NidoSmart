# Project

NidoSmart uses Graphify as its persistent project knowledge graph.

Repository source files are the authoritative source of truth.

OpenCode is responsible for maintaining Graphify synchronization as part of the Git commit workflow.

---

## Primary responsibility

Before creating a project commit, ensure that Graphify reflects the repository state that will be committed.

Expected workflow:

```text
review project changes
→ determine whether project knowledge changed
→ update Graphify when required
→ review Graphify changes
→ stage source files
→ stage shared Graphify artifacts
→ commit
```

The objective is that each relevant commit contains a Graphify representation consistent with the source files in that commit.

---

## When Graphify must be updated

Update Graphify when the changes modify project knowledge, including:

- documentation,
- technical specifications,
- project decisions,
- research,
- investment assumptions,
- financial assumptions,
- bibliography,
- regulations,
- supplier information,
- quotations or evidence,
- relationships between project elements.

For these changes, run:

```bash
graphify update .
```

or, when appropriate:

```bash
/graphify . --update
```

Do not rebuild the complete graph unnecessarily.

---

## When Graphify does not need to be updated

Do not update Graphify merely because a commit is being created if the changes do not affect project knowledge.

Examples may include changes that are purely local, transient, or unrelated to information represented in the project graph.

Inspect the diff before deciding whether an update is required.

---

## Commit workflow

Before each commit:

1. Review:

```bash
git status
git diff
```

2. Determine whether the changes affect project knowledge.

3. If project knowledge changed, run:

```bash
graphify update .
```

4. Review the resulting Graphify changes.

5. Verify that the graph update corresponds to the source changes being committed.

6. Stage the relevant source files.

7. Stage the shared Graphify artifacts that belong in Git.

8. Do not stage local, transient, cache, cost, or machine-specific Graphify state.

9. Review the staged diff:

```bash
git diff --cached
```

10. Create the commit.

The source changes and the corresponding Graphify update should normally be included in the same commit.

---

## Graphify artifacts

Version the shared Graphify artifacts defined by the repository's Graphify versioning policy.

Do not commit local or transient Graphify state.

Respect the repository `.gitignore`.

If unexpected Graphify files appear, do not commit them automatically. Inspect them first.

---

## Graph consistency

Repository files remain authoritative.

If Graphify output conflicts with the source files:

1. treat the repository files as correct,
2. refresh Graphify,
3. inspect the result,
4. do not alter source files merely to match stale graph output.

---

## Graphify commands

### Build the graph

Use only when an initial build or explicit rebuild is required:

```bash
/graphify .
```

### Incremental update

Preferred during normal project work:

```bash
graphify update .
```

or:

```bash
/graphify . --update
```

### Hook management

```bash
graphify hook install
```

Check hook status with:

```bash
graphify hook status
```

The post-commit hook does not replace the explicit Graphify update required for documentation-heavy NidoSmart changes.
