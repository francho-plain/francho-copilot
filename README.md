# Francho's Copilot Configs

Personal GitHub Copilot agents, skills, and instructions, stored in one repo and linked into `~/.copilot/`.

## License

This repository is licensed under Apache-2.0.

If you redistribute this project or derivative works, keep the `LICENSE` and `NOTICE` files.
For commercial and non-commercial use, preserve the attribution to the original source:
`https://github.com/francho-plain/francho-copilot`


## Current Configurations

### Agents

- `code-cop.agent.md`: read-only security review agent for dependency, license, code, and configuration risk analysis.
- `python-databricks-coach.agent.md`: Python coaching and code review agent focused on Python quality, Databricks Apps, and professional engineering practices.

### Skills

- `skills/english-teacher/`: adds brief English corrections when the user writes in English.

### Instructions

- `instructions/tone.instructions.md`: answer in the user's language, keep documentation and code in English by default, and stay concise unless asked otherwise.

### Prompts

- `prompts/codecop.prompt.md`: run the `Code Cop` agent against the current repository or an optional focus area.


## Setup

Run this from the repository root:

```bash
mkdir -p ~/.copilot
ln -sfn "$PWD/agents" "$HOME/.copilot/agents"
ln -sfn "$PWD/instructions" "$HOME/.copilot/instructions"
ln -sfn "$PWD/prompts" "$HOME/.copilot/prompts"
ln -sfn "$PWD/skills" "$HOME/.copilot/skills"
```

To verify the links are correct, run:

```bash
ls -l ~/.copilot
```

If the links are correct, changes in this repo are immediately reflected in Copilot.

This repo then becomes the source of truth for your personal Copilot configuration.

### Internal Repo copilot

This repository also contains a repository-specific Copilot configuration used only to generate, review, and maintain the contents of this repo itself.

Do not link this internal configuration into `~/.copilot/`. It is not part of the reusable personal setup and should remain scoped to this repository.

- `.github/prompts/francho-copilot-create.prompt.md`: create or extend customizations in this repository while keeping placement and conventions correct.
- `.github/prompts/francho-copilot-review.prompt.md`: review this repository for inconsistencies, weak frontmatter, broken references, and documentation drift.
- `.github/prompts/francho-copilot-sync-doc.prompt.md`: update README and related metadata after changing this repository's customizations.
