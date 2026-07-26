# agent-guidance

Portable guidance for AI tools that support `AGENTS.md`-style workspace context,
system prompts, user profiles, or custom instruction files.

## Repository layout

- `global-instructions.md` — master instructions intended for web-based AI models.
- `user-profile/background.md` — role, projects, environment, and goals.
- `user-profile/preferences.md` — tone, style, formatting, and anti-patterns.
- `templates/AGENTS.md` — a universal project-root instruction template.
- `templates/custom-instructions.json` — a machine-readable context variant.

## Sync and deployment model

1. Keep durable, platform-neutral guidance in this repository.
2. Copy or adapt `global-instructions.md` into a model's system or custom-instructions field.
3. Copy the two `user-profile` files into tools that support separate profile/context fields.
4. Copy `templates/AGENTS.md` into a project root and customize the project-specific sections.
5. Translate the JSON template into platform-specific fields when a tool accepts structured context.
6. Review changes before syncing them to external tools; never commit secrets, access tokens, or private credentials.

## Maintenance

Use this repository as the source of truth. When a platform has different limits or instruction
semantics, make a small documented adaptation rather than changing the canonical files silently.
