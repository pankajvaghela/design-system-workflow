# OpenAI submission preparation

Prepared November 15, 2026 for package **0.1.5**. This is a skills-only package maintained by Pankaj Vaghela. No submission, approval or directory listing is claimed.

## Listing

The authoritative copy is `extensions.com.openai.interface` in [plugin.json](../plugin.json). The compatibility manifest carries matching metadata for older hosts.

| Field | Prepared value |
| --- | --- |
| Name | Design System Workflow |
| Subtitle | Reusable design, reviewed |
| Publisher | Pankaj Vaghela; must match the verified portal identity |
| Category | Art & Design |
| Description | Full task, audience and capability-limit description in the manifest |
| Starter prompts | Three prompts covering staged design, component review and typography/color/icon foundations |
| Icon | Original square SVG of connected components and a review check; used for composer and listing |
| Website | Public GitHub repository |
| Support | Public SUPPORT.md and GitHub Issues |
| Privacy | Public PRIVACY.md |
| Terms/license | Existing MIT LICENSE; no additional service terms |

The plugin supplies seven related skills. No server, authentication, lifecycle hooks, external app references or executable runtime are bundled. Optional onboarding is omitted: installation should not initiate a design task. Invoke `design-workflow` when ready.

## Gaps addressed

- Replaced the overlong subtitle with a directory-length subtitle.
- Added the portable root manifest, full description, publisher, capabilities and three starter prompts.
- Added a square icon and explicit public support/privacy links.
- Kept Codex compatibility metadata aligned with the portable package.
- Made user-instruction precedence, reference-content boundaries and missing editor access explicit in the orchestrator.
- Kept MCP-only review fields absent rather than inventing tool calls, credentials or a demo recording.

Version 0.1.5 fixes the upload ZIP by excluding the repository-only marketplace manifest. It retains the 0.1.4 changes, which make platform priority and editor choice intent-led, adds project preferences and a platform-aware typography specification, compact icon guidance, native-file workflow, organized flow checks and source deduplication guidance. Plugin metadata and all relevant specialist links are aligned.

## Validation evidence and limits

Local checks cover the portable JSON schema, listing field limits, manifest parity, icon dimensions and safety, all seven skill headers, referenced files, relative links and ZIP contents. These checks cannot replace OpenAI's metadata/skill scans or certify acceptance.

The prior public v0.1.0 skills were installed in a clean temporary project for Codex and Claude Code using Skills CLI 1.8.1. The 0.1.1 candidate was also installed from the extracted submission ZIP into a clean temporary project for both hosts. All seven skills, supporting file contents and relative references passed verification. Telemetry was disabled for these tests.

[Behavioral scenarios](../evaluations/scenarios.md) remain review fixtures, not an executed live editor suite. Before submission, perform a fresh host smoke test: request a component contract using fictional supplied content, confirm the first review gate stops, give feedback without approval, then approve one next stage. Check that missing editor access produces a clear limitation rather than invented edits. A full connected-editor design session is still unverified.

## Build the upload ZIP

From the repository root, after reviewing the exact files to include:

```sh
mkdir -p dist
rm -f dist/design-system-workflow-0.1.5.zip
zip -r dist/design-system-workflow-0.1.5.zip plugin.json .codex-plugin/plugin.json skills assets README.md LICENSE PRIVACY.md SUPPORT.md evaluations submission -x '*.DS_Store' '*__pycache__*' '*.pyc'
unzip -t dist/design-system-workflow-0.1.5.zip
```

The manifest and `skills/` must be at the archive root. Exclude `.agents/plugins/marketplace.json`: it is only for repository installation. Including it makes the uploader interpret this as a marketplace archive, whose remote-only entry has no local plugin to upload. Build a fresh ZIP, since updating an existing ZIP can retain excluded entries. Use the named release asset, not GitHub’s automatic source archive. Do not include `.git`, caches, personal files or nested `dist` output. The archive contains only the plugin and its public documentation. Rebuild after any package change; use a new version after publication rather than replacing a published release's contents.

## Remaining owner and portal steps

1. Review the icon, public listing, privacy statement and support route for accuracy.
2. Confirm the owner organization/project, submission permissions and verified publisher identity in the OpenAI portal.
3. Upload the ZIP as a skills-only draft. Inspect metadata and skill scan findings; resolve them before submitting. There is no server to connect.
4. Confirm the category and geographic availability in the portal. No country allowlist or translations are asserted by this package.
5. Complete the required policy attestations personally and submit when ready. Approval and final publication are separate actions.

No portal upload, scan, account verification, legal attestation or submission has been performed during preparation. No country availability is promised. GitHub-hosted policy/support pages must remain public and accessible.

## Official references

- [Package format](https://developers.openai.com/plugins/build/plugins)
- [Submission and listing field reference](https://developers.openai.com/plugins/deploy/submission)
- [Plugin guidelines](https://developers.openai.com/plugins/plugin-guidelines)
- [Skill authoring and instruction boundaries](https://developers.openai.com/plugins/build/skills)
- [Portable manifest schema](https://agent-plugins.org/schemas/1.0.0/plugin.schema.json)

Requirements can change; recheck the current portal findings before submitting. Skills-only metadata has different requirements from an MCP app, while the general plugin guidelines still apply.
