<div align="center">

# ⚡ GetVideo — High-Performance, Ad-Free Video & Audio Downloader

**The modern, privacy-focused open web utility to download public media in 4K, extract clean audio, and download bilingual subtitles without scammy ads or malware.**

[![Live Demo](https://img.shields.io/badge/Live_App-getvideo.techhowl.site-00C7B7?style=for-the-badge&logo=googlechrome&logoColor=white)](https://getvideo.techhowl.site)
[![Next.js 14](https://img.shields.io/badge/Frontend-Next.js_14_App_Router-black?style=for-the-badge&logo=nextdotjs)](https://nextjs.org/)
[![FastAPI](https://img.shields.io/badge/Backend-FastAPI_Python_3.13-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

[**Explore Live Web App »**](https://getvideo.techhowl.site) · [Report Bug](https://getvideo.techhowl.site/contact) · [Feature Request](https://getvideo.techhowl.site)

</div>

---

## 💡 Why GetVideo?

Almost every video downloader on the internet today is broken by design:
- ❌ Infested with popup ads, adult redirects, and fake green "Download" buttons.
- ❌ Forces you to wait 30 seconds for shady conversion servers.
- ❌ Fails on Reddit videos (downloads without audio) and leaves TikTok watermarks.
- ❌ Lacks modern subtitle support (SRT/VTT) and bilingual transcript merging.

**[GetVideo](https://getvideo.techhowl.site)** was built to fix this forever. It is an engineering-first web utility built on Next.js 14 and FastAPI that delivers clean, lightning-fast media downloads with **zero intrusive ads, zero user tracking, and zero long-term data storage**.

---

## ✨ Key Features

- **🎬 Universal Platform Support**: Seamless public downloads from YouTube (up to 4K 60fps / HDR), TikTok (100% Watermark-free), Instagram Reels, Facebook Public Videos, X/Twitter, Reddit (with synced audio), SoundCloud, and Pinterest.
- **⚡ Zero-Re-encoding Stream Copy**: Merges video and audio streams instantly using FFmpeg stream copy (`-c copy`) without CPU-heavy transcoding delays.
- **📝 Subtitles & Transcripts Studio**: Download timecoded subtitles (`.srt`, `.vtt`) or export clean plain-text transcripts. Supports **Bilingual Subtitles** (merge two languages side-by-side).
- **🔒 Privacy & Ephemeral Storage**: Zero user logs, no authentication required, and all temporary extraction files are permanently wiped after 15 minutes.
- **📱 Progressive Web App (PWA)**: Installable on iOS and Android with native **Web Share Target** support (share a link directly from YouTube/TikTok into GetVideo).
- **🌍 Multilingual**: Native English and Urdu (RTL) support with automatic locale detection.

---

## 📊 Comparison: GetVideo vs Legacy Downloaders

| Feature | Legacy Downloaders (Y2Mate, SaveFrom) | GetVideo (getvideo.techhowl.site) |
| :--- | :---: | :---: |
| **Ads & Popups** | 🚨 Intrusive popups, adult redirects | 🛡️ **Zero intrusive ads, clean UI** |
| **Reddit Video Audio** | 🔇 Usually downloaded muted | ✅ **Synced stereo audio merged via FFmpeg** |
| **TikTok Watermark** | ❌ Watermarked | ✅ **100% Clean / No Watermark** |
| **Subtitles Studio** | ❌ None | ✅ **SRT, VTT, Clean TXT & Dual-Subs** |
| **Speed** | ⏳ Slow queue / Artificial wait | ⚡ **Real-time SSE live progress** |
| **PWA Mobile Share** | ❌ None | ✅ **Native Android & iOS Share Target** |

---

## 🛠️ Architecture & Tech Stack

[ User Browser / PWA ] (Next.js 14 App Router, Tailwind CSS, SSE Progress) │ ▼ [ Caddy 2.0 Reverse Proxy ] (Automated TLS, Rate Limiting, HSTS) ├── / → Next.js 14 Standalone Server (Port 3000) └── /api/* → FastAPI Async Backend (Python 3.13, 4 Uvicorn Workers) │ ├── Redis 7 (Token Bucket Rate Limiting, ARQ Job Queue) ├── ARQ Worker Pool (yt-dlp extraction, FFmpeg stream-copy) ├── Ephemeral Cleanup Daemon (15-min TTL auto-purge) └── Prometheus & SRE Canary Probes


---

## 🚀 Try It Live

The production application is running live at:
👉 **[https://getvideo.techhowl.site](https://getvideo.techhowl.site)**

### Popular Utilities:
- [YouTube 4K & MP3 Downloader](https://getvideo.techhowl.site/en/youtube-video-downloader)
- [TikTok No-Watermark Downloader](https://getvideo.techhowl.site/en/tiktok-video-downloader)
- [Instagram Reels Downloader](https://getvideo.techhowl.site/en/instagram-reels-downloader)
- [Reddit Video Downloader with Audio](https://getvideo.techhowl.site/en/reddit-video-downloader)

---

## ⚖️ Legal & DMCA Compliance

GetVideo respects intellectual property rights. It is strictly engineered for **publicly accessible content** only. It does not bypass DRM, does not store private user tokens, and does not retain media files permanently. Takedown requests can be submitted directly via our [DMCA Policy](https://getvideo.techhowl.site/dmca).

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
