# CookieClip Compressor 🍪🎥

**[🚀 Try it live here!](https://cookiebaits.github.io/ccvideocompress/)**

A purely client-side, browser-based video compressor and trimmer built for GitHub Pages. 

CookieClip uses WebAssembly (`FFmpeg.wasm`) to process videos locally inside your browser. It formats files perfectly for YouTube (H.264, AAC, and `+faststart`) while drastically reducing file sizes without noticeable quality loss.

## ✨ Features
* **100% Private:** Videos never leave your device. All processing happens in your browser's RAM.
* **Auto-Cleanup:** Converted files and memory cache are automatically wiped the moment you close or refresh the tab.
* **Smart Trimming:** Easily cut out intros and outros down to the millisecond.
* **YouTube Optimized:** Applies Google's recommended video settings out of the box, including moving metadata to the front of the file so YouTube can process uploads faster.
* **Free Hosting:** Designed to work entirely on GitHub Pages without any backend server.

## 🚀 Deployment Instructions (GitHub Pages)

Because this tool utilizes complex multithreading via WebAssembly, modern web browsers require strict security headers (Cross-Origin Isolation) to run it. Since GitHub pages does not allow custom headers, this repository uses a Service Worker workaround.

1. Upload `index.html` to the root of your GitHub repository.
2. Download the `coi-serviceworker.js` file from the [official COI Service Worker repo](https://raw.githubusercontent.com/gzuidhof/coi-serviceworker/master/coi-serviceworker.js).
3. Upload `coi-serviceworker.js` to the root of your repository alongside `index.html`.
4. Go to your repository settings -> **Pages** -> Deploy from the `main` branch.
5. Visit your new GitHub pages URL at `https://cookiebaits.github.io/ccvideocompress/`!

## ⚠️ Limitations
Since this app relies on your web browser rather than a dedicated desktop application, it is bound by browser limitations:
* **Memory Limits:** Browsers generally cap WebAssembly memory at ~2GB. Very large files (like 4K hour-long uncompressed raw footage) will cause the browser tab to run out of memory and crash.
* **Speed:** Video processing runs through a browser virtualization layer. It will be slower than dedicated desktop software (like Handbrake or Premiere Pro).
