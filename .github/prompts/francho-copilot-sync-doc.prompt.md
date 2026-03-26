---
name: francho-copilot-sync-doc
description: "Update README and related metadata after changing Copilot customizations in this repository, keeping descriptions and layout documentation synchronized."
argument-hint: "What changed that should be reflected in the documentation?"
agent: agent
---

Use this prompt after adding, deleting, renaming, or materially changing customizations in this repository.

## Required behavior

1. Identify which repository documents and metadata should change, starting with `README.md` and any related instruction files.
2. Update descriptions, lists of available customizations, setup notes, and repository layout details so they match the current repository contents.
3. Distinguish clearly between internal repo prompts in `.github/prompts/` and personal prompts in `prompts/`.
4. Remove stale references and mention newly added prompts, agents, skills, or instructions when relevant.
5. Keep the documentation concise and factual.
6. If there is nothing to update, say so explicitly instead of rewriting files unnecessarily.

## Validation

- Verify that file names and paths mentioned in documentation exist.
- Verify that capability claims still match the actual files.
- Flag any remaining inconsistencies that are adjacent but out of scope.