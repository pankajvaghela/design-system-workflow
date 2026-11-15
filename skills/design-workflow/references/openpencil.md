# OpenPencil adapter notes

Read only when using OpenPencil. These observations came from one problematic editing session; verify behavior in the installed version. They are not an API specification or evidence of parity with Figma.

## Translate the abstract operations

Discover the available connector operations for inspection, component creation/conversion, variants, properties, slots, instances, layout, rendering and save/reopen. Use their current documented arguments. Do not copy endpoints, credentials, node IDs or machine paths from another session.

- Component conversion/`create_component` returned a **new ID** in the observed session. Reinspect the returned object and update references. Save/reload and lazy page loading may also remap IDs; rediscover current identities.
- Updating descendant positions inside an `INSTANCE` was rejected, while root-instance placement worked. Respect source layout ownership and supported instance properties.
- Arbitrary children could not be appended under an instance. Establish a real slot on the source first, then insert instance content using supported operations. Failed reparenting sometimes partially moved or orphaned the source; inspect both locations after any error.
- Cloned icon vectors displayed wrong glyphs with suspected vector-cache involvement. Diagnose with source/instance renders first. Fresh approved inline SVG content repaired the visible glyphs in that case; do not automatically replace all icons, change their approved identity or assume the same cause for every glyph issue.
- Explicit variant dimensions were more reliable than scattered shape overrides. Keep structural layout choices separate from state and content properties.

## Illustrative relationships, not prescribed product names

The session needed separate `EventListItem` and `EventCard` structures, each with `Bookmarked=Yes|No`; `MonthSection` with `Collapsed=Yes|No`; a list/card view toggle; and a reusable event section. Poster/copy selection had to stay independent of bookmark state. Replacement screens needed exact spacing, the first item's saved state and collapsed months preserved. Other products should use their own concepts.

Duplicate header, search and navigation sources remained after fixing event-card duplication. Audit the affected document broadly before cleanup and migrate inbound links before removing old sources. Creating detached repeated cards first and converting them later caused avoidable cleanup; final assembly should use linked instances.

## Bounded diagnosis and honest persistence

A blank canvas, duplicate imports and missing resumed component references occurred. Inspecting all pages before one retry helped one installation, possibly because of lazy loading; this is a diagnostic option, not a guaranteed repair. Do not repeatedly import or replay creation batches. Check actual state after an error and stop after a failed evidence-backed retry.

The live render was repaired, but save/reopen verification stalled. Such a result supports “visually repaired,” not “persistence verified.” Use a safe isolated verification copy and bounded waits where possible. Never overwrite the live file from a backup while the editor holds newer changes. Keep one writer per document and resume from fresh state.
