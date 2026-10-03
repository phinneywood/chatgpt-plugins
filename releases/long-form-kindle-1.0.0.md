# Long Form Kindle 1.0.0

Date: October 3, 2026. Target: personal ChatGPT Work skill. Ordinary Chat/iOS runtime is unverified.

| Gate | Result | Evidence and boundary |
| --- | --- | --- |
| Static package | Passed | Native quick_validate and portable checker pass; packaged SKILL.md SHA-256 360fb6da3c7f10fe33587cb24afa71d7d8aa71b426693e848bda7f3c210f720d. |
| Installation persisted | Passed | Personal skill saved and reconciled; remote instruction bytes match reviewed source. |
| Source equality | Passed | Native stored SKILL.md and this source have the same SHA-256. |
| Native discovery/reader | Unverified | Current session catalog/reader snapshot does not expose the newly saved identity; reopen Skills or use a fresh session. |
| Behavior | Passed, limited | Independent agent given only skill plus supplied Deployment Checklist text preserved ordered sections, planned send_custom_issue with citations, and did not send a prepare-only request. No Long Form tools were exposed. |
| Resumption | Backend passed | Mocked provider-accepted delivery followed by final-status failure retries without another send; frozen bytes and QA are retained. |
| Ordinary Chat cloud release | Not installed | ZIP validated; no upload or installation performed. |
| Authenticated live send | Unverified | Long Form connection unavailable in this session; no new email was authorized/sent by the build. |

Backend: additive custom_issue schema and service-role-only atomic RPC deployed; worker v67, app-api v61, MCP v14. Production tools/list exposes send_custom_issue with write scopes. Unauthenticated MCP and app API sending are rejected. 123 Deno and 75 Node tests passed. Provider acceptance is explicitly distinguished from Amazon ingestion.

Dependencies: existing authenticated Long Form connection with reader:read/reader:write; configured Kindle recipient. The skill uses existing Long Form pipelines rather than Gmail or handwritten EPUB.

Canonical backend source: https://github.com/phinneywood/long-form (custom-issue changes prepared on a feature branch; default-branch publication awaits explicit approval after automatic review rejection). This source mirror also awaits review before merging.

Use: ask to use long-form-kindle to send supplied content or original URLs to Kindle. A preparation-only request does not authorize sending.
