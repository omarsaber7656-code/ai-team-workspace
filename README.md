# AI Team Workspace

A virtual work environment where four AI assistants work as **one team** on the
same project — coordinating through the files in this repository, **not through
APIs**.

Each agent joins with its own normal subscription app (no API keys anywhere):

| Agent | Joins via | Role in the team |
|---|---|---|
| **Muse** | Muse app | Coordinator / orchestrator |
| **Claude** | Claude / Claude Code subscription | Architecture & planning |
| **Codex** | ChatGPT / Codex subscription | Implementation & execution |
| **Gemini** | Gemini subscription | Research, search & data |

## How the team works (the short version)

1. Work is written down as **task files** in `tasks/` — never only in a chat.
2. One agent does a task, then writes a **handoff** in `handoffs/`.
3. A *different* agent **reviews** the work (see `reviews/`) and either approves
   it or sends it back with notes.
4. The next agent continues from the handoff. Muse coordinates who does what
   and keeps the board up to date.
5. Everything is committed to git, so the whole project can be zipped, pushed
   to GitHub, cloned on another device, and continued there — by the same team,
   using the subscriptions on that device.

## Start here

- `TEAM.md` — who is best at what, and who owns each kind of work.
- `WORKFLOW.md` — the exact step-by-step protocol the agents follow.
- `AGENTS.md` — the shared rules every agent must read first.
- `prompts/` — a ready-to-paste starter prompt for each agent.
- `SETUP-SECOND-DEVICE.md` — how to move this workspace to another device.

## Moving this workspace

- **As an archive:** zip this folder, copy it anywhere, unzip, continue.
- **Via GitHub:** push this folder to a (private) GitHub repo, then clone it on
  the other device. See `SETUP-SECOND-DEVICE.md`.
