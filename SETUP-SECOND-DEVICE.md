# Setting this team up on the second device

The second device already has subscriptions for Muse, ChatGPT (Codex),
Claude, and Gemini. No API keys are needed anywhere.

## 1. Get the workspace onto the device
Either:
- **GitHub:** clone the repo:
  `git clone <repo-url> ai-team-workspace`
- **Archive:** copy the zip, unzip it, and open the folder.

## 2. Open the folder in each agent's app
- **Claude Code** — open the folder as the project.
- **Codex** — open the folder as the project.
- **Gemini** (app or CLI) — give it the folder / the files for its task.
- **Muse** — this chat; the coordinator keeps its own copy in sync via git.

## 3. Give each agent its starter prompt
Open `prompts/` and paste the matching file into that agent's first chat:
- `prompts/claude.md` → Claude
- `prompts/codex.md` → Codex
- `prompts/gemini.md` → Gemini
- Muse already coordinates from this chat.

## 4. Start working
Tell Muse (the coordinator) the goal. Muse writes the first task files,
and the loop in `WORKFLOW.md` runs from there: research (Gemini) → design
(Claude) → build (Codex) → review (cross-agent) → Muse reports to you.

## 5. Keep devices in sync
Commit and push at every handoff. On the other device: pull before starting.
The repo — not any single chat — holds the team's memory.
