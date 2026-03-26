# Repository Instructions

This repository stores personal GitHub Copilot customizations that are linked into `~/.copilot/`.
Treat it as the source of truth for reusable agent, skill, and instruction definitions.

## Repository Purpose

- Keep custom Copilot configurations high quality, reusable, and internally consistent.
- Prefer small, deliberate changes over broad rewrites.
- Preserve English for instruction, agent, skill, and README content unless a file explicitly exists to define language behavior.

## Repository Layout

- `agents/` contains reusable custom agents.
- `instructions/` contains reusable user-level instruction files.
- `.github/prompts/` contains internal repository prompts used to maintain this repo's customizations.
- `prompts/` contains reusable personal prompt files and mirrors the prompt layout under `~/.copilot/`.
- `skills/` contains reusable skills and their bundled guidance.
- `README.md` documents the current setup and usage.
- `.github/copilot-instructions.md` is the repository-wide Copilot instruction file.

## Editing Rules

- Before editing, inspect related files that define the same behavior so changes stay aligned across `README.md`, `agents/`, `instructions/`, `prompts/`, and `skills/`.
- When updating this repository, always search for inconsistencies, stale wording, duplicated guidance, broken references, misplaced files, and opportunities to improve clarity.
- Fix directly related inconsistencies in the same change when the scope is clear and safe. If an issue is adjacent but not clearly in scope, report it explicitly.
- Prefer updating an existing customization over adding a near-duplicate file.
- Keep frontmatter valid YAML. Quote descriptions when useful, avoid placeholder text, and do not leave commented template values in committed files.
- Follow official GitHub Copilot conventions for file locations and names, but adapt them to this repo's dual purpose: repository-wide instructions belong in `.github/copilot-instructions.md`, internal repo prompts belong under `.github/prompts/*.prompt.md`, path-specific instructions belong under `.github/instructions/*.instructions.md` when intentionally used, and reusable personal prompts for this setup belong under `prompts/*.prompt.md`.
- Internal maintenance prompts for this repository must stay in `.github/prompts/`.
- Personal prompts intended to be symlinked into `~/.copilot/prompts` must stay in `prompts/`.
- Use precise descriptions so Copilot can discover the right customization from the file metadata.

## Quality Expectations

- Keep guidance concrete, enforceable, and repository-specific rather than generic.
- Avoid contradictory instructions across agents, skills, prompts, and instructions.
- Align tool permissions with the stated purpose of each agent.
- Keep examples, file paths, and capability claims synchronized with the actual repository contents.
- When changing behavior, update documentation if the README or related customization files become outdated.

## Validation

- Validate changed Markdown for structure and readability.
- Re-read changed frontmatter blocks to confirm syntax, field names, and intent.
- Confirm that any new customization file is in the correct path for GitHub Copilot to load it.
- If a change affects setup or repository usage, verify that `README.md` still matches the real workflow.

Trust these instructions first for repository context and only search further when the instructions are incomplete or contradicted by the current files.