# FigCraft reference notes

Read only when using FigCraft. Checked November 15, 2026 with desktop and CLI version **0.18.1**. These notes distinguish an isolated engine test from live desktop behavior; they do not establish full editor parity or production stability.

## Observed in an isolated headless test

Using the installed `figcraft-cli`, a synthetic event component was created in a new document, without modifying an existing user document:

- `component.addProperty` bound a text property to a child layer. Two `instance.create` calls produced linked instances with different title overrides.
- `component.addVariant` created a component set with `Bookmarked=No` and `Bookmarked=Yes`. `instance.setProperties` switched one instance to Yes while preserving its distinct title. The second instance stayed No with its own title.
- Editing the saved variant's child label with `node.set` propagated to its linked instance without replacing the title override. Creating a variant duplicates its contents; the intended visual difference still needs to be authored explicitly.
- A color collection with Light and Dark modes bound the surface and title fill. Setting Dark on a parent frame resolved the nested instance's surface and text to the expected dark-mode values. Unbound literal colors stayed literal; a mode switch does not automatically make every color theme-aware.
- Native `.figcraft` save followed by reopening in a fresh CLI process preserved the two inspected instance trees exactly, including source links, text overrides, variable bindings and resolved colors.
- Rendering the reopened file produced an inspectable PNG. Adding a variant expanded the source set's layout; the initial preview overlapped a specimen placed below it. Moving the specimens clear of the source set corrected the preview. Leave room for sources and inspect the render rather than assuming a fixed source height.

Commands were obtained from this installed version's `--help` and `commands` output. Batch step references (`as`, `$ref`) worked for objects created earlier in a command script. Use returned IDs and inspect the actual objects; numeric IDs in a test are not portable identifiers.

## Execution mode and evidence boundary

`figcraft-cli run` edits a headless document. It does not edit or inspect the file currently visible in the desktop app. The tested native file round trip and rendering are headless results, not proof of desktop save/reopen behavior.

The installed app's accessibility window title was readable, but desktop screenshot capture failed in the test environment. No attached MCP session was exercised, and the user's imported design was not mutated. The user's report that their import looked correct is useful context, not an independent structural or visual import audit.

For work that must be visible in the app, consult the installed version and current [MCP documentation](https://github.com/storytold/figcraft/blob/main/docs/mcp.md) for attached mode. Upstream documents `figcraft-cli mcp --attach <port>` with an app control channel. This connection route is documented but untested here. Do not restart a user's app or discard unsaved work just to enable it; select the intended document explicitly where supported.

Upstream also warns that an attached edit may have completed before a transport reply is lost. Inspect state before retrying; do not replay a creation batch blindly. This is a documented precaution, not a failure observed in this test.

## Apply the shared workflow

Keep the same component-first stages and explicit review gates. Discover actual supported commands before mutation. Plan content properties independently from variant state; inspect `mainComponent`, `componentProperties`, children and bindings as well as the rendered result. Use explicit parent-relative coordinates and verify reparented placement. Do not transfer OpenPencil-specific repair assumptions to FigCraft.

For migration, keep the source intact and inspect a copy. Native reopen success for a synthetic file does not verify `.fig` import fidelity. Check fonts, images, source links, variants, nested instances, overrides, layout and themes in the migrated document before adopting it.

Not tested: full imported-document fidelity, attached MCP, slots, nested component swaps, auto-layout propagation, image overrides, prototypes, undo/recovery, concurrency, or extended-session stability. These remain capability checks for the task that needs them, not reasons to build speculative workarounds.

## Sources

- [CLI documentation](https://github.com/storytold/figcraft/blob/main/docs/cli.md)
- [MCP and control modes](https://github.com/storytold/figcraft/blob/main/docs/mcp.md)
- [Feature depth and limitations](https://github.com/storytold/figcraft/blob/main/docs/target-app-parity.md)

Use these references for current syntax; the installed binary's command discovery determines which operations are available locally.

## Subsequent attached-session evidence

Later on November 15, 2026, the attached FigCraft MCP session was used to edit the existing Bailamigo native document: text-style application, component creation and linked instances, content overrides, source/page organization, native screen-frame edits and prototype destination wiring. Native screenshots were inspected and save_file confirmed the existing document path. This extends the earlier headless-only evidence above; it does not establish a fresh desktop reopen, full import fidelity, exercised prototype interactions or runtime form behavior.
