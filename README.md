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

**Here's the key:** The AI maintains these documents as it works. You don't manually write them.

**During a session:**
```
You: "Build user registration with email validation"
AI: *builds the feature*
AI: *updates PROGRESS.md*: "Implemented user registration in components/RegisterForm.tsx"
AI: *updates DECISIONS.md*: "D-012 — Chose Zod for validation (integrates with React Hook Form)"
```

**Next session:**
```
You: "Add password validation to registration"
AI: *reads PROGRESS.md and DECISIONS.md first*
AI: "I can see the registration form uses Zod for validation.
     I'll add password rules to the existing schema."
```

The AI writes. The AI reads. You review and approve.

This is the AI creating its own persistent memory system.

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

**2. Add the AI system prompt (optional but recommended)**
Copy `.ai/AI_SYSTEM_PROMPT.md` and paste it into your AI assistant. This tells the AI to maintain the docs as it works.

**3. Start building**
Give your AI tasks. It will automatically update the four docs as it builds.

**4. Review**
Check what the AI built AND what it documented. Both should be accurate.

That's it. The AI maintains its own memory. You guide and review.

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
