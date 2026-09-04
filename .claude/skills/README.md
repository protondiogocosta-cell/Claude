# Skills

This directory contains skills vendored from upstream skill repositories as
project skills, so they're automatically available in any Claude Code
session opened against this repository — including the mobile and web apps,
not just the local CLI. Each skill triggers by matching its own description,
so no extra setup is needed on any surface.

## Sources

- **[anthropics/skills](https://github.com/anthropics/skills)** — all skills
  from the `document-skills` and `example-skills` plugin bundles, plus
  `claude-api`, `academy-guide`, and `discernment-nudge`. Each skill folder
  carries its own `LICENSE.txt`. See the upstream
  [README](https://github.com/anthropics/skills#readme) and
  [THIRD_PARTY_NOTICES.md](https://github.com/anthropics/skills/blob/main/THIRD_PARTY_NOTICES.md)
  for full attribution.

- **[obra/superpowers](https://github.com/obra/superpowers)** — the 14 skills
  under `skills/` in that repo (`using-superpowers`, `brainstorming`,
  `test-driven-development`, `systematic-debugging`, `writing-plans`,
  `executing-plans`, `subagent-driven-development`,
  `dispatching-parallel-agents`, `receiving-code-review`,
  `requesting-code-review`, `writing-skills`, `using-git-worktrees`,
  `finishing-a-development-branch`, `verification-before-completion`).
  Licensed under MIT — see `LICENSE-superpowers.txt`.

  Note: upstream Superpowers is a full plugin that also ships a `SessionStart`
  hook (forces a skill-check reminder into every new conversation) and other
  plugin scaffolding. Only the skills themselves are vendored here — the hook
  was intentionally left out since hook execution isn't confirmed to behave
  identically across CLI, web, and mobile sessions. Each skill's own
  description still triggers it automatically without the hook.

## Updating

To update either source to its latest upstream version, re-copy its `skills/`
folder into this directory.
