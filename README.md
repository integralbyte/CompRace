# CompRace
**Client-Side Video compression** using FFmpeg compiled to WebAssembly → Your videos never leave your device.

## ⚙️ Options

* **Frames per second (FPS)** → lowering FPS reduces size; typical values: 30 → 24 → 20 → 15.
* **Target file size** → specify the desired MB, CompRace will adjust bitrate to aim near that size.

## 📦 Libraries note

This repo includes **2 of 4** required libraries directly.

* `ffmpeg.min.js` **initiates** loading of `814.ffmpeg.js`.
* Because that file is dynamically imported, browsers enforce **same-origin rules**.
* **Result**: `814.ffmpeg.js` cannot be loaded from a CDN (CORS blocks it).
* Therefore, both `ffmpeg.min.js` and `814.ffmpeg.js` are hosted **inside this repo**, while the other two libraries can safely come from a CDN.
