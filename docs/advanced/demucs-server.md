# Demucs Server

Short answer: the Demucs server is an advanced backend for source separation and lyric-alignment workflows.

## Use It For

- Separating a song into stems.
- Aligning lyrics against vocals.
- Supporting karaoke or vocal workflows.
- Offloading heavy processing to a GPU-capable machine.

## Before You Start

- This is an advanced setup.
- A CUDA-capable GPU is recommended for practical performance.
- FFmpeg and Python are required.
- First-time model downloads can be large.

## Basic Workflow

1. Install the server from its repository.
2. Install Python dependencies.
3. Start the server on the chosen host and port.
4. Configure FeedBack or the relevant plugin to use that server URL.
5. Test health/status before running a long job.

## Common Problems

| Problem | Try This |
|---|---|
| First request is slow | Model weights may be downloading or warming up. |
| Server is unreachable | Check host, port, firewall, and URL. |
| GPU is not used | Check CUDA installation and server device settings. |

## Related Pages

- [Stems and Stem Mixer](../plugins/stems.md)
- [Lyrics](../plugins/lyrics.md)

