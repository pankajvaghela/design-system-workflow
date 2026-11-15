---
name: design-handoff
description: Align a design with existing code components, tokens and accessibility contracts, and prepare a concise implementation handoff. Use when implementation alignment or handoff is requested. For ordinary pack requests, enter through design-workflow unless its stage is already active or this specialist is explicitly requested in isolation.
---

# Align design and implementation

For ordinary pack requests, start with [design-workflow](../design-workflow/SKILL.md). If it already assigned this active stage, execute it without routing back: return a checked artifact and respect its current review/continuation mode and authorized boundary. Do not bypass a pending gate or expand that scope. An explicitly requested isolated specialist task is the routing exception and stays within its own scope.

Read the relevant product/design guidance, actual design sources, and available implementation components or token definitions. Treat existing agreed values and platform conventions as constraints. Do not infer implemented behavior from a rendered mockup or replace an established component library simply to match a drawing.

## Map the meaningful contract

For the requested scope, map design source names to existing or proposed code components. Record only implementation-relevant differences:

- Props/state axes and their values; content slots and nested component replacement.
- Parent versus child layout ownership, sizing behavior, spacing and responsive behavior actually specified.
- Typography, color, spacing, radius and other reused values mapped to existing semantic tokens.
- Interaction behavior, accessible role/name, keyboard operation, focus visibility and relevant selected/expanded/disabled state.

For token parity work, establish the authoritative source and permitted update direction. Compare mapped names, types, per-mode values and alias targets, not just resolved literals. Keep review read-only; apply only authorized deltas, preserve identities and alias relationships, then re-read affected bindings. Do not retire stale tokens without scope to do so.

Use a compact table or native component descriptions. Reuse existing tokens before proposing new ones. Distinguish a necessary new semantic role from a one-off literal; do not create a token system from every observed number. Keep approved fonts, icons and poster/image assets intact. Document asset identity or export needs when implementation actually requires them.

## Resolve discrepancies within scope

If requested to align the design, update the affected sources and check their instances. If asked only for a handoff, report mismatches with evidence rather than changing either design or code. Code implementation requires its own authorized scope; do not imply it happened because names were mapped.

Accessibility is part of the component contract. Describe focus order and transitions for the actual state and slot content, including activation and expected announcements. Keep shared intent together, with platform differences only where relevant. Inspect label clarity, contrast, focus treatment, target size and reading order where the editor provides evidence. For platform-specific thresholds or guidance, consult the relevant current official guidance. A static design cannot verify runtime keyboard navigation, screen-reader output or dynamic announcements: specify those as implementation acceptance checks. Do not represent unchecked behavior as accessible.

Deliver the smallest useful handoff: component/token mappings, required behavior, asset references and unresolved decisions that affect implementation. Separate approved facts, proposals and missing evidence. Include only states required by the requested flow, avoiding speculative flexibility.

For source contract repair use [design-components](../design-components/SKILL.md); for evidence quality use [design-verify](../design-verify/SKILL.md). Both are optional when the current handoff needs no document mutation.
