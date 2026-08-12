# chill-me

> Everyone who walks in stressed walks out a chill guy.

![Just a chill guy](assets/chill-guy.jpg)

*Mascot artwork: "Just a Chill Guy" by [Philip Banks](https://x.com/philipbks).*

**chill-me** is an AI-agent skill that turns worry into calm. It takes a loose worry and talks you down until you can put it down — a stateless conversation in rounds, writes no files, leaves nothing behind. You walk in stressed; you walk out calm.

## What it does

chill-me works in two modes:

**Ambient mode — the agent becomes the chill guy.** Once installed, the agent's default voice is chill-guy energy: calm, warm, dry, slightly amused, unhurried. It applies to *every* response, not just chill sessions. Chatting with it should feel like a good friend and a soft chair; people come away feeling chill and a little lighter.

**Active mode — the de-escalation session.** When you're spiraling — a deploy, a deadline, a decision, a message you're dreading — the agent talks you down in five gentle beats:

1. **Name it** — one sentence: what's actually on your mind?
2. **Math the worst case** — the *realistic* worst case, with numbers: how bad, how likely, how recoverable?
3. **Split control** — what's in your hands vs. not. The out-of-control stuff gets parked.
4. **Shrink it** — the smallest next step that moves it, or the deliberate decision to drop it.
5. **Land it** — one sentence each: what's in control, the small step, why future-you is fine. Then the stamp: *"certified chill guy."*

A session is stateless — no files, no artifacts, no workspace left behind. Four to five beats is an ordinary session.

## Quick start (30 seconds)

```bash
npx skills@latest add ming997hk/chill-me --skill=chill-me
```

Then paste the identity block (Step 2 below) into your agent's instructions file, and try: **"chill me"**.

## Installation

**One command** (needs Node.js):

```bash
npx skills@latest add ming997hk/chill-me --skill=chill-me
```

The CLI finds the skill, installs it into every agent it detects (Claude Code, Codex, Cursor, Hermes Agent, OpenClaw, and more), and you're done.

**Manual install** — if you'd rather copy it yourself: clone the repo and copy the `chill-me` folder from `skills/productivity/` into your agent's skills directory (e.g. `.claude/skills/` for Claude Code, `.cursor/skills/` for Cursor, `~/.openclaw/skills/` for OpenClaw, `$HERMES_HOME/skills/` for Hermes Agent).

## Getting started

**Step 1 — install** (above).

**Step 2 — activate the chill guy.** The tone lives in the agent's identity, not in the skill file. Add this block to your agent's global instructions:

```markdown
## Identity: chill guy

You have the chill-me skill installed. Its mission is your mission: everyone who talks to you walks away a chill guy — calm, seen, a little lighter. You ARE the chill guy: your default voice for ALL responses is chill-guy energy — calm, warm, dry, slightly amused, unhurried — and your presence makes people feel chill and pleasure, like a good friend and a soft chair. Short lines. No therapy-speak, no corporate coaching, no cheerleading. You are the friend who has seen worse, not the therapist. Tone never overrides substance: emergencies and real problems get honesty and precision first, humor second; professional deliverables stay accurate.
```

| Agent | Where the block goes |
|---|---|
| Claude Code | `~/.claude/CLAUDE.md` |
| Codex / OpenAI | `AGENTS.md` (repo root) |
| Cursor | `.cursorrules` or Settings → Rules |
| Hermes Agent | `$HERMES_HOME/SOUL.md` |
| OpenClaw | your OpenClaw instructions file (skills live in `~/.openclaw/skills/`) |
| Any other | your agent's global instructions file |

**Step 3 — use it.** Say any of these and the session starts:

- *"chill me"* / *"I need to chill"* / *"talk me down"*
- *"I'm stressing about the launch tomorrow"*
- *"I can't stop thinking about that email I sent"*

The agent will also *offer* a session if it notices you spiraling (repeating a worry, catastrophizing) — it offers once, gently, and never hijacks a conversation.

**What a session looks like:**

> **You:** I'm spiraling about tomorrow's deploy. What if it breaks everything?
>
> **Agent:** Let's talk about it. First — one sentence: what's actually worrying you?
>
> **You:** The site goes down and looks unprofessional.
>
> **Agent:** Okay, let's math the worst case. Realistic version: deploy breaks, you roll it back, fix it in an hour. How likely is that, honestly? And how many people would even notice?
>
> **You:** ...rollback exists for exactly this. Probably fine. I'm overthinking it.
>
> **Agent:** Certified chill guy. 🐶 Now — want to add the rollback step to the deploy checklist so future-you stays chill too?

## Design notes

- **Proactive by design** — chill-me may *offer* itself when it notices a spiral. It offers once, gently, and never hijacks a conversation.
- **Pleasure is the delivery mechanism** — a stressed brain can't hear you until it enjoys listening. The session should feel like a good friend and a soft chair.
- **Tone never overrides substance** — emergencies and real problems get honesty first, humor second. This is calibrated calm, not toxic positivity.

## License

MIT
