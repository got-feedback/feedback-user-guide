# Stem Splitter

Short answer: the Stem Splitter plugin creates separated audio parts (vocals, drums, bass, guitar, and more) from a song's full mix, and can transcribe or re-time its lyrics — all from inside FeedBack, without a terminal.

The [Stems and Stem Mixer](stems.md) plugin plays and balances stems. Stem Splitter is the one that *makes* them.

## When To Use This

- A song only has a full mix, and you want isolated parts to practice against.
- You want to mute vocals for karaoke, or solo the drums.
- A song has no lyrics and you want them transcribed from the vocals.
- A song's lyrics are correct but their timing drifts, and you want them re-aligned.

## Before You Start

Splitting and transcribing are heavy audio jobs. They can run three ways, and the plugin picks whichever you've set up:

- **On this machine** — download a local engine once, then everything runs offline. A GPU is faster, but a CPU works.
- **On a server** — point the plugin at a Demucs/WhisperX server (yours or a shared one). See [Demucs Server](../advanced/demucs-server.md).
- **The built-in managed server** — the plugin can install and run a local server for you (**Settings → Stem Splitter → Install server + models**). This is the easiest path and needs no command line.

The first job of each kind downloads its models — up to a couple of gigabytes, once. Nothing large is ever downloaded until you ask for it: the plugin warns and waits for your confirmation before any big download.

## Steps

### Split a song into stems

1. In your library, open the menu on a song's card.
2. Choose **Split stems**. (It's greyed out on songs that are already fully split.)
3. If models aren't downloaded yet, the plugin tells you the size and asks first. Approve it.
4. Watch progress in the **queue** — click the "Split queued" toast, or open **Settings → Stem Splitter → Open the queue**.
5. When it finishes, open the [Stem Mixer](stems.md) to hear the parts.

The original full mix is always kept in the song, so a split never throws audio away.

### Transcribe lyrics

1. Open a song's card menu.
2. Choose **Transcribe lyrics**. (Enabled only when the song has no lyrics yet.)
3. Approve the model download if prompted, then watch the queue.

Transcription listens to the vocals and writes the words *and* their timing. An instrumental produces no lyrics — that's a normal result, not an error.

### Re-align existing lyrics

Use this when the words are right but the timing is off — lyrics pasted from the web, imported from a Guitar Pro file, or transcribed against a different mix.

1. Open a song's card menu.
2. Choose **Re-align lyrics to vocals**. (Enabled only when the song has both lyrics and a vocal stem.)

Re-align keeps your words exactly as they are and only fixes their timing. It never replaces a word — if you want the words themselves redone, use **Transcribe lyrics** instead. Re-align needs a server (the built-in managed one is fine); the local engine can transcribe but can't re-align.

## What You Should See

- Card-menu actions: **Split stems**, **Transcribe lyrics**, **Re-align lyrics to vocals**, each enabled only when it applies to that song.
- A **queue** you can reach from the toast or from the plugin's Settings page, showing each job's progress and a badge with the number running.
- A failed job shows its full error, with a **Copy** button for pasting into a bug report.

Screenshot placeholders:

- `SCREENSHOT: song card menu showing the three Stem Splitter actions`
- `SCREENSHOT: Stem Splitter settings — engine choice, managed server card, Open the queue button`
- `SCREENSHOT: the queue with a split and a transcription running`

## Managing the Built-In Server

Everything below lives in **Settings → Stem Splitter**, and needs no terminal.

| Button | What it does |
|---|---|
| Install server + models | Sets up the managed local server and downloads its models. |
| Start / Stop | Runs or stops the local server. Auto-start is on by default once installed. |
| Test status | Checks the server is up and reports its device (CPU/GPU) and warmup state. |
| Prepare models | Downloads the model weights on their own, ahead of your first job. |
| Check for update | Refreshes the server to pick up fixes, without re-downloading models. |

The status chips distinguish **loading** (reading a model you already have from disk) from **downloading** (fetching over the network), so a quick warm-up isn't mistaken for a fresh multi-gigabyte pull.

### Running FeedBack in Docker

If you run the FeedBack app itself in a container, the plugin can't install a server on your host. Instead it offers a **compose snippet** to run the server as a companion container (always shown, recommended), and — only when the Docker socket is already available to the app — a one-click option. GPU is requested only when your Docker setup actually advertises one.

## Common Problems

| Problem | Try This |
|---|---|
| The action is greyed out | Split needs an un-split song; Transcribe needs a song with no lyrics; Re-align needs both lyrics and a vocal stem. |
| "Re-align needs a server" | Re-align can't run on the local engine. Configure a server, or use the built-in managed one. |
| A job seems stuck at the start | It may be downloading models. Check the queue and the Settings page for download progress. |
| Models re-download every launch | Update the server with **Check for update** — an older server had a bug that deleted weights. |
| Transcription returns nothing | The vocal stem may be silent (an instrumental) or in a different language than expected. |
| A job failed | Open the queue, read the full error, and use **Copy** if you need to report it. |
| The whole batch failed at once | Often a server that's unreachable or missing its models. Check **Test status**. |

## Related Pages

- [Stems and Stem Mixer](stems.md)
- [Lyrics](lyrics.md)
- [Demucs Server](../advanced/demucs-server.md)
- [What Is a feedpak?](../feedpak/index.md)

## Applies To

Version: Stem Splitter 0.4.x
Platforms: Windows, macOS, Linux (managed server and local engine); any host for a remote/Docker server
