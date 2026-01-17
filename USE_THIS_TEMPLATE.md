# How to Use This Template

## Getting Started

1. **Create a new repository using this template**
   - Click "Use this template" on GitHub, or
   - Clone locally: `git clone <this-repo> your-project-name`

2. **Fill in `/docs/PRD.md`**
   - Describe your project's purpose and goals
   - Define what's in scope and out of scope

3. **Create your first task**
   - Copy `.ai/AI_TASK_TEMPLATE.md`
   - Fill in the task details
   - This becomes your contract with the AI

4. **Use your preferred AI coding tool**
   - Copy the system prompt from `.ai/AI_SYSTEM_PROMPT.md`
   - Paste it into Claude Code, Gemini, or your preferred AI assistant
   - The AI will follow the documentation requirements

5. **Review before merging**
   - Check that code changes are documented
   - Verify that decisions are recorded
   - Use the PR template checklist

## Adapting This Framework

You are encouraged to adapt this framework to your needs:
- Rename files to match your conventions
- Adjust the documentation requirements
- Modify the AI system prompt
- Customize the enforcement rules

The core principle remains: **AI assists execution, documentation preserves intent.**

## Optional Integrations

This template works well with:
- **Notion** - for visual task tracking (status only, not source of truth)
- **Linear** - for issue tracking
- **GitHub Projects** - for kanban boards

Keep these tools downstream of the repository. The repo is always the canonical source.

## Getting Help

- Read [AI_CONTRIBUTING.md](AI_CONTRIBUTING.md) for the full contract
- Review the example entries in `/docs/PROGRESS.md` and `/docs/DECISIONS.md`
- Check the task template in `.ai/AI_TASK_TEMPLATE.md`

## Common Questions

**Q: Do I need to update documentation for every single change?**
A: No. Only for meaningful changes. Typo fixes and trivial updates don't require documentation entries.

**Q: Can I use this without AI?**
A: Yes! This framework also works well for human-only development. It simply enforces good documentation discipline.

**Q: What if I disagree with some of the rules?**
A: Adapt them. This is a framework, not a mandate. Take what works for you.
