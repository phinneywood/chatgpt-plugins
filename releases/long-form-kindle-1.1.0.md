# Long Form 1.1.0 candidate

October 3, 2026. Combined package for the existing Long Form Kindle plugin; not uploaded or installed.

## Source and validation

- Existing personal skill identity retained; account-specific identity is recorded privately.
- Revised Work skill saved and remote bytes verified. SKILL.md SHA-256: `c7385e4459fe81fbd35591967b550801f57c5d45c19c6330ef82d9f8d8ecf6d6`.
- Builder emits `plugin.json`, `.app.json`, SKILL.md, agents metadata, and tool-contract.md. Packaged skill bytes match reviewed source.
- Archive SHA-256: `d529ab80acc6f53dac7d51d1c969790b28394b61ebcc7e3c42cc815af763dccb`.
- `.app.json` references the existing registered app mapping in the package; creates no new connector or scopes. Display name becomes Long Form.
- Native skill validator passed. Independent preparation-only and DOCX-to-custom-issue forward tests passed; no delivery call made.

## Runtime evidence and limits

- Existing skill-only Long Form Kindle 1.0.0 was installed; the account-specific installation pointer is retained privately.
- Its native skill and contract reader were previously verified in fresh ordinary Chat; the verification conversation is retained privately.
- Existing Long Form connector was connected; its account-specific installation pointer is retained privately. Authenticated profile/history/status reads succeeded October 3. Antonio confirmed iPhone connection.
- User video demonstrates successful Kindle import of the original LangGraph issue, with flattened formatting. Backend repair https://github.com/phinneywood/long-form/pull/77 merged as `c036880a11812417c5bcc8dd5ae4031bc548b8c9`; worker v68, app-api v62, MCP v15 deployed.
- Fixed title cover, named chapter navigation, safe Markdown/HTML, preserved code/lists, and removed synthetic original-source links. 125 Deno and 78 Node tests passed; three entrypoint type checks passed. Reconstructed LangGraph issue retains every original paragraph and all 22 preformatted blocks; canonical EPUB QA reports 18 entries.
- Uploading a combined version to the generated app wrapper was rejected for a manifest-name mismatch. Its Download ZIP control yielded no download, so no further guessed wrapper identities were tried.
- Automatic approval review rejected an attempted update to the separate Long Form Kindle plugin: it could preserve the confusing duplicate setup, and separate-plugin mutation was not explicitly authorized. No combined upload occurred. Specific approval is required to update this existing package, verify it reuses the connected account and loads in fresh ordinary Chat, then uninstall the superseded connector-only plugin. Do not uninstall before successful verification.
- Combined package ordinary Chat and iOS runtime remain unverified. No replacement issue emailed. User approval for the corrected issue is pending.

Official packaging: https://developers.openai.com/plugins/build/plugins. Private registered-app reference handling must be verified in this personal uploader; static package validity is not installation evidence.

Personal installation identifiers and verification links were moved to private deployment records on October 3, 2026. This cleanup preserves the evidence above and the required `.app.json` integration mapping. It does not remove historical copies or establish a newer runtime state.
