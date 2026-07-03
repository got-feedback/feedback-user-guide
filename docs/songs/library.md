# Library Views

Short answer: the library is where you browse, filter, sort, and open songs.

## Library Basics

- Song cards represent playable songs or charts.
- Sorting and filters help narrow the library.
- Some filter and sort choices may be remembered by the app.
- Album and grouped-chart behavior may change as the 0.3.0 library work lands.

## Common Tasks

- Search or browse for a song.
- Sort by artist, title, or practice state.
- Filter by available facets.
- Open a song card to play.
- Use card actions for playlists, metadata, or related tools.

## Library Surfaces

| Surface | Purpose |
|---|---|
| Song grid | Main browse/play surface. |
| Search | Find a song, artist, or album quickly. |
| Sort menu | Change ordering. |
| Filters | Narrow by facets such as artist, album, genre, tuning, or practice state where supported. |
| Card actions | Add to playlist, inspect metadata, favorite, or open related actions. |

## Filters and Sorting

Filters should always be visible when active. If the app remembers a filter or sort from a previous session, the UI should make that state obvious so the library does not look accidentally empty.

## Albums and Multiple Charts

Some songs may have more than one chart or authored version. 0.3.0 library work may group related charts or expose album views. When the UI groups versions, the user's play action should still be clear: which chart and arrangement will open.

## Design Notes

Screenshot placeholders:

- `SCREENSHOT: Library card grid`
- `SCREENSHOT: Filter drawer`
- `SCREENSHOT: Sort menu`

## Related Pages

- [Import Songs](import.md)
- [Playlists and Queue](playlists.md)
- [Song Metadata](metadata.md)
