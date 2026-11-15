# Typography specification

Read when creating, changing, applying or handing off a type scale. The product's approved styles remain authoritative. This is a specification format and an illustrative starting scale, not permission to replace an existing system.

## Workflow and deliverable

1. Inspect existing fonts, text styles, target platforms and representative screens. Identify missing roles or inconsistent overrides before proposing values.
2. Define the required mobile roles first when the brief is mobile-first. Include desktop only when requested; mark unreviewed values as proposed.
3. Create native named text styles and an editable typography specimen on the existing foundations page alongside colors. Use one row per role and realistic content, not only alphabet samples.
4. Verify the specimen in a real screen at native width and 100% scale. In review mode, obtain approval before propagating a new scale; explicit continuation still requires these checks.
5. Apply approved styles to canonical controls, domain sections and then linked screens. Audit relevant overrides so older hard-coded sizes do not mask source updates. Preserve deliberate brand wordmarks and other documented exceptions.
6. Inspect affected sources and representative instances, save the native file, and report remaining prototype/runtime checks separately.

For each role record: semantic name, intended use, font family and fallback, weight, size, line height, tracking, casing, platform/viewport scope, native style identity and approval status. Record wrapping or truncation only where its component contract needs it. Text color uses existing semantic color roles, rather than a separate copy per type style.

## Example compact app scale

These values are an illustrative starting proposal inspired by a mobile event app, not an accessibility standard or a requirement for every product. Use the approved product font; Inter is an example. Desktop values are a starting proposal and require their own review. Values are size/line-height in design pixels, not device pixels; implementation must map to platform text units and user text scaling.

| Semantic role | Mobile example | Desktop proposal | Weight | Intended use |
| --- | --- | --- | --- | --- |
| Title | 22/28 | 28/36 | 600 | Screen or event title |
| Section | 18/24 | 22/28 | 600 | Section heading |
| Item | 16/22 | 18/24 | 600 | Card/list title |
| Body | 14/20 | 16/24 | 400 | Short supporting copy |
| Reading | 16/24 | 16/26 | 400 | Longer descriptions |
| Label | 14/20 | 14/20 | 600 | Buttons and fields |
| Meta | 12/18 | 13/20 | 400 | Dates and supplementary facts |
| Caption | 11/16 | 12/18 | 400 | Nonessential annotations |
| Eyebrow | 11/16 | 12/18 | 600 | Short category label |

Start tracking at zero unless the product calls for another value. Use sentence case by default; uppercase belongs only to a deliberately specified role. Do not use caption size for essential instructions or shrink text just to fit a row. Desktop can retain mobile control sizes while increasing heading size and reading width; a single scale multiplier is not a responsive specification.

Native names may follow `Type/Mobile/Title` and `Type/Desktop/Title`, but preserve an existing naming scheme. If platforms share identical values, reuse a style or alias where supported instead of duplicating it without purpose.

## Icon specification alongside type

Record semantic action, asset/source, visible bounds, stroke weight, color role, interaction target and accessible name separately. A compact UI may start with 16–20 px glyphs and larger interaction targets, but validate the target against applicable platform guidance. A small visible icon does not justify a small hit area. Check optical alignment with text and shared leading/trailing insets.

Share, external link, expand and bookmark require distinct meanings. Provider logos retain their official assets and applicable branding rules. Icon-only controls still need a specified accessible name; a design label does not implement it.

## Specimen and acceptance checks

- Show a long title, two-line item title, body paragraph, input label/value/helper, date/location row and icon action. Check line height, glyph availability, truncation and alignment at the target viewport.
- Confirm real native style bindings in sources and instances, not merely matching numeric values. Check each materially different layout affected by a source change.
- Keep captions, notes and specimen labels outside prototype screen frames. Preserve the intended viewport and scrolling boundaries.
- Specify implementation acceptance for browser zoom, native text scaling and long/localized text. Static inspection cannot establish runtime reflow, screen-reader behavior or accessibility conformance.
- Report approved values separately from proposals, missing fonts, untested breakpoints and runtime checks. Do not claim desktop approval from a mobile specimen.
