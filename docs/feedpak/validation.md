# Validating feedpak Files

Short answer: validation checks whether a feedpak follows the expected file structure and schemas.

## When To Validate

- After hand-editing a feedpak.
- Before sharing a feedpak.
- When FeedBack refuses to load a song file.
- When metadata or arrangements look malformed.

## What Validation Checks

- Manifest structure.
- Referenced files exist.
- Paths are safe and valid.
- Arrangement data follows the schema.
- Side files such as lyrics, timeline, stems, or harmony match expected shapes.

## Basic Workflow

1. Back up the feedpak.
2. Install the validator dependencies from the feedpak spec repo.
3. Run the validator against the feedpak directory or archive.
4. Fix reported errors.
5. Validate again.

## Related Links

- feedpak spec site: https://got-feedback.github.io/feedpak-spec/
- feedpak repository: https://github.com/got-feedback/feedpak-spec
- [Authoring and Editing](authoring.md)

