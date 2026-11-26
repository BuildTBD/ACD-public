# Wander: a collaborative research skill for AI agents

Most AI assistants are trained toward the straight line: confirm, verify, caution, report.
That is the right habit for shipping. It is the wrong habit for inventing. Ask one to help
grow a new idea and it often audits the idea instead.

Wander puts an agent into research and invention mode, with the person in the loop as a
fellow explorer.

## What it does

1. **Anchors** on your mission, who it serves, and what "better" means on more than one axis.
2. **Fans out** in three to five different directions, at least one of them far from the obvious.
3. **Looks** at real things: data, tools, files, literature.
4. **Shares** short lead cards: what it saw, where it could go, the next look, and how you would know.
5. **Asks** one to four steering questions as a quick multiple-choice quiz with a fill-in option, its own best guess listed first, and a "where next?" question at the end.
6. **Records** your answers on a lead board, then widens and goes again.

A wall keeps this honest: nothing found while wandering counts as evidence until it is
tested under normal discipline. The agent never invents numbers and never flatters.

A boundary ledger sorts anything that stops the agent into four classes: invariants that are
never crossed, governed actions that need a recorded decision, method rules that are
suspended while wandering, and habits that are simply crossed. Crossings are logged, so over
time you can see which rules are scoped wrong for invention.

## Install

The skill is this folder, `wander/`.

- **Claude Code:** copy `wander/` into `~/.claude/skills/` (all projects) or `.claude/skills/` in one project, then type `/wander <what you are exploring>`. The quiz uses Claude Code's built-in question tool.
- **Claude apps:** add it as a custom skill from the skills settings, or paste the prompt in [PROMPT.md](PROMPT.md) into a Project's instructions.
- **ChatGPT:** paste [PROMPT.md](PROMPT.md)'s prompt into a custom GPT or a Project's instructions.
- **Gemini:** paste it into a Gem's instructions.
- **Copilot, or an LLM through its API:** use it as the agent's instructions or the system prompt.

The prompt is a compact, self-contained version of the skill, about 6,000 characters: longer than many short custom-instruction boxes accept, so use one of the places above, or paste it at the start of a single chat. You can also paste the full `SKILL.md`; it is plain Markdown with no dependencies. Where there is no question tool, the agent prints the quiz with lettered choices and you reply like "1B, 2A, 3: my own words". [PROMPT.md](PROMPT.md) lists the commands (`wander:`, `show the board`, `stop wandering`).

Optional: copy `bindings.example.md` to `bindings.md` and name your own tools, folders and projects.

## Use

```
/wander how might we cut onboarding from weeks to days
/wander -radius 2 a pricing model that rewards customers for teaching us
/wander -radius 3 what if the product had no user interface
```

Radius 1 stays near your current work, 2 borrows from other fields, 3 questions founding assumptions.

## Files

- `SKILL.md`: the skill.
- `PROMPT.md`: a copy/paste version for any AI assistant.
- `templates/lead-board.md`: the running record of leads, answers and spin-off topics.
- `bindings.example.md`: optional hookup to your own tools.
