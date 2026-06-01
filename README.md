# OpenWebcam for Windows — downloads

Official download home for the **OpenWebcam desktop client**: the small Windows app that
receives video from the OpenWebcam Android app and turns your phone into a PC webcam.

- 🌐 Website: **https://openwebcam.site**
- 📥 Download: the [**Releases**](https://github.com/TonmoyBishwas/openwebcam-desktop-src/releases) page on this repo
- 🔒 Privacy: **https://openwebcam.site/privacy** — your video stays on your local network; nothing is uploaded

> This repository hosts the **public release installers** for the Windows client. It's free,
> ad-free, and has no account or paywall.

## What it does

OpenWebcam streams your Android phone's camera to your PC over **USB or Wi-Fi**. The phone runs
the OpenWebcam app (the camera end); this desktop client is the receiving end on your PC. It:

- creates an **OpenWebcam virtual camera** that shows up in Zoom, Meet, Teams, Discord, and OBS, and
- re-serves the stream as **MJPEG on localhost** so OpenCV can read it directly.

## Install (Windows 10 / 11, 64-bit)

1. Download the latest installer from the [**Releases**](https://github.com/TonmoyBishwas/openwebcam-desktop-src/releases) page.
2. Run it (Inno Setup installer, ~25 MB).
3. Open OpenWebcam on your phone and this desktop client on your PC, then connect over USB or Wi-Fi.
4. In your call or capture app, pick **OpenWebcam** from the camera list.

### Reading frames in code

The client re-serves the stream as MJPEG on localhost, so any OpenCV pipeline can read it in one line:

```python
import cv2
cap = cv2.VideoCapture("http://127.0.0.1:8090/video")
```

## Questions

Email **mevaser909@gmail.com**.

## License

[MIT](LICENSE).
