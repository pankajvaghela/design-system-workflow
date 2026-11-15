---
name: design-assemble
description: Assemble or update design screens from linked component instances while preserving layout, content and requested states. Use once screen architecture is sufficiently decided. For ordinary pack requests, enter through design-workflow unless its stage is already active or this specialist is explicitly requested in isolation.
---

# Assemble screens from linked components

For ordinary pack requests, start with [design-workflow](../design-workflow/SKILL.md). If it already assigned this active stage, execute it without routing back: return a checked artifact and respect its current review/continuation mode and authorized boundary. Do not bypass a pending gate or expand that scope. An explicitly requested isolated specialist task is the routing exception and stays within its own scope.

Inspect the current screen, its layout and source components before editing. For replacement work, capture exact screen position, dimensions, spacing, ordering, content, interaction states and approved assets. Do not substitute a visually similar fresh screen that loses these details.

Use the editor's real instance operations. Reuse canonical controls, domain components and reusable sections. If a source lacks a necessary property or slot, resolve its contract before dependent assembly. Under orchestration, route material or out-of-stage source repairs back to the orchestrator; do not treat the gap as new approval to change an accepted contract. Local corrections already authorized for this stage can proceed. [design-components](../design-components/SKILL.md) can guide authorized source work. If architecture is still unresolved, explore with minimal temporary parts before turning the chosen structure into reusable sources.

## Compose without breaking ownership

- Put linked instances inside screen/layout frames. Nonreusable screen containers and unique content can remain frames; reusable UI should not become cloned or detached frames.
- Use existing spacing tokens to express grouping: container padding owns insets and sibling gaps own separation. Keep component interior spacing with its source; inspect grouping at the requested widths.
- Position and size at the level that owns layout. Change root-instance placement or supported instance properties, not arbitrary descendant coordinates that violate the source contract.
- Insert content only through supported properties or explicit slots. Configure nested content independently from state; changing a saved/bookmarked state must preserve the chosen content.
- Use explicit layout/state axes or distinct structural components. Do not fake a different structure using scattered instance overrides that the source cannot express.
- Reuse section compositions across screens where their behavior and layout are shared. Keep intentional one-off content local. A screen-owned wrapper of linked children can be an honest limited fallback, but is not equivalent to a reusable section with configurable slots.
- Use the existing spacing scale: container padding for insets, layout gaps for peers, and meaningful separation between groups. Preserve approved spacing in migration work; do not impose a new ratio or token scale.

For an existing screen, change the smallest subtree needed. Preserve selected/saved items, collapsed sections, active navigation and other intentional initial states. For a new screen, implement the requested realistic content and states without inventing extra product behavior.

## Make screen frames usable as screens

Keep each prototype destination frame scoped to the actual viewport and intended scroll content. Put screen numbers, rationale and review notes outside it; a presentation board surrounding a phone is not the phone's prototype screen. Preserve the user's page organization. For related flows on one page, use consistent frame dimensions, spacing and ordered rows by journey rather than one page per state.

Use the approved role mapping from the [typography specification](../design-foundations/references/typography-specification.md); do not infer new font sizes from a zoomed screenshot. Apply approved text styles and compact icon sizes to linked sources and supported overrides. Align trailing actions to the shared content inset, not an arbitrary text-box edge; align leading metadata icons with their text group. Use realistic long copy to check one-line metadata layouts instead of shrinking text to force a fit.

For cover/header changes, follow the latest accepted arrangement. Treat image cropping, solid header versus overlay, gradient strength, button contrast and scrolling as separate choices; do not reintroduce a rejected overlay. Keep selectable values per item separate from unrelated profile roles or skills. When adding flow steps, update progress labels, ordered placement, forward/back links and skip destinations together. Mark sample selections and unimplemented inputs outside the screen.

## Inspect after each risky mutation

A failed move, conversion or reparent operation may have partially changed the document. Inspect source and destination before retrying. Confirm the instance remains linked, its content is present and no source was orphaned. Re-resolve identifiers after conversion or reload.

Render the assembled screen and representative sources. Compare against the captured layout and intended hierarchy, including spacing, crop, typography, icons and state. Inspect source references as well as pixels; appearances alone cannot prove reuse. Remove temporary exploration objects only when they are known to be disposable and no longer referenced.

Report the changed screens and actual verification status. Use [design-verify](../design-verify/SKILL.md) for broader structural or persistence checks, and the optional [OpenPencil notes](../design-workflow/references/openpencil.md) only for that editor.
