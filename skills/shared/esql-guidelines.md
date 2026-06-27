# ACE ESQL Guidelines

## Purpose
This document defines ACE-focused guidance for creating and refining ESQL used by Compute nodes.

## When to use
Use this document when generating or reviewing `.esql` files for ACE Compute nodes.

## Performance and tree navigation
- Declare `REFERENCE` variables when navigating heavily nested logical trees to reduce repeated navigation cost.
- Avoid unnecessary full tree copying when a change is limited to a small part of the message tree.
- Avoid multiple consecutive Compute nodes where a simpler design would achieve the same result.
- Avoid using `CARDINALITY` inside loops when the value can be determined once outside the loop.
- Minimize expensive string manipulation where a simpler approach is available.
- Minimize the number of statements when doing so improves clarity and efficiency.

## Field existence checks
- Use `LASTMOVE` or `CARDINALITY` when checking whether a field exists.
- Prefer the most direct existence check that matches the tree navigation pattern being used.

## Tree construction
- Consider `CREATE ... PARSE` when it is more efficient than serializing and reparsing a copied logical tree.
- Be deliberate about Compute node copy behavior and avoid unnecessary message assembly duplication.

## Flow design considerations
- Prefer clean flow design over wiring every failure terminal individually when a consistent catch strategy is more suitable.
- Consider whether a subflow or shared library is more appropriate when logic is repeated.

## Validity guardrails
- Do not invent ESQL built-in functions.
- If a requested function or syntax is uncertain, use known ACE ESQL constructs rather than guessing.

## Related files
- [`skills/ace-esql/SKILL.md`](../ace-esql/SKILL.md)
- [`skills/shared/review-checklist.md`](review-checklist.md)
