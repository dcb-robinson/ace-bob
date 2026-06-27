# ACE Skill Review Checklist

## Purpose
Use this checklist before returning generated ACE artifacts.

## When to use
Use this checklist after generating or updating ACE artifacts and before finalizing a response.

## Checklist

### Artifact correctness
- The correct artifact type was created.
- The generated files were placed in the correct project type.

### Project metadata — Application projects
When a new Application project is created, all three of the following must be present:
- `.project` contains **exactly 2 natures**: `com.ibm.etools.msgbroker.tooling.applicationNature` and `com.ibm.etools.msgbroker.tooling.messageBrokerProjectNature`. Do not add extra natures.
- `.settings/org.eclipse.core.resources.prefs` exists with `eclipse.preferences.version=1` and the `encoding/<project>=UTF-8` line.
- `application.descriptor` exists in the project root with the validated XML structure from `ace-projects.md`.

### Project metadata — Policy projects
- Any new Policy project contains the required metadata files.

### Message flow nodes
- Every message flow node uses a validated `xmi:type`.
- HTTP Input and HTTP Reply nodes use `ComIbmWSInput.msgnode` and `ComIbmWSReply.msgnode` — **not** `ComIbmHTTPInput` or `ComIbmHTTPReply`.

### Connector-specific
- Connector-specific rules were applied where relevant.
- Required schema files were created where relevant.
- Required policy files were created where relevant.

### Simplicity
- The flow topology is the minimum required to satisfy the request. Do not add Compute nodes, ESQL files, or transformation logic unless the user explicitly asked for transformation. A direct wire from Input to Reply is correct for a pass-through or echo pattern.

### Final response
- Version-specific assumptions were either confirmed or clearly stated.
- The final response includes a concise summary of what was created.
- If a new Application project was created, include the ACE Toolkit import guidance.

## Related files
- [`skills/shared/ace-projects.md`](ace-projects.md)
- [`skills/shared/policy-projects.md`](policy-projects.md)
- [`skills/shared/message-flow-rules.md`](message-flow-rules.md)
