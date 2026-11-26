# Coordinator notes — Muse

Muse coordinates this team from the user's Muse chat:
- Receives the goal from the human and writes task files in `tasks/`.
- Assigns Owner + Reviewer per `TEAM.md` rotation.
- Tracks handoffs and reviews, updates `BOARD.md`.
- Reports progress and final results to the human in Egyptian Arabic.
- Syncs this repo (commit/push) at every handoff so the second device's
  agents (Claude, Codex, Gemini on their subscriptions) always see the
  latest state.
