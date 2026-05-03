# AI Shared Brain — Starter Kit

Give your AI agent persistent memory using nothing but markdown files.

This is the system from the video: **[My AI and I Share a Brain — Here's How I Built It](https://youtube.com/@Jason_Cyr)**

## What This Is

A set of template files that create a "shared brain" between you and your AI agent. You both read and write to the same files. Over time, the agent builds genuine context about you, your work, and your preferences — without databases, fine-tuning, or custom code.

## Requirements

You need an AI agent that can **read and write files autonomously**. This won't work with ChatGPT or Claude's web interface — they can read uploads but can't write back to a file system.

**Tools that work:**
- [OpenClaw](https://openclaw.ai) — what I use (persistent agent with file access, messaging, tools)
- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) — Claude with full file system access
- [Codex](https://openai.com/index/codex/) — OpenAI's coding agent
- [Cursor](https://cursor.sh) / [Windsurf](https://codeium.com/windsurf) — AI-native code editors with file access

Any system where the AI can read files, write files, and run between sessions will work.

## Quick Start

1. Clone this repo into your agent's workspace
2. Edit `USER.md` with your details (name, timezone, role, preferences)
3. Edit `SOUL.md` to shape the agent's personality (or keep the default)
4. Review `AGENTS.md` — this is the operating manual that tells the agent how to use the shared brain
5. Start a session with your agent — it should read the files and begin building context
6. Give it a few days. The `MEMORY.md` and `memory/` folder will fill up on their own.

## File Structure

```
ai-shared-brain/
├── SOUL.md          # Layer 1: Agent identity — personality, boundaries, voice
├── USER.md          # Layer 1: Your identity — who the agent is helping
├── AGENTS.md        # Layer 1: Operating manual — startup ritual, rules, behavior
├── MEMORY.md        # Layer 2: Long-term memory — curated by the agent over time
├── memory/          # Layer 3: Episodic memory — daily notes
│   └── .gitkeep
└── README.md
```

## The 4 Layers

### Layer 1: Identity
**SOUL.md** — Who the agent is. Personality, communication style, boundaries.
**USER.md** — Who you are. Name, timezone, role, preferences. So the agent doesn't have to ask.
**AGENTS.md** — The operating manual. What to read on startup, when to write things down, how to behave.

### Layer 2: Long-Term Memory
**MEMORY.md** — Starts empty. The agent fills it over time with curated knowledge: key decisions, project context, your preferences, lessons learned. Think of it as the agent's distilled understanding of your world. The agent periodically reviews daily notes and promotes important things here.

### Layer 3: Episodic Memory
**memory/YYYY-MM-DD.md** — Daily notes. The agent creates one each day and logs what happened: what you worked on, decisions made, things to follow up on. These are the raw material that feeds long-term memory.

### Layer 4: Active Context (bring your own)
Connect your own knowledge base — Obsidian vault, Notion workspace, project folders, whatever you use. The agent reads from it to get real-time context on your work. This layer is yours to configure based on your setup.

## The Key Instruction

The entire system works because of one instruction in `AGENTS.md`:

> Before doing anything, read SOUL.md, USER.md, today's daily note, yesterday's daily note, and MEMORY.md.

That startup ritual is what creates continuity between sessions. Without it, the files are just files. With it, they're a shared brain.

## Tips

- **Give it time.** The system gets dramatically better after 2-3 weeks as memory accumulates.
- **Read MEMORY.md yourself.** It's a plain text file. You can see exactly what your AI "knows" about you. Correct it. Delete things. There's no black box.
- **The agent should write things down, not keep "mental notes."** If it doesn't write to a file, it won't remember next session.
- **Start simple.** A few lines in each file is enough. You'll naturally add more over time.

## About

Built by [Jason Cyr](https://jasoncyr.ca) — VP Design at Cisco, building AI systems for real work.

- YouTube: [@Jason_Cyr](https://youtube.com/@Jason_Cyr)
- LinkedIn: [jasncyr](https://linkedin.com/in/jasncyr)
- Substack: [jasoncyr.substack.com](https://jasoncyr.substack.com)
