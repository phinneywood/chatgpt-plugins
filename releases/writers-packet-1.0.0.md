# Writer’s Packet 1.0.0 — release candidate

Date: 2026-09-27
Source: `6cb309581b811e5812bac4e62b23c8f8447241b9`
Target: personal Work skill and separate ordinary Chat plugin.

| Gate | Status | Evidence |
| --- | --- | --- |
| Static validation | Passed | Host quick_validate.py on managed candidate; package checker ok=true with no errors. No full-schema or security certification claimed. |
| Personal skill persisted | Passed | Supported save completed; reconciled remote path found with matching SKILL.md SHA-256. |
| Source equality | Passed | SKILL.md SHA-256 `39bd17730479ed99bedf6d0f06ce81bf381dc7c35f58cddf06d6661cd64cb6ac`; candidate ZIP entries inspected and compared byte-for-byte. |
| Cloud archive | Built | `writers-packet-1.0.0.zip`, SHA-256 `ccbdb4af3f013c1ec6dfc17c7cc644a858c409584ba174804dd892814dc44626`. Build with the existing build_plugin.py. |
| ChatGPT customization | Saved and verified | Appended concise authorial boundary; reopened form and confirmed exact original text plus addition. Unrelated customization preserved. |
| Behavioral forward tests | Passed, source-loaded Work agents only | Portfolio, whitepaper, LinkedIn preparation; diagnostic critique; comparison without third version; explicit rewrite; assistant email draft. See test record below. |
| Cloud upload/install | Blocked before upload | Automatic approval review rejected file selection because the current authored user message was only a document URL. Need explicit authorization to upload and install this archive in ChatGPT. No bypass attempted. |
| Fresh ordinary Chat discovery/read | Unverified | Pending cloud installation; do not claim completion. |
| Fresh ordinary Chat behavior | Unverified | Pending installation and native reader evidence. |
| iOS | Unverified | Requires a separate fresh iOS check. |

## Scope

One self-contained skill plus a global customization invariant. No MCP server, executable helper, or new access permission. Attribution to Thomas Ptacek’s [How To Write With An LLM](https://sockpuppet.org/blog/2026/09/17/how-to-write-with-an-llm/) is included in SKILL.md. The pre-writing packet and explicit-drafting exception are identified as adaptations.

## Resume

After explicit upload/install authorization, use ChatGPT Plugins → Personal → Add → Upload plugin archive. Select the validated candidate, add it, then Install plugin. Start fresh ordinary Chat without copied skill content; discover writers-packet and read its installed SKILL.md through native tools. Retain tool evidence and run the seven behavior cases in the handoff. Record exact plugin version, fresh Chat evidence, and limits here. Test iOS separately.

## Forward tests

Two independent agents loaded the source file, with only fictional task context. Neither modified live systems. Actual outputs retained in [writers-packet-1.0.0-forward-tests.md](writers-packet-1.0.0-forward-tests.md). Tests showed preparation rather than publication copy; a factual, bounded rewrite on explicit request; and a short assistant email draft. Source-loaded agent behavior is not proof of installed ordinary Chat behavior.

## Restore

Prior repository source: `8bab66fcbaf6fe812c8c84f61cb5a25c230195c2`. This is a new skill/plugin; no previous cloud version was replaced. Rebuild the pinned source for byte verification. Revert only the added authorial-boundary paragraph if the owner later requests it.

Invocation after release: “Use Writer’s Packet to help me prepare a portfolio case study.”
