# ASIO, WASAPI, and CoreAudio

Short answer: driver types are the operating-system audio paths FeedBack can use to reach your input or output device.

## Why This Matters

The same physical audio interface can appear more than once if the operating system exposes it through different driver paths. Choosing the wrong path can cause higher latency, missing channels, or the wrong device being opened.

## Driver Types

| Driver Type | Platform | Notes |
|---|---|---|
| ASIO | Windows | Often preferred for low-latency audio interfaces. |
| WASAPI / Windows Audio | Windows | Built-in Windows audio path; useful for many devices. |
| CoreAudio | macOS | Standard macOS audio system. |
| PipeWire / PulseAudio / JACK | Linux | Availability depends on distribution and setup. |

## Choosing an Input

1. Pick the device name that matches your hardware.
2. If Windows shows driver labels, pick the driver path you intend to use.
3. Pick the correct channel.
4. Confirm signal in the tuner or input meter.

## Common Problems

| Problem | Try This |
|---|---|
| Same interface appears twice | Pick by driver label, not only device name. |
| Channel is missing | Try another driver path for the same interface. |
| Latency is high | Try the low-latency driver path for your interface. |

## Related Pages

- [Audio Input Setup](../first-run/audio-input.md)
- [Audio Input Problems](../troubleshooting/audio-input.md)

