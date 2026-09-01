# CookieClip Combine & Compress 🍪🎥

**[🚀 Try it live here!](https://cookiebaits.github.io/ccvideocompress/)**

A purely client-side, browser-based video merger, compressor, and trimmer built for GitHub Pages. 

CookieClip uses WebAssembly (`FFmpeg.wasm`) to process videos locally inside your browser. Seamlessly merge sequences, trim clip boundaries, and optimize files for YouTube (H.264/AAC) while drastically reducing file sizes without noticeable quality loss.

## ✨ Features
* **Multi-Clip Merging:** Upload and combine up to 10 video clips into a seamless video file.
* **Drag-and-Drop & Custom Ordering:** Drag and drop files directly into the browser and reorder clips with one click before stitching.
* **Dual Format Export:** Choose between **MP4** or **MOV** container formats for both merged and compressed exports.
* **Smart Trimming & Compression:** Cut precise seconds from the beginning or end while shrinking file size for YouTube uploads.
* **100% Private & Ephemeral:** Videos never leave your device. All processing occurs locally in RAM with **zero history saved**—files are completely wiped the moment you close or refresh the tab.
* **Serverless Hosting:** Runs entirely on GitHub Pages without any backend server or API dependencies.

## 🚀 Deployment Instructions (GitHub Pages)

Because this tool utilizes complex multithreading via WebAssembly, modern web browsers require strict security headers (Cross-Origin Isolation) to run it. Since GitHub Pages does not allow custom headers, this repository uses a Service Worker workaround.

1. Upload `index.html` to the root of your GitHub repository.
2. Download `coi-serviceworker.js` from the [official COI Service Worker repo](https://raw.githubusercontent.com/gzuidhof/coi-serviceworker/master/coi-serviceworker.js).
3. Upload `coi-serviceworker.js` and an empty `.nojekyll` file to the root of your repository alongside `index.html`.
4. Go to your repository settings -> **Pages** -> Deploy from the `main` branch.
5. Visit your live site at `https://cookiebaits.github.io/ccvideocompress/`!

## ⚠️ Limitations
Since this app relies on your web browser rather than a dedicated desktop application, it is bound by browser limitations:
* **Memory Limits:** Browsers generally cap WebAssembly memory at ~2GB. Merging many high-resolution clips (like multiple 4K files) can exhaust browser RAM.
* **Immediate Download Required:** Files are kept only in temporary browser memory. If you refresh or navigate away before downloading, your processed video is purged and cannot be recovered.
* **Processing Speed:** In-browser WebAssembly encoding is subject to browser virtualization limits and will be slower than native desktop editors (such as Handbrake or Premiere Pro).
