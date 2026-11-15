---
name: design-verify
description: Verify design rendering, component links, saved persistence and prototype claims, or resume interrupted editor work from current state. Use for design verification and recovery, not as proof of implemented code. For ordinary pack requests, enter through design-workflow unless its stage is already active or this specialist is explicitly requested in isolation.
---

# Verify design integrity and persistence

For ordinary pack requests, start with [design-workflow](../design-workflow/SKILL.md). If it already assigned this active stage, execute it without routing back: return a checked artifact and respect its current review/continuation mode and authorized boundary. Do not bypass a pending gate or expand that scope. An explicitly requested isolated specialist task is the routing exception and stays within its own scope.

Match verification depth to the change. A label edit needs a local render and appropriate save check; a library migration needs source/reference and affected-screen checks. Begin with the current document, product constraints and requested outcome. Reacquire node identities after reload or resume rather than trusting an old script or ledger.

## Collect independent evidence

| Claim | Evidence needed |
| --- | --- |
| Visually correct | Render/inspect affected sources and linked screens at useful resolution; compare layout, copy, imagery, glyphs and requested state |
| Structurally reusable | Inspect real component types, variant properties, source links, nested relationships and content/slot independence |
| Saved | Editor/file save confirmation tied to the current document state |
| Reopened correctly | Close/reopen or reload a safe isolated verification copy and repeat relevant structural/render checks |
| Prototype works | Exercise the requested interactions and observe resulting states/navigation |
| Implemented in code | Inspect and run the relevant implementation checks; a design artifact provides no such proof |

A successful tool response proves only that the operation returned. When a shared source changes, render that source and representative linked instances because one can look correct while the other is broken. For a supported local content override, inspect the affected instance, its link, state and reflow; unrelated sources and screens need no render. In migration work, compare content and initial state as well as geometry and reference counts. Check that changing one state does not select different sample content.

For a review-only request, keep diagnosis read-only. State the inspected pages/screens/states and any inaccessible scope. Tie findings to actual frames/layers and evidence, with expected versus observed behavior and impact; omit unverified defects. When navigation or flow is in scope, trace the primary task from entry to outcome, checking predictive labels, grouping, context and return paths. Do not expand every local review into a full information-architecture audit.

## Test persistence without risking live work

Use the editor's supported save/reopen facilities. When reopening could disrupt the user's current document, prefer an isolated copy containing the saved result. Keep the live document and newer user changes intact. Set a bounded wait appropriate to the tool; if reopen stalls, stop and report persistence as unverified. A successful save is not proof of a successful reopen.

## Recover from observed state

For a blank canvas, missing sources or a failed mutation, first inspect document identity, loaded pages and source/instance relationships. A tool error may still leave a partial change. For a confirmed orphan, preserve the existing object and its content; restore it only to a placement established by current pre-error evidence or a verified supported destination, then recheck ownership and links. Do not guess from a divergent backup. Use a read-only diagnosis, then one evidence-backed retry for a suspected transient condition. If the same problem persists, stop mutating and report the unresolved state instead of looping imports, reloads or repair scripts.

Do not overwrite live files from backups, discard newer user edits or rerun non-idempotent creation batches on resume. Compare source/checkpoint and current state before a recovery decision. Obtain fresh identities after any conversion/reload. Editor-specific mechanics are optional: read [OpenPencil notes](../design-workflow/references/openpencil.md) only for that editor.

## Report precise completion

State what changed and which of visual, structural, save, reopen, prototype and code checks were actually completed. Mention only relevant categories, with concrete remaining limitations. If a check failed, preserve the useful completed work and say what evidence is missing. Never turn an untested persistence or interaction claim into a completion assertion.
