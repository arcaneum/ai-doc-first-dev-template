# How to Use This Template

Here's how to get started and give your AI assistant persistent memory.

## Step 1: Create Your Repository

Click "Use this template" at the top of this GitHub page, or clone it locally:
```bash
git clone https://github.com/arcaneum/ai-doc-first-dev-template.git your-project-name
cd your-project-name
rm -rf .git
git init
```

## Step 2: Choose Your Setup Method

You have two options depending on which AI assistant you use:

### Option A: Claude Code Skill (Recommended for Claude Code)

**What is this?**
A Claude Code skill that automatically enables the framework behaviour. No manual prompts needed.

**Installation:**

1. **Create the skill directory:**
```bash
mkdir -p ~/.claude/skills/ai-doc-first-framework
```

2. **Copy the skill file:**
```bash
cp .ai/SKILL.md ~/.claude/skills/ai-doc-first-framework/SKILL.md
```

3. **Restart Claude Code** (if already running)

**That's it!** The skill will automatically:
- Detect when you're in a repo with this framework
- Read `PROGRESS.md` and `DECISIONS.md` at session start
- Maintain docs as it works
- Reference past decisions before suggesting changes

**How to verify it's working:**
Start Claude Code in your project and ask: "What's the current project state?"
The AI should read the docs and summarise what it found.

### Option B: Initialisation Prompt (For any AI assistant)

**What is this?**
A reference document you mention to your AI assistant at the start of each session to provide full context.

**Works with:** Cursor, GitHub Copilot, Gemini, any AI coding assistant

**Setup:**

1. **Clone the template** into your project

2. **At the start of each session**, reference `.ai/INITIALIZATION_PROMPT.md` using your AI's file mention feature

**Example for Cursor:**
- Open Cursor
- Open a new chat
- Type: `@INITIALIZATION_PROMPT.md` (or use the file picker to select it)
- Start working

**Example for Copilot Chat:**
- Open VS Code
- Open GitHub Copilot Chat
- Type: `@INITIALIZATION_PROMPT.md` (or use `#file` to reference it)
- Start working

**Example for Claude (via claude.ai):**
- Upload the project
- At session start, type: `@INITIALIZATION_PROMPT.md`
- Start working

**How to verify it's working:**
Ask your AI: "What's the current project state?"
It should read the docs and summarise what it found.

## Step 3: Initialise Your Project

**Start with PRD.md**

Open `docs/PRD.md` and answer (or ask your AI to help you answer):
- What are you building?
- Why does it exist?
- What problems does it solve?
- Who is it for?

This gives your AI the high-level context for every session.

**Your AI can help with this:**
```
You: "Help me fill in the PRD for a SaaS project management tool"
AI: [Asks clarifying questions and fills in PRD.md]
```

## Step 4: Start Building

**IMPORTANT:** The AI maintains these documents, not you.

As it builds features and makes decisions, it automatically updates:
- `PROGRESS.md` - What it just built
- `DECISIONS.md` - Choices it made and why
- `ARCHITECTURE.md` - If structure changed

**Your workflow:**

1. **Give the AI a task:**
   "Build a user registration form with email validation"

2. **AI builds and documents:**
   - Writes the code
   - Updates `PROGRESS.md`: "Implemented registration in components/RegisterForm.tsx"
   - Updates `DECISIONS.md`: "D-012 — Chose Zod for validation"

3. **You review:**
   - Check the code
   - Check the documentation
   - Approve or request changes

4. **Next session:**
   - AI reads the docs first
   - Knows what's built
   - Knows what was decided
   - Builds on previous work

## The Four Core Documents

**📋 PRD.md - What You're Building**
- Project purpose and goals
- Problem you're solving
- What's in scope (and what's not)

Update this when project scope or goals change.

**📝 DECISIONS.md - What You've Decided**
- Architectural choices
- Technology selections
- Approach decisions

Add an entry whenever you make a meaningful choice. Your AI reads this before making suggestions.

**🏗️ ARCHITECTURE.md - How It's Structured**
- System components
- How pieces connect
- Key patterns and conventions

Update this when you add major components or change structure.

**✅ PROGRESS.md - What You've Built**
- Completed features
- Current work in progress
- What's next

Update this after meaningful sessions. It gives your AI session-to-session continuity.

## Who Does What? (This Is Important)

**What the AI does:**
- Builds features when you give it tasks
- Documents what it built in PROGRESS.md
- Logs decisions it made in DECISIONS.md
- Updates ARCHITECTURE.md when structure changes
- Reads these docs at the start of each session
- References past decisions when making suggestions

**What you do:**
- Give the AI tasks and direction
- Review what the AI built AND what it documented
- Approve or request changes to both code and docs
- Guide the overall project direction
- Make final decisions on architecture and approach

**The workflow:**
1. You: "Build a user dashboard with activity feed"
2. AI: *builds the feature*
3. AI: *updates PROGRESS.md*: "Implemented user dashboard in `pages/Dashboard.tsx`"
4. AI: *updates DECISIONS.md*: "D-015 — Used React Query for activity feed data fetching"
5. You: *review code and documentation, approve if good*
6. Next session: AI reads those docs, knows dashboard exists, knows you're using React Query

This is the AI creating its own persistent memory. You're not doing the documentation work - you're reviewing it.

## Making It Work For You

**Do I need to document every tiny change?**
No. The AI doesn't document typo fixes, small tweaks, or trivial updates. Only meaningful work.

**What counts as "meaningful"?**
- Implemented a feature
- Made an architectural decision
- Chose one approach over another
- Built something your AI should remember

**How detailed should entries be?**
Brief but clear. A few sentences explaining what and why. You're not writing a novel.

**Can I change the format?**
Absolutely. This is a framework, not a mandate. Adapt it to your workflow. Rename files. Adjust the structure. Make it yours.

The core principle is what matters: **documentation as persistent memory for your AI**.

## Optional: AI System Prompt

Want your AI to actively maintain these docs? Reference `.ai/AI_SYSTEM_PROMPT.md` using your AI assistant's file mention feature (e.g., `@AI_SYSTEM_PROMPT.md`) at the start of a session.

This works especially well with Claude Code and Cursor, but any AI assistant that accepts custom instructions can use it.

## Optional: Task Template

Working on something specific? Use `.ai/AI_TASK_TEMPLATE.md` to create scoped work descriptions. This prevents your AI from wandering into unrelated changes.

## Optional: Pull Request Checklist

If you're working with a team, the `.github/pull_request_template.md` ensures documentation gets updated before merging.

## Tools That Play Well With This

This template works alongside (not instead of):
- **Notion** - for visual project planning
- **Linear** - for issue tracking
- **GitHub Projects** - for kanban boards

Keep these downstream of your repository. The repo is always the source of truth.

## Common Questions

**Does this work without AI?**
Yes. This is just good documentation practice. It helps human developers too.

**Which AI assistants does this work with?**
All of them. Claude Code, Cursor, GitHub Copilot, Gemini, or any LLM-based tool. It's just markdown files.

**What if my team thinks this is too much overhead?**
Start small. Just DECISIONS.md and PROGRESS.md. Add the others if they prove useful. The framework scales to your needs.

**Do I have to use all four documents?**
No. Use what helps. If you only need DECISIONS.md to stop your AI from contradicting itself, that's fine.

**Can I add more documents?**
Sure. Some projects add TESTING.md, DEPLOYMENT.md, or TROUBLESHOOTING.md. Add what makes sense.

## Getting Help

- Review the example entries in `docs/PROGRESS.md` and `docs/DECISIONS.md`
- Read `AI_CONTRIBUTING.md` for the complete framework
- Check the task template in `.ai/AI_TASK_TEMPLATE.md`

## What's Different Here

Most AI development frameworks focus on task management. This one focuses on **context engineering** - giving your AI the persistent memory it needs to be genuinely useful across sessions.

The immediate benefit isn't cleaner code or better architecture (though those are nice bonuses).

It's **better AI sessions starting today**. Less time re-explaining. More time building.

Your AI assistant becomes a collaborative partner instead of a goldfish.

---

Questions? Issues? Improvements? Open an issue or PR. This template gets better when people share what works (and what doesn't).
