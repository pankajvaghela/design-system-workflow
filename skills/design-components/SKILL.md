---
name: design-components
description: Create or repair real reusable design components, properties, variants and slots in a visual editor. Use for component source work, not every screen edit. For ordinary pack requests, enter through design-workflow unless its stage is already active or this specialist is explicitly requested in isolation.
---

# Build reusable design components

For ordinary pack requests, start with [design-workflow](../design-workflow/SKILL.md). If it already assigned this active stage, execute it without routing back: return a checked artifact and respect its current review/continuation mode and authorized boundary. Do not bypass a pending gate or expand that scope. An explicitly requested isolated specialist task is the routing exception and stays within its own scope.

Inspect the current canvas, relevant product guidance and existing sources first. Preserve approved palette, theme modes, typography, icons, images and dimensions unless the request changes them. Discover editor capabilities and use actual component/instance objects; disclose unsupported variant or slot behavior rather than simulating it under misleading names.

Use approved typography roles from the [typography specification](../design-foundations/references/typography-specification.md); retain native text-style links and document intentional exceptions. Use approved semantic color roles and theme bindings from [design-foundations](../design-foundations/SKILL.md). Check representative states in every required theme. If foundations are missing or need material changes, return that decision to the orchestrator before dependent source construction; do not invent a palette inside component work.

## Define a small useful contract

For each concept being created or changed, identify:

- Semantic name and responsibility, compatible with implementation names.
- State properties and allowed values; content properties and replaceable slots.
- Layout ownership: what the parent positions, what the component lays out, fixed/flexible dimensions and spacing.
- Interaction and accessibility expectations, including label, role and relevant keyboard/focus behavior.

Keep this contract in native descriptions/properties when practical. Use a short note only for facts the editor cannot represent. Do not manufacture a document for an obvious control.

## Build the source before populating screens

1. Find the existing canonical source or set, including shell controls such as headers and navigation. Prefer repairing it to creating a duplicate. Inventory inbound instances before changing its public contract.
2. Build required small controls, then domain components, then section compositions. Each semantic concept has one canonical source or set, except deliberately distinct structures with distinct responsibilities. Repeated section compositions should also be reusable when the requested screens need them.
3. Model state through explicit properties/variant axes. Keep sample text, imagery and nested content independent of state. A bookmark change must not silently swap the event, image or copy. Structurally different layouts can use separate components rather than one overloaded variant set.
4. Create real content slots before inserting replaceable instance content, where the editor supports slots. Otherwise use supported text/image/component properties or document the limitation. Do not append arbitrary children into instances or detach them to hide an unsupported contract.
5. Instantiate the sources and test their contract with differing real content. Cover the requested states and obvious states needed for the specified interaction; do not build a speculative Cartesian product of variants.

Name layers by role, not coordinates, colors or sample content. Prefer `EventCard`, `EventListItem`, `Bookmarked=Yes|No`, and `MonthSection/Collapsed=Yes|No` as illustrative naming patterns, not required product concepts. Keep content selection separate from those axes.

Keep canonical sources in the existing shared component page or library. Do not create another source copy for each screen, list/card view or authentication flow. Repeated sections, such as a title/actions block, date/time row, location row or ticket action, can be reusable compositions when they have a stable responsibility. A one-off label does not need its own component. Shared controls should inherit approved typography and icon sizing from foundations.

## Check the resulting objects

Reinspect returned objects: conversion may create a new identifier. Confirm source type, variant properties, nested sources, slot ownership and instance links. Render both the source and representative linked instances; successful creation is not visual proof. Check long or missing content only where the contract permits it, plus a second content sample to catch state/content coupling.

For screen composition, optionally use [design-assemble](../design-assemble/SKILL.md). For broad deduplication use [design-consolidate](../design-consolidate/SKILL.md). Editor-specific failures belong in [OpenPencil adapter notes](../design-workflow/references/openpencil.md), read only if applicable.
