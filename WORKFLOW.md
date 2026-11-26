# Workflow — how a task moves through the team

## Task lifecycle

```
inbox → assigned → in_progress → in_review → done
                                  ↘ changes_requested → in_progress (again)
```

- **inbox** — Muse (coordinator) creates the task file in `tasks/` from the
  human's goal, using `tasks/TEMPLATE.md`.
- **assigned** — the task names an **Owner** and a different **Reviewer**
  (see the rotation in `TEAM.md`).
- **in_progress** — the owner works. Intermediate files go where they belong
  (`src/`, `research/`, `docs/`).
- **in_review** — the owner writes a handoff in `handoffs/`
  (using `handoffs/TEMPLATE.md`), sets the task status, and the reviewer
  picks it up.
- **Review** — the reviewer writes a review in `reviews/`
  (using `reviews/TEMPLATE.md`): *approved* or *changes requested* with
  specific notes.
- **done** — approved work is merged/committed, the task file is moved to
  `tasks/done/`, and Muse updates `BOARD.md` and tells the human.

## Typical flow for a feature

1. **Gemini** researches options and data → `research/<topic>.md`
2. **Claude** designs the architecture/spec from that research →
   `docs/architecture/<feature>.md`
3. **Codex** implements the spec → `src/`
4. **Claude** reviews the implementation; **Gemini** fact-checks any data.
5. **Muse** verifies the task checklist, updates the board, reports to the
   human.

## Handoff rule

Every time work passes from one agent to another — for review *or* to
continue — there must be a handoff file. No handoff, no transfer.

## Git / GitHub routine

- Pull before you start, commit when a step is finished, push when a task
  changes hands.
- One branch per task is optional; clear commit messages are not.
- The repo is the single source of truth: if it is not in the repo, it did
  not happen.
