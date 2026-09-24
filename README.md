# KompPRO v1.2 — The Ultimate Successor to Komp-presor PRO

Welcome to **KompPRO v1.2**, the official upgraded successor to **Komp-presor PRO**. KompPRO has been completely re-architected and upgraded from a single-file processing interface into a professional-grade, multi-threaded, hardware-accelerated **batch video compression studio**.

---

## 📸 Evolution & UI Comparison

| Feature / Aspect | Previous Version (Komp-presor PRO)[cite: 1] | New Successor (KompPRO v1.2) |
| :--- | :--- | :--- |
| **Workflow** | Single-file input queue ("Engage Compression")[cite: 1]. | Full **Batch Import Queue** supporting multi-file processing concurrently. |
| **Hardware Telemetry** | Static or placeholder counters[cite: 1]. | **Live, Real-Time Telemetry** featuring animated graphs tracking CPU, RAM, and NVIDIA GPU usage via `psutil` and `GPUtil`. |
| **Concurrency Control** | Hardcoded single stream[cite: 1]. | **Dynamic Concurrency Profiling** that auto-scales streams (1 to 4) based on system VRAM, with manual override options. |
| **Error Handling** | Basic layout prone to crashing on unsupported codecs[cite: 1]. | **Self-Healing Smart Fallback System** that automatically switches to a pure CPU pipeline (`libx264`) if hardware decoding/encoding locks up. |
| **Logs & Monitoring** | Basic bottom container[cite: 1]. | Expanded, color-coded **System Logs Console** tracking granular session states, warnings, and success flags. |

---

## 🚀 What’s New in KompPRO v1.2

* **Complete UI/UX Overhaul ("Metric Flow"):** Evolving past the legacy look, KompPRO introduces a modern "Nightshade/Ember" dark dashboard with persistent sidebar navigation (*Dashboard, Settings, Output Library, Help Center*), top window navigation arrows, and instant path-loading capabilities.
* **Intelligent Batch Queue & VRAM Management:** Safely manages massive video batches using worker threads coupled with strict VRAM flushing and a 2-second cooldown between tasks to prevent memory overflow on consumer graphics cards.
* **Precise Session Analytics:** Replaced generic layout counters with color-coded job completion times (`Done in Xm Ys`) and persistent output directory integration.
* **Robust FFprobe Metadata Analysis:** Features suppressed background terminal windows (`CREATE_NO_WINDOW`) to eliminate window-flashing and prevent I/O pipeline crashes during high-speed batch imports.

---

## 🛠️ Core Architecture & Tech Stack
* **Core Framework:** Python, Eel, Tkinter, psutil, GPUtil
* **Frontend:** HTML5, Modern CSS (Nightshade/Ember theme), Vanilla JavaScript
* **Media Engines:** FFmpeg / FFprobe with native NVIDIA NVENC (H.264 & HEVC/H.265) support and CPU (`libx264`) fallback.

---

## 💻 Installation & Usage
1. Go to the **[Releases](../../releases)** tab on the right side of this repository.
2. Download the latest `KompPRO-v1.2.zip` release archive.
3. Extract the folder and run `main.exe` *(Ensure `ffmpeg.exe` and `ffprobe.exe` are placed in the same directory)*.

---

## 📜 License
This project is open-source software licensed under the [MIT License](LICENSE.txt).
