# ChatGPT plugins

Source for Antonio's personal ChatGPT skills and their cloud plugin releases.

This is a collection of separate plugins, not one combined plugin. Assistant Harness contains only `assistant-harness`, `portfolio-pm`, `knowledge-reconcile`, and `harness-audit`. Long Form, Writers Packet, and Pocock Handoff have independent packages; installing Assistant Harness does not install them.

## What lives here

- `skills/<name>/`: reviewed skill instructions and resources. `pocock-handoff` is the source for the installed cloud plugin; `chatgpt-plugin-factory` is the release workflow used in Work.
- `plugins/<name>/plugin.json`: versioned manifest for each cloud plugin.
- `scripts/build_plugin.py`: assemble a ZIP with skills and optional registered app mappings from the selected skill folders.
- `releases/`: evidence of source, upload, installation, and fresh host loading. A ZIP in `dist/` is a build artifact, not an installed plugin.

## Skill inventory

| Skill | Source | Ordinary Chat status |
| --- | --- | --- |
| Assistant Harness core | [Package and setup](docs/assistant-harness.md) | Four shared skills plus private configuration and pinned schedule prompts. Personal Work installation and cloud/native behavior gates are recorded separately in [release evidence](releases/assistant-harness-1.0.0.md). |
| `long-form-kindle` | [`skills/long-form-kindle/`](skills/long-form-kindle/) | Cloud 1.0.0 installed and native reading verified in ordinary Chat. Revised Work skill preserves structured documents. Combined 1.1.0 package prepared; upload and duplicate cleanup await explicit approval. See [release evidence](releases/long-form-kindle-1.1.0.md). |
| `writers-packet` | [`skills/writers-packet/`](skills/writers-packet/) | Cloud 1.0.0 installed; native loading and explicit behavior verified in fresh web Chat. Automatic use failed; iOS unverified. See [release evidence](releases/writers-packet-1.0.0.md). |
| `pocock-handoff` | [`skills/pocock-handoff/`](skills/pocock-handoff/) | Cloud plugin 1.0.1 read in fresh web Chat. |
| `distill` | [`skills/distill/`](skills/distill/) | Source and personal skill preserved; cloud plugin and fresh ordinary Chat reading are unverified. |
| `investigate-prior-art` | [`skills/investigate-prior-art/`](skills/investigate-prior-art/) | Source and personal skill preserved; depends on `strategy-factory`; cloud plugin and fresh ordinary Chat reading are unverified. |
| `chatgpt-plugin-factory` | [`skills/chatgpt-plugin-factory/`](skills/chatgpt-plugin-factory/) | Installed as a personal Work skill; ordinary Chat use is unverified. |
| Strategy Factory stages | [Strategy Factory repository](https://github.com/phinneywood/strategy-factory/tree/main/skills) | Keep source in that project; ordinary Chat loading remains to be tested. |

## Add or update a skill

1. Use ChatGPT Work's `skill-creator` and `chatgpt-plugin-factory` to create or revise the personal skill and validate it in the managed checkout. Review its files, then copy the approved source into `skills/<name>/` here. Commit the source. This GitHub repository is the durable review and release history; the managed personal-skill copy is an installation that must be kept in sync. Host-specific `agents/openai.yaml` metadata may differ between personal and cloud installations; compare the actual `SKILL.md` bytes for the release.
2. Put essential instructions in `SKILL.md`. Ordinary Chat read `SKILL.md` in the `pocock-handoff` control test but did not expose its bundled `HOST.md` through the native reader.
3. Add or increment `plugins/<plugin-name>/plugin.json`. Build the archive:

   ```bash
   python3 scripts/build_plugin.py pocock-handoff
   ```

   For a related set of skills sharing one release, pass their names: `python3 scripts/build_plugin.py my-plugin --skills first-skill second-skill`. Inspect the ZIP and validate the actual candidate before upload.
4. Upload the ZIP in ChatGPT **Plugins → Personal → Add → Upload plugin archive**, then install it. For an existing cloud plugin use **More actions → Upload new version**. Updating GitHub or the personal-skills checkout alone does not update the cloud plugin.
5. Open a fresh ordinary Chat without copied instructions. Ask it to discover the installed skill and read `SKILL.md` through its native reader; require a distinctive instruction from that installed version. Verify behavior separately. Test iOS separately before claiming support. Record each gate in `releases/`.

The current control release is [`pocock-handoff` 1.0.1](releases/pocock-handoff-1.0.1.md). See [`chatgpt-plugin-factory`](skills/chatgpt-plugin-factory/SKILL.md) for the full checklist and boundaries. The upstream Pocock handoff license is retained in its skill folder.

## Public sharing and licensing

Original code and documentation are available under the [MIT license](LICENSE). Retain the upstream copyright and license in `skills/pocock-handoff/LICENSE` when redistributing that skill, and preserve source attribution elsewhere. This license does not grant access to connected accounts or private deployment records.

Keep account configuration, schedule backups, installed identities, and verification-chat links privately. Public release records retain generic test evidence. Registered service app mappings and public service endpoints are intentional integration metadata; each user must establish their own authorized service connection. See [the repository hygiene procedure](docs/repository-hygiene.md) for a reusable scheduled audit.
