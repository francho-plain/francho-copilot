# Francho's Copilot Configs

Personal GitHub Copilot agents, skills, and instructions, stored in one repo and linked into `~/.copilot/`.


## Current Configurations

### Agents

- `code-cop.agent.md`: read-only security review agent for dependency, license, code, and configuration risk analysis.
- `python-databricks-coach.agent.md`: Python coaching and code review agent focused on Python quality, Databricks Apps, and professional engineering practices.

### Skills

- `skills/english-teacher/`: adds brief English corrections when the user writes in English.

### Instructions

- `instructions/tone.instructions.md`: answer in the user's language, keep documentation and code in English by default, and stay concise unless asked otherwise.

## Setup

Run this from the repository root:

```bash
mkdir -p ~/.copilot
ln -sfn "$PWD/agents" "$HOME/.copilot/agents"
ln -sfn "$PWD/instructions" "$HOME/.copilot/instructions"
ln -sfn "$PWD/skills" "$HOME/.copilot/skills"
```

To verify the links are correct, run:

```bash
ls -l ~/.copilot
```

If the links are correct, changes in this repo are immediately reflected in Copilot.

This repo then becomes the source of truth for your personal Copilot configuration.

