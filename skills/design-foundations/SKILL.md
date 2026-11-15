---
name: design-foundations
description: Decide or refine a product color palette and semantic theming before component construction. Use when visual foundations are missing or explicitly being changed. For ordinary pack requests, enter through design-workflow unless its stage is already active or this specialist is explicitly requested in isolation.
---

# Establish palette and theming

For ordinary pack requests, start with [design-workflow](../design-workflow/SKILL.md). If it already assigned this active stage, execute it without routing back: return a checked artifact and respect its current review/continuation mode and authorized boundary. Do not bypass a pending gate or expand that scope. An explicitly requested isolated specialist task is the routing exception and stays within its own scope.

## Start with approved foundations

Inspect product/design guidance, existing palette, tokens, theme modes, typography and representative screens. Establish the authoritative source. Reuse approved foundations; a new screen or component does not authorize rebranding. If they already satisfy the task, record that reuse and return without inventing a new palette or review cycle. Changing an approved foundation requires explicit scope; report conflicts rather than silently replacing it.

When foundations are undecided, propose a small coherent direction grounded in the audience, brand and required UI. Offer alternatives only for a real unresolved decision. Decide which themes are required by the brief: do not automatically add light, dark or high-contrast modes. Theme switching behavior (system preference, manual choice, persistence) is a separate product decision; identify it only if relevant, and do not imply a mockup implements it.

## Define only the roles the UI needs

- Keep brand/base colors separate from semantic roles such as background, surface, text, border, action, focus and feedback. Reuse existing names and scales; avoid tokenizing every literal or generating unused shades.
- Map the same semantic roles to values in each required theme. Preserve existing aliases and identities. Selected, bookmarked, disabled and error states must remain distinguishable in every required theme, with cues beyond color where needed.
- Use editor-native variables, modes or styles when supported. Bind components to semantic roles; do not duplicate an entire component library per theme. If mode switching or bindings are unsupported, provide clearly labeled previews and a small mapping table, and state that they are not functioning theme bindings.
- Preserve approved typography, icon style and imagery. Confirm how the palette works with them; redesigning them is not implied by color work.

## Produce a reviewable foundation

Show palette roles and representative UI samples in every required theme, including text, surfaces, action/focus and relevant selected states. Temporary samples are exploration artifacts, not duplicate canonical components. Check actual foreground/background pairs, including transparency and image overlays; consult current official accessibility guidance for applicable contrast thresholds. Record measured results and unchecked combinations instead of claiming accessibility from appearance. Static previews cannot establish runtime theme or assistive-technology behavior.

Return the chosen/proposed palette, semantic role mapping, required theme modes, representative previews, contrast evidence and unresolved decisions. In default workflow mode, wait for explicit approval before dependent component work; explicit continuation still requires verification and cannot resolve a genuinely missing user decision. Revisions that materially change an approved foundation return to the orchestrator's review gate.

Pass approved roles and bindings to [design-components](../design-components/SKILL.md), and implementation mappings to [design-handoff](../design-handoff/SKILL.md) only when needed. Do not publish or modify application code as part of this stage.
