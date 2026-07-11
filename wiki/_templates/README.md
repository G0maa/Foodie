# Templates

Reusable skeletons. Copy, don't edit these in place.

## Work-item hierarchy (Linear)

```
Epic  →  Issue (story)  →  Task
```

| Template | Maps to in Linear | Is | Source of truth for |
| --- | --- | --- | --- |
| [epic.md](./epic.md) | Project (or parent issue) | A feature area (Cart, Order) | Scope & value |
| [issue.md](./issue.md) | Issue | A shippable slice that implements a use case | Acceptance criteria |
| [task.md](./task.md) | Sub-issue | A technical step of an issue | Definition of done |

The **use-case template** lives with the use cases: [`../use-cases/_use-case-template.md`](../use-cases/_use-case-template.md).

## How these relate to the wiki

- The **wiki** holds the *design* (use cases, ERD, diagrams) — the what & why.
- **Linear** holds the *work* (status, owner, estimate) — the who & when.
- **Link, don't copy.** An issue links back to its wiki use case; its acceptance
  criteria are the *testable distillation* of that use case's flows — not a paste
  of the whole spec (which would drift).
