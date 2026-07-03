# Audio Input Problems

Short answer: most audio input problems come from the wrong device, wrong channel, muted gain, missing OS permission, or a fallback to the system default input.

## Symptoms

- Tuner does not move.
- Note Detection does not score.
- FeedBack hears the laptop microphone instead of your interface.
- Calibration does not advance.
- A virtual device appears selected but does not provide signal.

## First Checks

1. Confirm the instrument or mic is plugged in.
2. Confirm the interface has gain and is not muted.
3. Confirm the OS sees the device.
4. Confirm FeedBack selected the same device.
5. Confirm the selected channel is correct.
6. Open the tuner and check for movement.

## Windows Notes

If the same interface appears more than once, check whether entries are labeled by driver type. Pick the driver path you intend to use.

## macOS Notes

If you use BlackHole or another virtual device, confirm both macOS and FeedBack are pointed at the expected device.

## When Reporting

Include:

- Platform.
- FeedBack build.
- Device name.
- Whether the tuner moves.
- Whether normal system audio input sees the device.
- Diagnostics bundle.

## Related Pages

- [Audio Input Setup](../first-run/audio-input.md)
- [Export Diagnostics](../first-run/export-diagnostics.md)

