# Security Rules — e44cg Personal Projects

## Data classification

| Tier | Description | Rules |
|------|-------------|-------|
| **Public** | Open-source code, learning exercises, published samples | No restrictions |
| **Internal** | Draft tools, experiments, unpublished work | Work freely; don't transmit to external services without approval |
| **Sensitive** | API keys, tokens, credentials, personal data | Never hardcode. Use environment variables. Add to deny rules. |

## Core security rules

1. **No credentials in code.** Ever. Use environment variables or config files excluded by `.gitignore` and `.claudeignore`.
2. **Blast radius principle.** Before any action, ask: "If this goes wrong, is the worst case limited to inconvenience or is it reversible?" If no, flag to Emilio.
3. **Dependency installs require approval.** Explain what the package does, why it's needed, and whether it has known security issues.
4. **No network requests to external APIs without explicit approval.** Explain what data will be sent and where.
5. **No system-level changes.** Do not modify PATH, environment variables, registry, or global configurations without explicit approval and plain-language explanation.

## Git safety

- Never force push.
- Never amend published commits.
- Commit messages in plain language describing what changed and why.
- Review `git diff` before committing — summarize changes to Emilio in plain language.

## Cross-project isolation

- This workspace cannot edit any Pacific-Outcomes file (hard deny in settings.json).
- This workspace cannot read PO's sensitive paths: banking, taxes, recovery codes, NDA, client originals, confidential folders, `_locked` folders (hard deny).
- General PO files (strategy, outreach) are readable only when Emilio explicitly initiates cross-pollination.
- If a tool or project needs data from Pacific-Outcomes, that is a red flag — stop and discuss with Emilio.

## The `_locked` convention

Any folder named `_locked` is globally denied — no Claude Code session can read or edit its contents. This applies here too:
- Create `_locked` subfolders for personal sensitive data (credentials, private materials).
- The global `settings.json` enforces this. Cannot be overridden.
