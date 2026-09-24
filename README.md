# chromium based browsers AMD D3D11 Blur Fix for videos

WORKS ON: YOUTUBE, NETFLIX, TWITCH and more

Tiny Chrome extension that removes the `backdrop-filter: blur()` applied to video element. Workaround for blurry video playback on Chrome's D3D11 backend with some AMD drivers — D3D9 renders fine, D3D11 looks soft until the blur filter is neutralized.

## Install (unpacked)

1. Clone or download this repo.
2. Open `chrome://extensions`.
3. Enable **Developer mode**.
4. Click **Load unpacked** and select this folder.
5. Reload any open tabs with videos.

## What it does

Injects one CSS rule globally on every site that uses video via D3D11:

```css
video {
  backdrop-filter: blur(0px) !important;
}
```

That's the whole extension. No JS, no permissions beyond the matched hosts.

BEFORE:
<img width="2560" height="1920" alt="image" src="https://github.com/user-attachments/assets/22b471b3-5143-49a7-9e54-3f1d44357368" />
AFTER:
<img width="2560" height="1920" alt="image" src="https://github.com/user-attachments/assets/efb8a333-8ad2-4941-9085-870208377be4" />



## Credit

Fix surfaced by Reddit users debugging blurry YouTube playback on AMD GPUs under Chrome's D3D11 renderer.
