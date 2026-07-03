# Known Limitations

This page lists current user-facing limitations for the 0.3.0 launch.

## Validate Before Publishing

- Some platform-specific audio issues require diagnostics to debug.
- Virtual audio devices can be confusing because the OS and FeedBack may select different inputs.
- Some library metadata depends on what is present in the song file.
- Some advanced routing features are desktop-only or planned.

## Audio Input

FeedBack can only score or tune correctly if it is listening to the intended input. If the selected device and the actual device differ, export diagnostics in the same session after reproducing the issue.

## Library Metadata

Some fields only appear when the song file includes them or when a local metadata feature has filled them in. Missing album, genre, track number, or cover art is not always a bug.

## Platform Differences

Desktop builds can expose native audio and routing features that are not available in browser-hosted setups. Windows, macOS, and Linux may also name or route devices differently.

## Plugin Coverage

Not every plugin supports every arrangement type. A guitar-focused view may not appear for drums, keys, or vocals.

## Maintainer Note

Do not use this page as a bug graveyard. Keep it short, current, and linked to fixes or troubleshooting pages.
