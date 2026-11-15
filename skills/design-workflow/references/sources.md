# Sources and adaptation map

Original synthesis informed by [Figma’s “Claude skills for design” roundup](https://www.figma.com/resource-library/claude-skills-for-design/) and the upstream instructions linked below, reviewed in November 2026. Upstream manuals, scripts and templates are not redistributed. Tool-specific syntax, publication assumptions and fixed configuration were not imported. These sources establish ideas for Figma workflows, not feature parity in other editors.

The roundup has ten entries, with two named contract skills in the tenth entry (eleven named skills overall). The current voice workflow also has an Extract Voice companion, noted separately below.

| Article entry and source | Adapted idea | Location |
| --- | --- | --- |
| 1. [figma-use](https://github.com/figma/mcp-server-guide/blob/main/skills/figma-use/SKILL.md) | Verify document identity and hierarchy before writes; inspect partial failures; recoverable batches | workflow, verify |
| 2. [figma-generate-design](https://github.com/figma/mcp-server-guide/blob/main/skills/figma-generate-design/SKILL.md) | Find existing composites, fill gaps with approved linked parts and supported properties | assemble |
| 3. [figma-generate-library](https://github.com/figma/mcp-server-guide/blob/main/skills/figma-generate-library/SKILL.md) | Scope one family or required foundations; meaningful axes/slots; specimen instances and dependent checks | components |
| 4. [audit-design-system](https://github.com/edenspiekermann/Skills/blob/main/skills/audit-design-system/SKILL.md) | Read-only structural findings tied to real nodes; disclose inaccessible coverage | consolidate, verify |
| 5. [apply-design-system](https://github.com/edenspiekermann/Skills/blob/main/skills/apply-design-system/SKILL.md) | Compatible source replacement with retained geometry, content, overrides and before/after evidence | consolidate, assemble |
| 6. [create-voice](https://github.com/redongreen/uSpec/blob/main/skills/create-voice/SKILL.md) | Accessibility handoff tied to actual states, slots and visible focus stops | handoff |
| 7. [rad-spacing](https://github.com/nolanperk/rad-spacing/blob/main/rad-spacing.md) | Content hierarchy expressed through existing padding/gap scale; inspect rendered grouping | assemble |
| 8. [sync-figma-token](https://github.com/firebenders/sync-figma-token-skill/blob/main/skills/sync-figma-token/SKILL.md) | Source-authority-aware comparison of names/types/modes/aliases; scoped updates and fresh recheck | handoff |
| 9. [frontend-design](https://github.com/anthropics/skills/blob/main/skills/frontend-design/SKILL.md) | Task-grounded visual direction, deliberate hierarchy, real copy and purposeful motion | workflow, assemble |
| 10a. [cc-figma-component](https://github.com/nvillapiano/component-contracts-figma/blob/main/skills/cc-figma-component/SKILL.md) | Translate authoritative contracts to actual variants, slots and bindings; disclose unsupported features | components, handoff |
| 10b. [cc-figma-tokens](https://github.com/nvillapiano/component-contracts-figma/blob/main/skills/cc-figma-tokens/SKILL.md) | Preserve typed primitives, semantic aliases and dependency relationships | handoff |

The current [extract-voice companion](https://github.com/redongreen/uSpec/blob/main/skills/extract-voice/SKILL.md) interprets extracted component behavior; Create Voice lays an existing specification beside instances. This pack takes the accessibility-contract idea without requiring either plugin or implying that a static canvas verifies assistive technology. The article’s older frontend-design link was unavailable; the table uses Anthropic’s maintained repository.

## Five custom workflow ideas from the article

- **Design brief:** a compact outcome/constraints/states brief in workflow; reuse an existing brief.
- **Design review:** evidence-linked, read-only findings in verify; diagnosis does not authorize repair.
- **Information architecture review:** inspect task paths, labels, grouping and return paths in verify when navigation is in scope.
- **Handoff checklist:** component, token, asset, state and accessibility deltas in handoff.
- **Research synthesis:** trace supplied observations and contradictions into decisions in workflow; do not fabricate findings.

These ideas do not need five more skills: their outputs fit the existing task boundaries. Fixed spacing ratios, full variant matrices, mandatory publication, extra approval loops and tool-specific repair scripts were deliberately omitted. Conflicting upstream concurrency advice is resolved here with one writer per design document.

## Local experience

An early design session supplied failure observations from a real design session: detached duplication, missed shell duplicates, state/content coupling, icon rendering drift, changed IDs, partial failed mutations and unverified reopen. General invariants inform the skills; conditional mechanics live only in [OpenPencil notes](openpencil.md). These observations are not claims from the Figma article.

## User-requested orchestration

The review gates are a later explicit user preference, not an upstream requirement. The default workflow pauses for feedback between relevant stages. Explicit bounded or through-end continuation permits self-verified progress within that scope; a pause restores review gates. Specialist tasks remain available in isolation when explicitly requested.
