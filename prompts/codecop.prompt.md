---
name: codecop
description: "Use the Code Cop agent to analyze the current repository for security, dependency, license, configuration, and install-script risks."
argument-hint: "Optional focus area within the current repository"
agent: "Code Cop"
---

Analyze the current repository with the `Code Cop` agent.

## Scope

- Default to the entire current repository.
- If the user provided an argument, treat it as a focus area, file, or subdirectory inside the current repository.
- Do not analyze unrelated external paths unless the user explicitly requests them.

## Required behavior

1. Use only the `Code Cop` agent for the analysis.
2. Treat the task as read-only security and compliance review.
3. Cover project overview, dependencies, license risk, code security, configuration and infrastructure, and install/build scripts when applicable.
4. If the repository is small, analyze it fully. If it is large, prioritize likely risk surfaces first.
5. Report concrete findings with severity, affected files, and rationale.
6. End with a clear overall verdict and recommended next actions.

## Output format

- Security verdict
- Findings ordered by severity
- License summary
- Recommended fixes or follow-up checks