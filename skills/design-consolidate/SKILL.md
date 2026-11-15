---
name: design-consolidate
description: Audit and consolidate duplicate or detached design components safely, preserving inbound instances, user content and current screen layouts. Use for explicit library cleanup or demonstrated source duplication. For ordinary pack requests, enter through design-workflow unless its stage is already active or this specialist is explicitly requested in isolation.
---

# Consolidate an existing design library

For ordinary pack requests, start with [design-workflow](../design-workflow/SKILL.md). If it already assigned this active stage, execute it without routing back: return a checked artifact and respect its current review/continuation mode and authorized boundary. Do not bypass a pending gate or expand that scope. An explicitly requested isolated specialist task is the routing exception and stays within its own scope.

Start with a read-only inventory broad enough to find all sources and inbound instances in the affected document. Inspect every relevant page, including shell/navigation components, hidden library pages and alternate screens. Names alone do not establish equivalence. If the tool cannot inspect part of the document, mark the audit partial and avoid deleting sources whose references cannot be established.

For an audit-only request, stop at evidence-linked findings: affected sources/instances, expected versus observed relationships, impact and suggested remediation. Do not migrate or delete anything unless the user authorized fixes. The migration steps below apply only to that authorized scope. For token-binding or code-parity findings, use the relevant checks in [design-handoff](../design-handoff/SKILL.md).

## Decide what is actually duplicate

Map semantic concepts to canonical sources/sets, variant axes, nested sources, content contracts and inbound instances. Distinguish true duplicates from intentionally different structures or versions. A compact list item and a rich card can be valid distinct components; two indistinguishable header sets are likely duplication. Preserve separately configurable content even when samples happen to match.

Partial reference visibility can still permit a verified migration of known instances; retain the old source and avoid shared contract changes with unknown effects.

Choose a canonical source based on contract correctness, approved visuals, valid links and downstream use, not simply age or name. Record a short old-source → new-source mapping only when needed for a multi-step migration. Do not expand a local repair into an unrelated visual redesign.

## Migrate references before deleting sources

1. Capture a safe checkpoint and current screen renders/layout values. Work with one document writer. Never recover by replacing a live file that contains newer user edits.
2. Bring the canonical source up to the required contract before migrating instances. Preserve supported content properties, slots, variants, layout and accessibility meaning.
3. Replace inbound references using supported editor operations. Preserve instance content, meaningful overrides, coordinates, spacing and initial state. If overrides cannot migrate faithfully, repair that instance explicitly and verify before proceeding.
4. After each risky operation, inspect actual source/destination state, even on error. Confirm that no content disappeared or became orphaned. Do not blindly repeat a partially applied mutation.
5. Render affected sources and screens, then recount references. Remove an obsolete source only when no remaining instance or nested source needs it and the available inspection is sufficient to establish that fact. If references remain uncertain, leave it and report why.

Check the whole affected library again, including header/search/navigation sources; fixing only domain cards can leave most duplication intact. Completion means the intended concepts have one valid canonical source/set, their instances remain linked, and no content or screen state was lost. Report intentional exceptions and incomplete visibility.

Use [design-verify](../design-verify/SKILL.md) for persistence evidence. The [OpenPencil adapter notes](../design-workflow/references/openpencil.md) cover conditional recovery behavior, not a mandatory repair recipe.
