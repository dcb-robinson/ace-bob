---
name: ace-connector-flows
description: Use when the user wants to create or modify IBM App Connect Enterprise connector-based message flows with the correct node attributes, policy artifacts, and schema files.
---

# ACE Connector Flow Skill

## Purpose
Use this skill when the user asks to create or modify ACE message flows that include connector-specific nodes.

## When not to use this skill
- If the request does not involve connector-specific nodes, use [`skills/ace-message-flow/SKILL.md`](../ace-message-flow/SKILL.md).
- If the request is primarily about project scaffolding, use [`skills/ace-project-setup/SKILL.md`](../ace-project-setup/SKILL.md).

## Required reading order
1. [`skills/shared/ace-versions.md`](../shared/ace-versions.md)
2. [`skills/shared/message-flow-rules.md`](../shared/message-flow-rules.md)
3. [`skills/shared/node-types.md`](../shared/node-types.md)
4. [`skills/shared/policy-projects.md`](../shared/policy-projects.md)
5. [`skills/shared/connector-index.md`](../shared/connector-index.md)
6. The relevant file under [`skills/shared/connectors/`](../shared/connectors)
7. [`skills/shared/review-checklist.md`](../shared/review-checklist.md)

## Critical rules
- Do not invent connector node types or attributes.
- Apply the connector-specific allowed operations exactly as documented.
- Create required policy and schema artifacts when the connector guidance requires them.
- If version-specific validation matters and the ACE version is not known, ask the user.

## Output requirements
- Create or update the requested connector-based flow artifacts.
- Create any required supporting policy and schema artifacts.
- Provide a concise summary of what was created or changed and which connector guidance was applied.
