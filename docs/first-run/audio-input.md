# Audio Input Setup

Short answer: choose the microphone, cable, or audio interface FeedBack should listen to before calibration and scoring.

## When To Use This

- First launch.
- Note detection does not respond.
- The tuner is listening to the wrong device.
- You changed your audio interface or driver mode.

## Before You Start

- Plug in your interface or microphone before opening FeedBack.
- On Windows, decide whether you want the ASIO or Windows audio path if both appear.
- On macOS, confirm virtual devices such as BlackHole are already installed and visible to the system.

## Steps

1. Open the audio input setup screen.
2. Select the input device you want FeedBack to hear.
3. If channels are shown, choose the channel that carries your instrument.
4. Pluck or play your instrument.
5. Continue only when FeedBack shows that it can hear the input.

## What You Should See

- Device names should be readable.
- Windows devices may include driver labels such as ASIO or Windows Audio.
- The input meter or tuner should react when you play.

Screenshot placeholders:

- `SCREENSHOT: Audio input picker`
- `SCREENSHOT: Input meter reacting to signal`

## Common Problems

| Problem | Try This |
|---|---|
| No signal | Check the device, channel, cable, gain, and OS permissions. |
| Wrong device after setup | Re-select the input and export diagnostics if it repeats. |
| Duplicate-looking devices | Pick the entry with the driver type you intend to use. |
| Virtual device selected but internal mic is heard | Check OS sound input and FeedBack diagnostics. |

## Related Pages

- [Audio Devices](../tuning/audio-devices.md)
- [Audio Input Problems](../troubleshooting/audio-input.md)
- [Export Diagnostics](export-diagnostics.md)

## Applies To

Version: 0.3.0+
Platforms: Windows, macOS, Linux

