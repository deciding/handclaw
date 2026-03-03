---
name: project_workflow
description: "Create or update project workflow documentation in AGENTS.md (for opencode/codex) or CLAUDE.md (for claude). Use when: user asks to create/update a workflow, document build/test/debug steps, or update project documentation. The skill will check memory and repo to extract relevant commands, then write sections to the appropriate file. NOT for: one-off commands, reading existing docs only, or when the workflow sections are already complete."
metadata: { "openclaw": { "emoji": "📋", "requires": {} } }
---

# Project Workflow Skill

Create or update project workflow documentation in the repo's AGENTS.md (for opencode/codex) or CLAUDE.md (for claude).

## When to Use

✅ **USE this skill when:**

- User asks to "create a workflow" or "document the workflow"
- User asks to add "build", "test", "debug" steps to AGENTS.md/CLAUDE.md
- User asks to document how to build, test, or debug the project
- Setting up a new project and need to document development workflow
- User asks to add "command cheatsheet", "workflow process", or "mistake list"

## When NOT to Use

❌ **DON'T use this skill when:**

- User only wants to run a single build/test command
- User is asking about a specific error or bug (use debugging tools)
- AGENTS.md/CLAUDE.md already has complete workflow sections and user just wants to read them
- User wants to commit/push workflow docs (that's a git operation)

## Process

### Step 1: Detect Agent Type

Determine which agent is being used:
- **opencode** or **codex** → use `AGENTS.md`
- **claude** → use `CLAUDE.md`

### Step 2: Check Memory

Look for relevant context in the agent's memory:

- Check for any remembered build commands, test commands, or debug tips
- Look for package manager info (pnpm, npm, bun, yarn)
- Check for any stored configuration or environment setup notes
- Check for previous mistakes and solutions

### Step 3: Check the Repo

Examine the repository to find workflow-relevant information:

- **package.json**: Look for scripts (build, test, dev, lint, typecheck)
- **README.md**: Check for build/test instructions
- **AGENTS.md** or **CLAUDE.md**: Check if workflow sections already exist
- **Makefile** or **justfile**: Check for build recipes
- **Dockerfile**: Check for build steps if applicable

### Step 4: Create ~/.handclaw Directory (if needed)

For long or reusable content, create a `.handclaw` directory in the user's home directory:

- `~/.handclaw/WORKFLOW.md` - Full workflow process documentation
- `~/.handclaw/TIPS.md` - Debug tips and common mistakes
- `~/.handclaw/COMMANDS.md` - Extended command reference

### Step 5: Write Sections to AGENTS.md/CLAUDE.md

Create or update the following sections at the END of the appropriate file:

#### 1. Command Cheatsheet

```markdown
## Command Cheatsheet

- Install deps: `<package-manager> install`
- Build: `<package-manager> build` if failed check solutions in @~/.handclaw/COMMANDS.md
- Dev: `<package-manager> dev`
- Test: `<package-manager> test`
- Lint: `<package-manager> lint`
- Typecheck: `<package-manager> typecheck`
```

If content is short, keep inline. If long, reference external file.

#### 2. Workflow

```markdown
## Workflow

1. **Plan**: Understand the task, analyze requirements, check existing code
2. **Todo**: Create a todo list with `TodoWrite` for multi-step tasks
3. **Change Code**: Implement changes step by step
4. **Review**: Review changes, run lint/typecheck
5. **Build/Test**: If successful → build → test → deploy
   - If problems → go back to step 2 or 3
6. **Commit** (only when explicitly asked)

For detailed workflow see @~/.handclaw/WORKFLOW.md
```

#### 3. Mistake List

```markdown
## Mistake List

- **[Error/Issue]**: [Solution/Tip]
- **Module Z failed**: add a debug=True parameter in the function xyz calling
- **Module X reports error Y**: Check Z as described in @~/.handclaw/TIPS.md

```

### Section Update Logic

- If a section already exists, update it with current information
- If a section doesn't exist, create it
- Preserve existing content that isn't part of these sections
- Create the file (AGENTS.md or CLAUDE.md) if it doesn't exist
- Place all new sections at the END of the file

## Output Format

Write sections like:

```markdown
---

## Command Cheatsheet

- Install deps: `pnpm install`
- Build: `pnpm build`
- Dev: `pnpm dev`
- Test: `pnpm test`
- Lint: `pnpm lint`
- Typecheck: `pnpm typecheck`

## Workflow

1. **Plan**: Understand the task, analyze requirements, check existing code
2. **Todo**: Create a todo list with `TodoWrite` for multi-step tasks
3. **Change Code**: Implement changes step by step
4. **Review**: Review changes, run lint/typecheck
5. **Build/Test**: If successful → build → test → deploy
   - If problems → go back to step 2 or 3
6. **Commit** (only when explicitly asked)

## Mistake List

- **pnpm install fails**: Try deleting node_modules and pnpm-lock.yaml first
- **TypeScript errors**: Run `pnpm typecheck` to see all errors
- **Build fails**: Check if all dependencies are installed
```

For longer content, use references:

```markdown
## Command Cheatsheet

If case1 encountered, See @~/.handclaw/COMMANDS.md for the `solutionToCase1` command.
```

## Notes

- Always use the actual commands found in the memory/repo, don't guess
- Prioritize memory over repo
- Add project-specific debug tips if discovered
- Keep sections concise but actionable
- Use references (@~/.handclaw/...) for long or reusable content
- The keyword format `@~/.handclaw/FILE.md` allows quick lookup
