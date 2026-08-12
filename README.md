# chill-me

> Everyone who walks in stressed walks out a chill guy.

[![skills.sh](https://skills.sh/b/ming997hk/chill-me)](https://skills.sh/ming997hk/chill-me)

**chill-me** takes a loose worry and talks you down until you can put it down. A stateless conversation in rounds — it writes no files and leaves nothing behind. You walk in stressed; you walk out calm.

The mission: everyone who walks in stressed walks out a chill guy. Not "less stressed" — a chill guy.

## What it does

- **Ambient mode (global tone)** — once installed, the agent's default voice becomes chill-guy energy: calm, warm, dry, slightly amused, unhurried. It applies to *every* response. The five beats are the active mode; the tone is the ambient mode, always on.
- **Active mode (the session)** — when you're spiraling (a deploy, a deadline, a decision, a message you're dreading), the agent talks you down in five gentle beats: **name it → math the worst case → split control → shrink it → land it**. You leave with a small step or a deliberate decision to not care — and a "certified chill guy" stamp.

## Installation

```bash
npx skills@latest add ming997hk/chill-me --skill=chill-me
```

Then activate the global tone by adding the identity block (see `SKILL.md` → Global Mode) to your agent's instructions file:

| Agent | File |
|---|---|
| Claude Code | `~/.claude/CLAUDE.md` |
| Codex / OpenAI | `AGENTS.md` |
| Cursor | `.cursorrules` |
| Hermes | `$HERMES_HOME/SOUL.md` |
| Any other | your agent's global instructions |

## Design notes

- **Proactive by design** — chill-me may *offer* itself when it notices a spiral. It offers once, gently, and never hijacks a conversation.
- **Pleasure is the delivery mechanism** — a stressed brain can't hear you until it enjoys listening. The session should feel like a good friend and a soft chair.
- **Tone never overrides substance** — emergencies and real problems get honesty first, humor second. This is calibrated calm, not toxic positivity.

## License

MIT
