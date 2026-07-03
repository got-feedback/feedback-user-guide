# FAQ

Use this page for quick answers to the questions new users are most likely to ask.

## What is FeedBack?

FeedBack is an interactive music practice app. It loads playable song files, shows arrangements such as guitar or bass parts, and can use plugins for tuning, note detection, tab, fretboard, lyrics, stems, playlists, and more.

See [What FeedBack Is](what-feedback-is.md).

## What is a feedpak?

A feedpak is a FeedBack song package. It can contain metadata, playable arrangements, audio, stems, lyrics, timing data, cover art, and related files.

If you just want to play, think of a feedpak as a FeedBack song file.

See [What Is a feedpak?](../feedpak/index.md).

## Where do I put songs?

Use the import or songs-folder workflow available in your build. Desktop users may be able to place song files in a songs folder and scan. Hosted or browser-based setups may need an upload/import path because the browser cannot directly see the server's folders.

See [Import Songs](../songs/import.md) and [Scan and Rescan](../songs/rescan.md).

## Where do I get songs?

Use songs you have the right to use. You can import compatible song files, create your own feedpak files, or use authoring/import plugins where available. Do not share copyrighted audio or charts unless you have the right to do so.

See [Getting Songs](getting-songs.md).

## Why can FeedBack not hear my instrument?

Most no-signal problems are one of these:

- Wrong input device.
- Wrong input channel.
- Interface gain is down.
- OS microphone/input permission is blocked.
- Virtual device is selected but no audio is routed into it.
- FeedBack is hearing the laptop mic instead of your instrument input.

Start with [No Signal](../troubleshooting/no-signal.md), then [Audio Input Problems](../troubleshooting/audio-input.md).

## Why is my score wrong?

Treat a very wrong score as a setup problem first. Check:

- Tuning.
- Selected arrangement.
- Audio input.
- Calibration.
- Room noise or backing bleed.
- Driver or latency changes.

See [Scoring and Mastery](../play/scoring.md).

## Why does the tuner open before a song?

The tuner may open or prompt when FeedBack detects that the selected arrangement uses a tuning different from your current setup. You can tune, close it, or change tuner/plugin settings if auto-open behavior is available in your build.

See [Tuner](../tuning/tuner.md) and [Extended-Range Instruments](../tuning/extended-range.md).

## Why do I see the same audio interface more than once?

On Windows, one physical interface can appear through more than one driver path, such as ASIO and Windows Audio/WASAPI. Pick the device entry that matches the driver path you want to use.

See [ASIO, WASAPI, and CoreAudio](../desktop-audio/driver-types.md).

## Why is a plugin missing?

The plugin may not be installed, enabled, supported for the selected arrangement, or available in your build. Restart after installing or updating plugins.

See [Plugin Problems](../troubleshooting/plugins.md) and [Plugin Directory](../plugins/directory.md).

## Why is a song missing from my library?

Common causes:

- The file is not in the expected folder.
- The library has not scanned yet.
- The file format is not supported.
- The song package is invalid.
- Metadata changed but a full rescan has not run.

See [Library Problems](../troubleshooting/library.md).

## Why is first launch slow?

First launch can take longer while FeedBack prepares resources, caches, or models. Later launches should be faster. If the app never opens, use the desktop install troubleshooting page.

See [First Launch](../install/first-launch.md) and [Desktop Install Problems](../troubleshooting/desktop-install.md).

## Should I use a microphone or an audio interface?

A microphone is easy to start with but can pick up room noise and backing audio. A USB instrument cable or audio interface usually gives a cleaner signal for tuning and scoring.

See [System Requirements](system-requirements.md) and [Audio Devices](../tuning/audio-devices.md).

## What should I include when reporting a bug?

Include:

- FeedBack build.
- Platform.
- Device/input.
- What you expected.
- What happened.
- Steps to reproduce.
- Screenshots or video if visual.
- Diagnostics bundle.

See [Reporting an Issue](../troubleshooting/report-issue.md).

