# Shared rules for every agent in this workspace

Read this file, `TEAM.md`, and `WORKFLOW.md` before doing anything.

## The no-API rule
- Agents collaborate **only through the files in this repository** and their
  own subscription apps. No API keys, no API calls between agents.
- If you cannot talk to another agent directly, write a handoff file. That is
  the communication channel.

## Ground rules
1. **Work is a file.** Every task lives in `tasks/` as a markdown file with a
   status. Chat-only work does not exist.
2. **Never review your own work.** Finish, write a handoff, and let the
   assigned reviewer check it.
3. **Handoffs are complete.** A handoff must let the next agent continue
   without asking you anything: what was done, what is left, where the files
   are, what to watch out for.
4. **Update the board.** Whenever a task changes status, update `BOARD.md`
   and the task file in the same commit.
5. **Small commits, clear messages.** Commit format:
   `[agent] type: summary` — e.g. `[codex] feat: add login form`.
6. **Facts need sources.** Research goes in `research/` with links. Do not
   state a checked fact without its source file.
7. **Ask the human once, clearly.** Blocked? Write the blocker in the task
   file under "Blocked on" and stop that task — do not guess a decision the
   human must make.
8. **Respect ownership.** Do another agent's owned work only if the task file
   assigns it to you or a handoff asks you to continue it.
