# CookieClip Combine & Compress 🍪🎥

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live%20Demo-brightgreen?style=flat&logo=github)](https://cookiebaits.github.io/ccvideocompress/)
[![GitHub Repo](https://img.shields.io/badge/Repository-ccvideocompress-blue?style=flat&logo=github)](https://github.com/cookiebaits/ccvideocompress)

**[🚀 Launch CookieClip Combine & Compress Live](https://cookiebaits.github.io/ccvideocompress/)**

A purely client-side, browser-based video merger, compressor, trimmer, and audio suite built specifically for static hosting on GitHub Pages.

CookieClip runs WebAssembly (`FFmpeg.wasm`) to process video files locally inside your browser. Merge mixed-orientation clips, customize background music with smooth fades, trim timing down to the tenth of a second, and optimize exports for YouTube (H.264/AAC) without backend servers, data logging, or third-party file uploads.

---

## ✨ Features

### 🎬 Multi-Clip Merging & Auto-Sorting
* **Combine Up to 10 Videos:** Stitch multiple MP4, MOV, or WebM files into a single video sequence.
* **Natural Alphanumeric Auto-Sorting:** Uploaded files automatically sort in natural alphabetical and numeric sequence (`1a`, `1b`, `1c`, `2`, `10`).
* **Drag-and-Drop & Custom Ordering:** Easily drag and drop files into the staging area and reorder clips with `▲` / `▼` controls.

### 📐 Mixed-Orientation & Universal Scaler
* **Aspect Ratio Normalization:** Seamlessly combines vertical (9:16 Shorts/TikToks) and horizontal (16:9) footage without stream mismatch crashes.
* **Aspect Ratio Selector:** Choose your output orientation (**Landscape 16:9** or **Portrait 9:16**) with automated letterboxing/pillarboxing.
* **Timestamp & Audio Sync:** Standardizes frame rates (`30 fps`), pixel formats (`yuv420p`), and audio sample rates (`44.1kHz stereo`) to prevent video skipping, freezing, or stutter.

### 🎵 Advanced Audio Controls
* **4 Audio Modes:**
  * **Keep Original Audio:** Retains existing audio tracks.
  * **Mute Output Video:** Drops the audio stream entirely.
  * **Add Custom Background Music:** Mixes your custom track (.mp3, .wav, .aac) over the original clip audio.
  * **Mute & Replace:** Replaces original video audio entirely with your background track.
* **Infinite Music Looping:** Automatically loops background music if the video is longer than the audio file (enabled by default).
* **Smart Audio Fades:** Applies customizable **Fade In** (default: 2.0s) and **Fade Out** (default: 3.0s) transitions.

### 🗜️ Video Compressor & Millisecond Trimmer
* **YouTube Ready:** Compresses video files using standard H.264 / AAC codecs with optimal CRF targets.
* **Precision Trimming:** Remove unwanted seconds from both the beginning and end of any video clip.

### ⚡ Seamless UX & Ephemeral Privacy
* **Interactive Button State:** The processing button transforms directly into a **⬇️ Download Merged Video (.FORMAT)** button upon completion.
* **Dual Container Formats:** Export both merged and compressed clips in `.MP4` or `.MOV`.
* **Zero Persistence & 100% RAM Processing:** No data is stored on disk or servers. Virtual file systems and memory are instantly purged when the tab is closed or refreshed.

---

## 🛠️ Repository & File Structure

```text
ccvideocompress/
├── .nojekyll              # Disables Jekyll processing on GitHub Pages
├── coi-serviceworker.js   # Cross-origin isolation helper script
├── index.html             # Application UI, drag-and-drop logic & FFmpeg engine
└── README.md              # Project documentation
