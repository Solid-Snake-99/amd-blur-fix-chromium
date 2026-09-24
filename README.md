# chromium based browsers AMD D3D11 Blur Fix for videos

WORKS ON: YOUTUBE, NETFLIX, TWITCH and more

Tiny Chrome extension that removes the `backdrop-filter: blur()` applied to video element, A VERY annoying bug for AMD video cards and amd integrated graphics. This workaround is for blurry video playback on Chrome's D3D11 backend with some AMD drivers — D3D9 renders fine, D3D11 looks soft until the blur filter is neutralized.

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
<img width="4000" height="3000" alt="20260924_183215" src="https://github.com/user-attachments/assets/ebc95db5-1ecf-4863-a01f-bab6659a5eb5" />

AFTER:
<img width="4000" height="3000" alt="20260924_183220" src="https://github.com/user-attachments/assets/097cc128-c7fd-43df-b8a1-1a10dac2675c" />




## Credit

Fix surfaced by Reddit users debugging blurry YouTube playback on AMD GPUs under Chrome's D3D11 renderer.
