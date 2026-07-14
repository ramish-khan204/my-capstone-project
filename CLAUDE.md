# Claude / AI Assistant Guidelines

This document provides context for AI coding assistants working in this repository.

## Tech Stack

| Layer | Technology | Purpose |
|-------|------------|---------|
| Markup | HTML | Semantic page structure and accessibility |
| Styling | CSS | Layout, theming, and responsive design |
| Logic | TypeScript | Application behavior with static type checking |
| Version Control | Git | Local commits, branches, and history |
| Hosting | GitHub | Remote repository, pull requests, and collaboration |

When adding new code, prefer vanilla or lightly configured tooling that fits this stack. Avoid introducing heavy frameworks unless the project requirements change.

## Coding Conventions

### HTML

- Use semantic elements (`<header>`, `<main>`, `<nav>`, `<section>`, `<article>`, `<footer>`) instead of generic `<div>` wrappers where appropriate.
- Include meaningful `alt` text on images and `aria-*` attributes when needed for accessibility.
- Keep markup shallow and readable; avoid unnecessary nesting.

### CSS

- Use consistent naming (BEM or a similar convention) for classes.
- Group related rules together; prefer one file per major component or page section.
- Write mobile-first media queries when implementing responsive layouts.
- Avoid inline styles except for truly dynamic values set by JavaScript.

### TypeScript

- Enable strict mode and resolve all type errors before committing.
- Prefer `interface` for object shapes and `type` for unions or aliases.
- Use descriptive names for functions, variables, and files (`kebab-case` for files, `camelCase` for variables/functions, `PascalCase` for classes/types).
- Keep functions small and single-purpose; extract reusable logic into modules under a `src/` directory.

### General

- Match the existing style of surrounding code before introducing new patterns.
- Do not commit secrets, API keys, or `.env` files.
- Keep changes focused; avoid unrelated refactors in the same commit.

## Git Conventional Commits

Follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

```
<type>(<optional scope>): <short description>

[optional body]

[optional footer]
```

### Common Types

| Type | When to use |
|------|-------------|
| `feat` | A new feature |
| `fix` | A bug fix |
| `docs` | Documentation only |
| `style` | Formatting, no logic change |
| `refactor` | Code change that neither fixes a bug nor adds a feature |
| `test` | Adding or updating tests |
| `chore` | Build process, tooling, or dependency updates |

### Examples

```
feat(nav): add responsive mobile menu
fix(form): prevent submit when email is invalid
docs: update README installation steps
chore: add .gitignore entries for dist and .env
```

- Use the imperative mood in the subject line ("add" not "added").
- Keep the subject line under 72 characters.
- Reference issue numbers in the footer when applicable (`Closes #12`).

## AI Usage Guidelines

### Do

- Read existing files and follow established patterns before writing new code.
- Make the smallest change that correctly solves the requested task.
- Explain non-obvious decisions in code comments sparingly and only where needed.
- Run or suggest running linters and type checks after substantive edits.
- Ask for clarification when requirements are ambiguous rather than guessing.

### Do Not

- Commit changes unless explicitly asked by the user.
- Add large dependencies or frameworks without a clear reason.
- Over-engineer solutions (extra abstractions, premature optimization).
- Include secrets, credentials, or personal data in generated code or commits.
- Rewrite unrelated files when fixing a targeted issue.

### Workflow

1. Understand the task and inspect relevant source files.
2. Propose or implement a focused solution.
3. Verify the change (build, lint, manual check) when tooling is available.
4. Summarize what changed and why in plain language.
