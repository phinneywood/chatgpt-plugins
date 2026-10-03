# Assistant Harness 1.0.0

Date: October 3, 2026. Target: personal Work deployment first; ordinary Chat and iOS through a separate cloud plugin release. Reusable skills: assistant-harness, portfolio-pm, knowledge-reconcile, harness-audit. Existing service plugins supply tools; no new MCP server/account connection is bundled.

## Evidence gates

| Gate | Status | Evidence and limit |
| --- | --- | --- |
| Source and package | Validated | Four self-contained SKILL.md files; root portable manifest; archive contains manifest plus skill files only. |
| Host skill validation | Passed | Built-in quick_validate.py ran on each actual personal installation candidate. |
| Portable convention checks | Passed | Plugin-factory checker ran on the extracted actual archive; zero errors. This is not full Agent Plugins schema or security certification. |
| Config and renderer checks | Passed | Nine unittest cases: permission type confusion, protected actions, personal-account boundary, unpinned sources, timezone/version, secret/credential URLs, duplicate task IDs, escaping paths, wrong private repository, event-task shortcut and read-only CLI. |
| Independent portfolio workflow | Passed, fixture only | Minimal-context agent used the portfolio skill: proposed dates did not authorize booking; email instructions did not override rules; no sending; event completion waited for write/readback; missing ready-list configuration was not guessed. |
| Independent knowledge workflow | Passed, fixture only | Minimal-context agent used the knowledge skill: 409 plus failed reread left update/watermark pending; timezone correctly kept date October 3; already-claimed interrupted sweep was skipped; shared/personal file excluded. |
| Personal Work persistence | Pending | Installation verification will be recorded after saving and native reading. |
| Pinned source loading | Pending | Current config/policy and pinned shared source must be read through intended connected tools before migration. |
| Saved task behavior | Pending | Prompt readback alone does not prove independent execution. |
| Cloud plugin installation | Unverified | Upload/install is separate from GitHub or personal skill installation. |
| Fresh ordinary Chat / iOS | Unverified | Require native reader result and actual behavior in each surface. |
| Automatic activation | Unverified | Explicit loading is the supported release route; universal rules stay in standing instructions. |

## Forward-test outputs

Portfolio fixture: the agent proposed a project next-action update, preserved the thread/message identifiers without inventing URLs, made no calendar/message operation, declined to guess the unconfigured ready list, and kept the processed-message checkpoint unchanged until verified effects. The claimed quote attachment was not treated as received without evidence.

Knowledge fixture: the agent retained the original reviewed-through value, required a successful current-SHA reread before retrying, and reported both actual failures. It correctly converted 00:30 UTC October 4 to 17:30 Pacific October 3 and skipped that date's already-claimed sweep without marking it completed. These are isolated prepare-only behavior checks, not live connector or scheduling tests.

## Dependencies and rollback

Each user supplies a private config locator, authorized current policies, existing GitHub/Trello/Google Drive tools and an assistant-managed Calendar where used. Runtime may fetch pinned source through GitHub when native skill loading is unavailable. A required read failure prevents dependent writes.

Private task/config/rollback records remain outside this public package. Existing enabled jobs are refactored in place only after source loading; schedules/enabled state/runtime remain fixed. Event tasks remain unchanged if their complete filters cannot be read. Disabled jobs are not reactivated. Specialty reading/brief/cleanup/watch recipes are not included in this core release.

User invocation: select Assistant Harness or request the relevant skill with your private config_locator. Source edits do not automatically upgrade cloud plugins or pinned tasks. Public Directory publication is not part of this release.
