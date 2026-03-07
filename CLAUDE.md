# e44cg — Personal Projects Workspace

**Version:** 1.0 | **Date:** March 7, 2026

Personal learning, experimentation, and tool-building space for Emilio Cantu-Gil. Not client-facing. Not connected to Pacific-Outcomes.

---

## Identity and scope

- This workspace is for personal skill development, code exploration, and building tools that may eventually support professional work.
- Stakes: low (learning) to medium (tools that could be used professionally).
- No client data, no NDA materials, no engagement details exist or belong here.
- GitHub account: `e44cg` (personal). Never push to `pacific-outcomes/` org from this workspace.

## Isolation — HARD RULE

This workspace has ZERO connection to Pacific-Outcomes.

- Never reference, import, copy, or depend on any Pacific-Outcomes files, client data, strategy, or deliverables.
- Never access `C:/Users/emili/OneDrive/Pacific-Outcomes/` from this workspace — not even to read.
- If Emilio asks to replicate something from Pacific-Outcomes, ask him to describe what he wants rather than looking at the source.
- Never mention client names, engagement details, or business strategy from Pacific-Outcomes sessions.

## Decision protocol

Same as global:
- Present 2-3 options with tradeoffs on strategic or structural questions.
- Provide a recommendation with reasoning. Wait for approval.
- Do not assume silence means approval.

## Non-coder rules

Inherited from global `~/.claude/CLAUDE.md` and reinforced here:
- Emilio cannot read or write code. Plain-language explanations are mandatory, not optional.
- Before installing dependencies, explain what each package does and why it's needed.
- Before creating files, explain the purpose and structure in plain language.
- After completing work, summarize: what changed, what files exist, what the current state is.
- Never run commands that modify system-level configuration without explicit approval and plain-language explanation.

## Project structure

```
e44cg/
├── CLAUDE.md              # This file
├── CLAUDE.local.md        # Session context (current focus, active experiments)
├── .claude/
│   ├── settings.json      # Project-level deny rules
│   └── rules/
│       └── security.md    # Security rules for personal projects
├── .claudeignore          # Search exclusions
├── .gitignore             # Git exclusions
├── projects/              # Individual project subdirectories
│   └── [project-name]/    # Each project gets its own folder
└── docs/
    └── project-log.md     # Running log of what was built, when, why
```

## New project checklist

Before starting any new project in this workspace:
1. Create a subfolder under `projects/` with a descriptive name.
2. Discuss scope and goals with Emilio before writing code.
3. Identify any external APIs or services needed — document and get approval.
4. Confirm: does this project handle any sensitive data? If yes, add project-specific deny rules.
5. Log the project in `docs/project-log.md`.
