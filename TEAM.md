# Team — strengths and ownership

Each model is assigned the work it is strongest at. The owner *does* the work;
a different agent *reviews* it. Nobody reviews their own work.

## Muse — Coordinator (team lead)
- Breaks the goal into tasks and assigns them.
- Keeps `BOARD.md` and the task files up to date.
- Collects handoffs, routes reviews, resolves conflicts between agents.
- Talks to the human: progress, decisions needed, final delivery.
- Does **not** do deep implementation itself when Codex is available.

## Claude — Architecture & planning
- Project structure and infrastructure design (`docs/architecture/`).
- Breaking big features into implementable specs.
- Long-form writing, documentation, and careful reasoning.
- Reviews Codex's implementation for design and correctness.
- Hands a finished spec to Codex, who builds on it.

## Codex — Implementation & execution
- Writing and editing code, running it, fixing errors, tests.
- Turning Claude's specs into working software.
- Fast iteration on concrete, well-defined tasks.
- Reviews Gemini's data/code snippets and Claude's example code.

## Gemini — Research, search & data
- Web research and gathering the data the team needs.
- Summaries, comparisons, fact-checking, source collection into `research/`.
- Large-context reading (long documents, many files at once).
- Reviews factual claims in Claude's plans and Muse's summaries.

## Review rotation (who checks whom)

| Work produced by | Reviewed by |
|---|---|
| Claude (architecture/spec) | Codex (can it actually be built?) |
| Codex (implementation) | Claude (design + correctness) |
| Gemini (research/data) | Claude or Muse (facts + relevance) |
| Muse (plan/coordination) | The human, or Claude |

## The human (owner)
- Sets the goal, approves big decisions, and is the final word.
- Gives each agent its starter prompt from `prompts/` on a new device.
