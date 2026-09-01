# CookieClip Combine & Compress 🍪🎥

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live%20Demo-brightgreen?style=flat&logo=github)](https://cookiebaits.github.io/ccvideocompress/)
[![GitHub Repo](https://img.shields.io/badge/Repository-ccvideocompress-blue?style=flat&logo=github)](https://github.com/cookiebaits/ccvideocompress)

**[🚀 Launch CookieClip Combine & Compress Live](https://cookiebaits.github.io/ccvideocompress/)**

A purely client-side, browser-based video merger, compressor, and trimmer built for static hosting on GitHub Pages.

CookieClip uses WebAssembly (`FFmpeg.wasm`) to process video files locally inside your browser. Combine clip sequences, trim timing down to the tenth of a second, and optimize exports for YouTube (H.264/AAC) without relying on backend servers or third-party file uploads.

---

## ✨ Features

* **Multi-Clip Merging:** Upload and combine up to **10 video clips** into a single sequence.
* **Drag-and-Drop & Reordering:** Drag files directly into the drop zone and adjust clip sequence order using up/down controls before stitching.
* **Dual Format Export:** Export both merged and compressed videos to **MP4** or **MOV**.
* **Precise Video Compression & Trimming:** Trim unwanted seconds from the start and end of videos while compressing footage to YouTube-ready bitrates.
* **100% Client-Side & Private:** Media never leaves your machine. Processing runs strictly in local browser RAM.
* **Zero-Persistence & Ephemeral RAM:** No history or files are cached to disk. Everything purges instantly when the tab is refreshed or closed.
* **Serverless Deployment:** Fully static web architecture ready for GitHub Pages hosting.

---

## 🛠️ Repository & File Structure

```text
ccvideocompress/
├── .nojekyll              # Disables Jekyll processing on GitHub Pages
├── coi-serviceworker.js   # Injects COOP/COEP headers for SharedArrayBuffer
├── index.html             # Main application UI and FFmpeg.wasm logic
└── README.md              # Project documentation
