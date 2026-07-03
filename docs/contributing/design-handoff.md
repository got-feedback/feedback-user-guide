# Design Handoff

This page tracks what design needs to turn the documentation bones into a polished public wiki.

## Goals

- Make first-run help feel trustworthy and easy to scan.
- Keep task pages practical, not promotional.
- Make troubleshooting pages easy to use during a real setup failure.
- Give plugins a consistent directory/card treatment.
- Add screenshots only after the UI for the relevant release is stable.

## Page Types

| Type | Design Need |
|---|---|
| Home page | Search-first layout, common tasks, start-here cards. |
| Task page | Clear steps, expected result, related links. |
| Troubleshooting page | Symptom table, first checks, report details. |
| Plugin page | Compact overview, workflow, settings, troubleshooting. |
| Reference page | Dense, searchable, low decoration. |
| Release page | Short overview, links to full tasks. |

## Screenshot Pass

Capture screenshots for these pages first:

1. [Quick Start](../quick-start.md)
2. [Audio Input Setup](../first-run/audio-input.md)
3. [Import Songs](../songs/import.md)
4. [Scan and Rescan](../songs/rescan.md)
5. [Play a Song](../play/play-a-song.md)
6. [Tuner](../tuning/tuner.md)
7. [Playlists and Queue](../songs/playlists.md)
8. [Library Views](../songs/library.md)
9. [Export Diagnostics](../first-run/export-diagnostics.md)
10. [Plugin Directory](../plugins/directory.md)

## Screenshot Rules

- Use a clean test library with non-sensitive file paths.
- Use the same theme for a full pass unless a page specifically compares themes.
- Avoid screenshots with copyrighted album art unless cleared.
- Crop to the UI area the article discusses.
- Add alt text for every image.
- Keep text readable at mobile width.

## Component Needs

| Component | Used For |
|---|---|
| Platform badges | Windows, macOS, Linux, Web, Desktop-only. |
| Version badges | Behavior that applies to 0.3.0+ or a future release. |
| Screenshot callout | Annotated UI steps. |
| Warning box | Data loss, volume/hearing safety, platform caveats. |
| Troubleshooting table | Symptom to action mapping. |
| Plugin card | Plugin directory. |
| Related links block | Bottom of every task page. |

## Launch Review Checklist

- P0 pages have no empty sections.
- Navigation links resolve.
- Search returns expected results for "audio", "tuner", "import", "feedpak", "calibration", "diagnostics", and "playlist".
- 0.3.0 release page does not promise unshipped features.
- Known limitations are current and short.
- Troubleshooting pages all link to diagnostics/reporting.
- Plugin directory labels match the actual launch build.
- Home page links to the most common support paths.

## Content Freeze Notes

Freeze slugs before sharing public links. It is fine to revise article bodies after launch, but URLs should stay stable once posted in Discord, GitHub Releases, or the app.
