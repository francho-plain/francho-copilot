---
name: francho-copilot-review
description: "Review this repository's Copilot customizations for inconsistencies, quality issues, broken references, invalid frontmatter, and documentation drift."
argument-hint: "What area, file, or customization set should be reviewed?"
agent: agent
---

Review this repository as a collection of reusable GitHub Copilot customizations.

## Review focus

Check the requested files, and also inspect directly related files when necessary, for:

- Contradictory guidance across agents, instructions, prompts, skills, and README.
- Invalid or weak frontmatter: missing fields, vague descriptions, placeholder text, wrong names, or wrong locations.
- Broken references to files, paths, tools, capabilities, workflows, or repository structure.
- Duplicated or near-duplicated customizations that should likely be merged.
- Capability mismatches, especially when an agent's declared tools do not match its stated purpose.
- Documentation drift between customization files and `README.md`.
- Wrong placement between internal repo prompts in `.github/prompts/` and personal prompts in `prompts/`.

## Output format

1. Findings first, ordered by severity.
2. For each finding, include file references and explain why it matters.
3. State explicitly when no findings are present.
4. End with a short list of the highest-value fixes or follow-up actions.

Do not pad the review with generic advice. Keep it specific to this repository.