# Stems and Stem Mixer

Stems are separated audio parts such as vocals, drums, bass, guitar, and other. Stem tools help you listen to, balance, or generate those parts where supported.

## Use It For

- Lowering or muting a part while practicing.
- Isolating vocals, drums, bass, or guitar.
- Preparing lyric or karaoke workflows.
- Checking whether a song package includes separated audio.

## Basic Workflow

1. Open a song that includes stems.
2. Open the Stems or Stem Mixer plugin.
3. Adjust stem levels.
4. Play the song and confirm the mix sounds correct.

## Full Mix vs. Separated Stems

When a song includes its original full mix — which every song split in-app keeps — the mixer is smart about which audio it plays:

- **Every stem on at 100% → you hear the original full mix.** Not a recombination of the separated parts, the actual untouched audio. This is the best-quality playback, and it's what you get by default.
- **Mute or lower any stem → the mixer switches to the separated stems**, so your change is audible. It stays on the separated mix until every stem is back on at 100%.

The reason for the switch is quality: separation is lossy, so summing the stems back together isn't identical to the original. Playing the real full mix whenever you haven't changed anything means you only pay that small quality cost when you actually want a custom balance.

This works because the feedpak format keeps the original mixdown as a reserved [`full` stem](https://got-feedback.github.io/feedpak-spec/feedpak-v1.html#the-full-stem--the-complete-mixdown): the format strongly recommends retaining it when a song is separated, precisely because separation is lossy and it's the only way to play the song exactly as recorded. Any song split inside FeedBack always keeps it, so this behavior applies automatically.

If a song has no full mix (an older or externally-made pack that dropped it), the mixer simply always plays the separated stems.

## Stem Availability

Not every song includes stems. To create stems from a song that only has a full mix, use the [Stem Splitter](stem-splitter.md) plugin.

## Common Problems

| Problem | Try This |
|---|---|
| No stems appear | The song may only include a full mix. |
| Stem generation is slow | First-time model downloads or CPU/GPU limits may apply. |
| Mix sounds unbalanced | Reset levels and adjust one stem at a time. |

## Related Pages

- [Stem Splitter](stem-splitter.md)
- [What Is a feedpak?](../feedpak/index.md)
- [Desktop Audio](../desktop-audio/index.md)

