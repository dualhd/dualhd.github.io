# Dual HD
Frame size specification for streaming horizontal and vertical video at the same time: [dualhd.org](https://dualhd.org/).

Dual HD places a horizontal video and a vertical video side by side in one frame. The encoder sends a single stream, and a server crops it into two outputs: horizontal for platforms such as Twitch and YouTube, vertical for platforms such as TikTok and Instagram.

## Frame sizes

The horizontal video is at position (0, 0). The vertical video is directly to its right, aligned to the top. Each frame size is named after its frame width.

| Name | Frame (w x h) | Horizontal video | Vertical video | Vertical position (x, y) |
|---|---|---|---|---|
| Dual HD 1760 | 1760x854 | 1280x720 | 480x854 | 1280, 0 |
| Dual HD 2000 | 2000x1280 | 1280x720 | 720x1280 | 1280, 0 |
| Dual HD 2640 | 2640x1280 | 1920x1080 | 720x1280 | 1920, 0 |
| Dual HD 3000 | 3000x1920 | 1920x1080 | 1080x1920 | 1920, 0 |
| Dual HD 3640 | 3640x1920 | 2560x1440 | 1080x1920 | 2560, 0 |
| Dual HD 4920 | 4920x2160 | 3840x2160 | 1080x1920 | 3840, 0 |

Image templates for each size are in [img/](img/).

## Scope

Dual HD defines frame sizes and video positions only. It does not specify codecs, bitrates or other encoding settings. The frame is larger than a single video, so an efficient codec such as HEVC or AV1 is recommended.

A reference server implementation is available at [dualhd/server-demo](https://github.com/dualhd/server-demo).

This project is supported by [Streamrun](https://streamrun.com/), which uses Dual HD to multistream horizontal and vertical video to different platforms at the same time.
