---
name: ace-esql
description: Use when the user wants to create or refine IBM App Connect Enterprise ESQL for Compute nodes using ACE-focused best practices.
---

# ACE ESQL Skill

## Purpose
Use this skill when the user asks to create or modify `.esql` files for ACE Compute nodes.

## When not to use this skill
- If the main request is to create or modify `.msgflow` structure, use [`skills/ace-message-flow/SKILL.md`](../ace-message-flow/SKILL.md) or [`skills/ace-connector-flows/SKILL.md`](../ace-connector-flows/SKILL.md).
- If the main request is JavaCompute logic, use [`skills/ace-java-compute/SKILL.md`](../ace-java-compute/SKILL.md).

## Required reading order
1. [`skills/shared/esql-guidelines.md`](../shared/esql-guidelines.md)
2. [`skills/shared/review-checklist.md`](../shared/review-checklist.md)

## Critical rules
- Generate ACE-compatible ESQL.
- Prefer simple, efficient, and maintainable ESQL.
- Avoid inventing nonexistent ESQL functions.
- Keep the response focused on the requested ESQL change.

## Output requirements
- Create or update the requested ESQL artifacts.
- Provide a concise summary of what was created or changed.
