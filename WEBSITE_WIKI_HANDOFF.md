# FeedBack Website Wiki Handoff

Purpose: give the website/design team a practical blueprint for integrating the FeedBack user guide into the upcoming public website.

Source repo: https://github.com/got-feedback/feedback-user-guide  
Current rendered preview: https://got-feedback.github.io/feedback-user-guide/  
Docs source: `docs/`  
Site config: `mkdocs.yml`

## Handoff Summary

The user guide is already organized as a portable Markdown wiki. It can be used in three ways:

1. Imported into the upcoming website as content source.
2. Kept as a standalone MkDocs-powered docs/wiki site.
3. Browsed directly from GitHub while the website integration is in progress.

The website team should treat the current docs as content scaffolding: the information architecture, article inventory, support flows, and page copy exist; final visual design, screenshots, UI callouts, and release-accurate wording still need review against the 0.3.0 build.

## Integration Goals

- Give new users a clear path from install to first playable song.
- Reduce support load for audio input, tuning, calibration, import, and playback issues.
- Give plugins a searchable directory.
- Keep advanced topics available without overwhelming first-run users.
- Preserve stable URLs for Discord, GitHub Releases, app help links, and support responses.
- Make the docs easy for maintainers to edit after launch.

## Recommended Website IA

Use these top-level groups in the website docs/wiki navigation:

1. Getting Started
2. Installing FeedBack
3. First-Time Setup
4. Songs and Library
5. Playing and Practicing
6. Tuning, Input, and Calibration
7. Plugins
8. Desktop Audio
9. Song Files and feedpak
10. Troubleshooting
11. Advanced Users
12. Releases and Updates
13. FAQ / Glossary / A-Z

The current MkDocs navigation in `mkdocs.yml` already implements this structure.

## Priority Launch Pages

These should be polished before launch because they will absorb most user support traffic:

| Priority | Page | Source |
|---|---|---|
| P0 | Quick Start | `docs/quick-start.md` |
| P0 | FAQ | `docs/getting-started/faq.md` |
| P0 | System Requirements | `docs/getting-started/system-requirements.md` |
| P0 | Install FeedBack Desktop | `docs/install/index.md` |
| P0 | First Launch | `docs/install/first-launch.md` |
| P0 | Audio Input Setup | `docs/first-run/audio-input.md` |
| P0 | Calibration | `docs/first-run/calibration.md` |
| P0 | Import Songs | `docs/songs/import.md` |
| P0 | Scan and Rescan | `docs/songs/rescan.md` |
| P0 | Play a Song | `docs/play/play-a-song.md` |
| P0 | Tuner | `docs/tuning/tuner.md` |
| P0 | No Signal | `docs/troubleshooting/no-signal.md` |
| P0 | Audio Input Problems | `docs/troubleshooting/audio-input.md` |
| P0 | No Sound or Output | `docs/troubleshooting/no-sound-output.md` |
| P0 | Reporting an Issue | `docs/troubleshooting/report-issue.md` |

## Secondary Pages

Polish these after the launch-critical pages:

- `docs/play/scoring.md`
- `docs/play/player-controls.md`
- `docs/play/speed-looping-sections.md`
- `docs/songs/library.md`
- `docs/songs/playlists.md`
- `docs/songs/metadata.md`
- `docs/plugins/directory.md`
- `docs/feedpak/index.md`
- `docs/releases/0-3-0.md`
- `docs/releases/known-limitations.md`
- `docs/reference/a-z.md`

## URL Recommendations

Use short, stable, human-readable URLs. Current MkDocs output already maps cleanly:

| Content | Recommended URL |
|---|---|
| Quick Start | `/quick-start/` |
| FAQ | `/getting-started/faq/` |
| Glossary | `/getting-started/common-terms/` or `/glossary/` |
| Install | `/install/` |
| Audio Input Setup | `/first-run/audio-input/` |
| Import Songs | `/songs/import/` |
| Tuner | `/tuning/tuner/` |
| No Signal | `/troubleshooting/no-signal/` |
| Report Issue | `/troubleshooting/report-issue/` |
| Plugin Directory | `/plugins/directory/` |
| feedpak | `/feedpak/` |

If the website platform changes URL paths, set redirects from the MkDocs paths so existing GitHub Pages, Discord, and release links do not break.

## Website Entry Points

The website should expose these doc entry points:

- Header nav item: `Docs` or `Guide`
- Footer link: `User Guide`
- Product pages: contextual links to install, quick start, plugins, and feedpak
- Download page: links to install, first launch, audio input, and troubleshooting
- Release notes: links to 0.3.0 notes, known limitations, reporting issues
- In-app help links later: deep links into setup, tuner, diagnostics, and troubleshooting

## Suggested Homepage Blocks

If the website has a docs landing page, use functional blocks:

1. Search bar.
2. Start here: Quick Start, Install, Audio Input Setup, Import Songs.
3. Common fixes: No Signal, Audio Input Problems, No Sound, Calibration, Reporting an Issue.
4. Browse by area: Songs, Practice, Plugins, Desktop Audio, feedpak.
5. 0.3.0 launch notes.
6. FAQ, Glossary, A-Z.

Avoid making the docs homepage a marketing hero. Users landing there usually need an answer.

## Design Components Needed

| Component | Use |
|---|---|
| Search | Primary docs navigation. |
| Platform badges | Windows, macOS, Linux, Web, Desktop-only. |
| Version badges | 0.3.0+, planned, desktop-only. |
| Screenshot block | Image + caption + alt text. |
| Callout / annotation | Point to controls in screenshots. |
| Warning box | Permissions, volume, routing loops, data loss. |
| Troubleshooting table | Symptom -> action. |
| Related links block | Bottom of every article. |
| Plugin card | Plugin directory. |
| Support shortcut panel | Troubleshooting pages. |

## Screenshot Plan

Capture screenshots after the 0.3.0 UI is frozen.

First screenshot pass:

1. Songs screen with at least one song.
2. Audio input picker.
3. Input signal/meter or tuner responding.
4. Import/Add Songs action.
5. Scan/rescan action.
6. Player view.
7. Arrangement picker.
8. Tuner current-song mode.
9. Playlist/detail view.
10. Diagnostics export.
11. Settings overview.
12. Plugin directory/plugin manager.

Screenshot rules:

- Use a clean test library.
- Avoid private file paths and personal device names where possible.
- Avoid copyrighted album art unless cleared.
- Capture final UI labels exactly as shipped.
- Add descriptive alt text.
- Keep images readable at mobile width.

## Content Review Checklist

Before launch:

- Replace planning language in `docs/releases/0-3-0.md` with final shipped features.
- Verify all UI labels against the final build.
- Verify platform package names and download paths.
- Verify plugin availability and status labels.
- Verify tuner auto-open wording against final behavior.
- Verify library/metadata pages against what actually ships in 0.3.0.
- Verify troubleshooting pages link to diagnostics.
- Confirm legal wording on `Getting Songs`.
- Confirm whether legacy/internal names should appear anywhere.

## In-App Link Recommendations

Future app integration should use stable deep links:

| App Location | Link Target |
|---|---|
| First-run audio setup | Audio Input Setup |
| No input detected | No Signal |
| Calibration wizard | Calibration / Calibration Problems |
| Tuner panel | Tuner |
| Song import | Import Songs |
| Scan/rescan UI | Scan and Rescan |
| Plugin manager | Plugin Directory / Plugin Problems |
| Diagnostics export | Export Diagnostics / Reporting an Issue |
| Failed playback | Playback Problems |

## Content Ownership

Recommended owners:

- Product/design: IA, homepage, screenshots, visual components.
- Engineering: UI label accuracy, platform notes, release-accurate behavior.
- Support/community: FAQ, troubleshooting, known limitations.
- Plugin maintainers: plugin-specific pages.
- Spec maintainers: feedpak pages.

## Website Build Options

### Option A: Import Markdown Into Website

Use `docs/` as source content. Preserve relative links or rewrite them during import. Recommended if the upcoming website has its own docs system.

### Option B: Embed/Theme MkDocs

Keep this repo as a docs build and theme it to match the website. Recommended if website integration needs to be quick and low-risk.

### Option C: Keep GitHub Pages As A Temporary Wiki

Use https://got-feedback.github.io/feedback-user-guide/ as the temporary wiki while the website team builds the integrated version.

## Current Known Gaps

The content is structurally complete enough for design handoff, but not final:

- Needs screenshots.
- Needs final 0.3.0 release wording.
- Needs UI label audit.
- Needs final plugin status audit.
- Needs owner review of README/root GitHub landing page changes.
- Needs redirect plan if the website changes paths.

## Handoff Deliverables Already In Repo

- Markdown source articles in `docs/`.
- MkDocs nav in `mkdocs.yml`.
- FAQ and glossary.
- A-Z reference.
- Design support docs:
  - `docs/contributing/design-handoff.md`
  - `docs/contributing/style-guide.md`
  - `docs/contributing/page-template.md`

## Recommended Next Step

Design should start with a docs landing page and the P0 article template. Engineering should do a UI-label pass against the final 0.3.0 build before screenshots are captured.

