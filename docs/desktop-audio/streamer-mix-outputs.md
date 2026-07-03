# Streamer Mix Outputs

Short answer: streamer mix outputs are planned desktop audio features for routing different mixes to local monitoring, OBS, or Discord.

## Use Cases

- Hear game audio locally while your hardware guitar tone stays outside FeedBack.
- Send game audio plus in-app tone to a stream.
- Send game audio plus hardware tone to a stream.

## Core Concepts

| Term | Meaning |
|---|---|
| Local monitor | What the player hears. |
| Stream mix | What OBS, Discord, or another app receives. |
| Dry input | A clean direct instrument signal. |
| Wet tone | A processed tone from hardware or in-app modeling. |
| Bus | A named mix with selected sources and levels. |

## Common Routing Shapes

### Simple Discord Session

The player hears the game locally. Friends hear the game plus the player's instrument tone through the stream or call.

### OBS Stream

The stream receives a selected mix that may differ from what the player monitors. This can help prevent double-monitoring or accidental guitar bleed.

### Hardware Rig

The player hears guitar through their own hardware rig, while FeedBack sends a separate stream mix that includes either a re-amped direct signal or the hardware wet signal.

## Current Status

This page is a launch planning page. The feature is desktop-focused and may depend on platform-specific audio routing. Use it to explain the design direction without promising that every routing option is available in every build.

## Platform Notes

| Platform | Notes |
|---|---|
| Windows | OBS/Discord capture can depend on available endpoints and driver mode. |
| macOS | Virtual audio devices may be needed for some routing. |
| Linux | PipeWire-style routing may make advanced paths easier. |

## Safety Notes

- Start with low output volume.
- Avoid routing call audio back into the same call input.
- Use headphones when testing voice-chat or stream-monitoring paths.
- Confirm "what you hear" and "what stream hears" separately.

## Design Handoff Notes

The final page should include:

- OBS setup path.
- Discord setup path.
- "What you hear" vs "what stream hears" explanation.
- Platform limitations.
- Safety notes for feedback/monitor loops.
