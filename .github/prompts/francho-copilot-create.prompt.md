---
name: francho-copilot-create
description: "Create or extend a Copilot customization in this repository while following official GitHub Copilot conventions and avoiding duplicates."
argument-hint: "What customization do you want to add or update?"
agent: agent
---

Related skill: `agent-customization`. Load and follow it when the task involves creating or restructuring customization files.

Work inside this repository as the source of truth for personal Copilot customizations.

## Goal

Create or update the smallest valid customization that solves the request while keeping the repository coherent.

## Required behavior

1. Determine the correct primitive before editing: repository instructions, path-specific instructions, prompt, custom agent, or skill.
2. For internal maintenance workflows of this repository, store prompts under `.github/prompts/*.prompt.md`.
3. Reserve `prompts/*.prompt.md` for personal prompts that are meant to be linked into `~/.copilot/prompts`.
4. Search for existing files that already cover the requested behavior and prefer updating them over adding near-duplicates.
5. Inspect adjacent files that define the same behavior so names, descriptions, examples, and claims stay aligned.
6. Search for inconsistencies, stale wording, broken references, misplaced files, and missing README updates as part of the task.
7. Keep frontmatter valid YAML and descriptions specific enough for discovery.
8. If the request is ambiguous, clarify scope, target files, and whether the rule should be internal to this repo or part of the personal `~/.copilot/` setup.

## Output expectations

- Implement the change when the intent is clear.
- Summarize what was added or updated.
- Call out any adjacent inconsistencies you fixed.
- If something related is still ambiguous, state the gap explicitly and propose the next precise customization to add.