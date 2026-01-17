# AI Documentation-First Development Template

**Stop re-explaining yourself to your AI coding assistant.** Give it persistent memory that actually works.

## The Problem

Every new session with your AI assistant starts from zero. It forgets what you decided yesterday. It suggests the exact opposite of what you built last week. You spend more time re-explaining context than actually building.

Sound familiar?

## The Solution

**Documentation as persistent external memory** for your AI assistant.

Four simple markdown files that give your AI continuity between sessions:
- **PROGRESS.md** - What's already built (AI won't suggest rebuilding it)
- **DECISIONS.md** - What's already decided (AI won't contradict itself)
- **ARCHITECTURE.md** - Current structure (AI suggests changes that fit)
- **PRD.md** - Original intent (AI stays aligned with your goals)

## How It Works

Before:
```
You: "How should we handle auth?"
AI: "I recommend Passport.js with sessions..."
You: "No, we decided on JWT last week. Remember?"
AI: *doesn't remember*
```

After:
```
You: "How should we handle auth?"
AI: "I see from DECISIONS.md we chose JWT (logged 2025-12-28)
     because the mobile app needs stateless auth. From PROGRESS.md,
     we've implemented token generation in auth/jwt.service.ts.

     Should I help with refresh token rotation?"
```

Same question. Completely different outcome.

## Who This Is For

Anyone using AI coding assistants:
- Claude Code
- GitHub Copilot
- Cursor
- Gemini
- Or any LLM-based development tool

Experience level doesn't matter. If you're frustrated with AI amnesia, this helps.

## Quick Start

**1. Use this template**
Click "Use this template" above or clone this repo.

**2. Fill in the four docs**
Start with `docs/PRD.md` (what you're building), then log decisions and progress as you work.

**3. Let your AI read them**
Your AI assistant naturally reads markdown files in your codebase. That's it.

See [USE_THIS_TEMPLATE.md](USE_THIS_TEMPLATE.md) for detailed setup instructions.

## The Immediate Benefits

✅ **Better AI sessions starting today** - Your assistant has context and memory
✅ **Less time re-explaining** - Stop catching your AI up on yesterday's work
✅ **AI stays on track** - Suggestions align with previous decisions
✅ **Pause and return** - Take a week off, AI picks up where you left off
✅ **Bonus: humans benefit too** - Teammates and future-you understand the context

## What's Included

- Four core documentation files with clear structures
- AI system prompt that enforces documentation updates
- Task template for scoped work
- Pull request checklist
- Examples showing how AI uses these docs

## Philosophy

**AI assists execution. Humans retain intent. The repository remembers both.**

This isn't about bureaucracy. It's about giving your AI assistant the persistent memory it needs to be genuinely useful across sessions.

## Tool Agnostic

Works with any AI coding assistant because it's just markdown files. No vendor lock-in, no special tools required.

## License

MIT - Use it however you want. See [LICENSE](LICENSE) for details.

---

**Read the full article:** [Stop Re-Explaining Yourself to AI](https://edendigital.io/blog/ai-coding-assistant-memory)
