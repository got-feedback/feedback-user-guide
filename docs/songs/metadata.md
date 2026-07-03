# Song Metadata

Short answer: song metadata controls how songs appear in your library, including title, artist, album, year, genre, and related grouping information.

## Where Metadata Comes From

| Source | What It Means |
|---|---|
| Song file | Authored data included in the feedpak. |
| Local database | User edits, favorites, tags, and local organization. |
| Enrichment | Optional matched data from external sources when supported. |

## Metadata Fields Users May See

| Field | What It Means |
|---|---|
| Title | Song title shown in the library. |
| Artist | Recording or performing artist. |
| Album | Album/release name when known. |
| Album artist | Grouping artist for albums or compilations where supported. |
| Year | Release or authored year when available. |
| Genre | One or more genre tags where supported. |
| Track/disc | Album ordering information where supported. |
| Tuning | Arrangement tuning. |
| Arrangements | Playable parts included in the chart. |

## FeedBack vs Local Edits

The song file carries authored metadata. FeedBack may also keep local user metadata such as favorites, tags, notes, or preferred versions. Local metadata helps organize your own library and does not necessarily travel with the song file.

## Common Tasks

- Correct a title or artist.
- Understand why two versions of a song appear.
- Group songs by album.
- Filter by genre or practice state.

## Multiple Versions of a Song

If you have several authored versions of the same recording, FeedBack may show them as separate charts or group them depending on your build and settings. A future grouped view should make the preferred chart clear and let you open alternate versions.

## Design Handoff Notes

The final page should show provenance labels such as "from song file", "your edit", or "matched" if those appear in the UI.

## Related Pages

- [What Is a feedpak?](../feedpak/index.md)
- [Library Views](library.md)
