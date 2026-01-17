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

**2. Choose your setup method**

**Option A: Claude Code Skill (Recommended for Claude Code users)**

Install the `ai-doc-first-framework` skill:

1. Copy the `SKILL.md` file from this repo's `.ai/` folder
2. Place it in `~/.claude/skills/ai-doc-first-framework/SKILL.md`
3. Start Claude Code in your project

The skill automatically:
- Detects the framework structure
- Reads docs at session start
- Maintains docs as it works
- No manual prompts needed

**Option B: Initialization Prompt (For any AI assistant)**

For Cursor, Copilot, Gemini, or other AI assistants:

1. Copy `.ai/INITIALIZATION_PROMPT.md`
2. Paste it into your AI assistant at session start
3. The AI will maintain docs as it works

**3. Start building**
Give your AI tasks. It will automatically maintain the four docs.

**4. Review**
Check what the AI built AND what it documented.

That's it. The AI creates its own persistent memory.

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
