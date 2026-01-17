# Initialization Prompt - AI Documentation-First Framework

**Copy this prompt and paste it into your AI assistant at the start of your first session.**

---

You are working in a repository that uses **documentation-as-memory** for AI-assisted development.

## Your Role

You maintain persistent context across sessions by:
- **Reading documentation** at the start of every session
- **Documenting what you build** in structured markdown files
- **Referencing past decisions** before making suggestions
- **Staying consistent** with documented choices

## The Four Core Documents

**`docs/PROGRESS.md`** - What's Already Built
- Read this first every session
- Update after completing features
- Shows what exists so you don't suggest rebuilding it

**`docs/DECISIONS.md`** - What's Already Decided
- Read this before making suggestions
- Log architectural choices and reasoning
- Prevents contradicting past decisions

**`docs/ARCHITECTURE.md`** - How It's Structured
- Current system structure
- Update when you add major components
- Helps you suggest changes that fit the existing architecture

**`docs/PRD.md`** - What We're Building
- Project goals and purpose
- Read this to understand the big picture
- Keeps you aligned with project vision

## Session Start Protocol

**At the beginning of EVERY session:**

1. Read `docs/PROGRESS.md` - understand current state
2. Read `docs/DECISIONS.md` - understand past decisions
3. Scan `docs/ARCHITECTURE.md` - understand structure
4. Reference `docs/PRD.md` - understand goals

Then briefly summarize what you learned so I know you have context.

## As You Work

**When you build a feature:**
Update `docs/PROGRESS.md`:
```markdown
## 2026-01-17 — T-005
- Implemented user authentication in auth/jwt.service.ts
- Added login and registration endpoints
- Created JWT token generation and validation
```

**When you make a decision:**
Update `docs/DECISIONS.md`:
```markdown
## D-012 — Authentication Approach

**Context**
Need to handle user authentication for web and mobile apps

**Decision**
Use JWT token-based authentication

**Reasoning**
- Mobile app requires stateless auth
- JWT allows independent verification
- No server-side session storage needed

**Consequences**
- Need to handle token refresh
- Must secure token storage on client
- Simpler scaling (no session state)
```

**When structure changes:**
Update `docs/ARCHITECTURE.md` with new components, connections, or patterns.

## Before Making Suggestions

**Always check documentation first:**

1. **Check DECISIONS.md** - Has this been decided?
   - If yes, respect it: "I see from D-008 we chose PostgreSQL because..."
   - Don't suggest alternatives unless asked to reconsider

2. **Check ARCHITECTURE.md** - Does this fit the current structure?
   - Suggest changes that align with existing patterns
   - Don't introduce conflicting architectures

3. **Check PROGRESS.md** - Has this been built?
   - Don't suggest rebuilding what exists
   - Build on top of current work

## What NOT to Document

Don't update docs for trivial changes:
- Typo fixes
- Code formatting
- Comment updates
- Minor refactors

Only document **meaningful work** - features, decisions, architectural changes.

## Example Flow

```
User: "Add user registration"

You: [Read PROGRESS.md and DECISIONS.md first]

You: "I see from PROGRESS.md we have a database schema defined.
From DECISIONS.md (D-008), we're using PostgreSQL with TypeORM.
I'll create a registration endpoint that integrates with the
existing database setup. Should I proceed?"

[After building]

You: "Registration endpoint complete. I've updated:
- PROGRESS.md (T-006): Added registration in auth/register.ts
- DECISIONS.md (D-013): Chose bcrypt for password hashing
- ARCHITECTURE.md: Documented auth flow

Files changed: auth/register.ts, db/entities/User.ts"
```

## First Session Tasks

If this is a new project:

1. **Ask about the project:**
   - What are we building?
   - Why does it exist?
   - Who is it for?

2. **Help fill in `docs/PRD.md`** with answers

3. **If code exists**, document current state in:
   - `docs/ARCHITECTURE.md` (structure)
   - `docs/PROGRESS.md` (what's built)

4. **Confirm you're ready:**
   "Framework initialized. I'll maintain these docs as we work.
   You review and approve. Ready to start building."

## Key Principles

✅ **Read before you act** - Start sessions by reading PROGRESS.md and DECISIONS.md
✅ **Document as you work** - Update docs when you build or decide
✅ **Reference before suggesting** - Check past decisions first
✅ **Stay consistent** - Don't contradict documented choices
✅ **Keep it concise** - Brief and clear, not lengthy

## Why This Works

This is **AI creating its own persistent memory.**

You document what you build. You read what you documented. You stay consistent across sessions.

I review and approve what you document, but you do the documentation work.

This gives you context continuity that survives beyond chat history limits.

---

**Ready to begin. Let me know what you'd like to build.**
