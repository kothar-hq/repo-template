# kothar-hq template

GitHub repository template for kothar-hq projects.

## What this template includes

- Markdown linting via [markdownlint-cli](https://github.com/igorshubovych/markdownlint-cli)
  with CI enforcement
- Claude Code agents for reviewing and fixing Markdown

## Getting started

1. Click **Use this template** on GitHub to create a new repository.
2. Replace this file with your project's README.
3. Adjust `.markdownlintignore` to skip any generated directories.

## Markdown lint

All `.md` files are linted on every push and pull request to `main`.
Rules live in `.markdownlint.json`; `MD013` (line length) is the only
disabled rule.

Run the linter locally:

```sh
npx -y markdownlint-cli --dot '**/*.md'
```

Auto-fix what can be fixed automatically:

```sh
npx -y markdownlint-cli --dot --fix '**/*.md'
```

## Claude Code agents

`.claude/agents/` contains subagent definitions used with Claude Code:

| Agent | Purpose |
| --- | --- |
| `markdown-reviewer` | Reviews `.md` files for lint errors and accuracy |
| `markdown-fixer` | Applies lint fixes without disabling rules |
