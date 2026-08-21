# 🚆 RailHop — Offline Train & Interchange Search

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](#-roadmap--contributing)
[![Offline First](https://img.shields.io/badge/Offline-First-orange.svg)](#)
[![Search Speed](https://img.shields.io/badge/Search%20Time-~10ms-brightgreen.svg)](#)

> A lightweight, client-side transit search engine for Indian Railways that discovers both **direct trains** and **multi-hop connecting routes** in under 20 milliseconds — completely offline.

🔗 **Live Demo:** [railwaysearch.netlify.app](https://railwaysearch.netlify.app)

---

## ✨ Features

- ⚡ **Instant Client-Side Computation:** Computes routes in **7–40 ms** directly in the browser with zero API latency or backend roundtrips.
- 🔄 **Smart Connecting Train Routing:** Automatically discovers 1-hop interchange journeys with layover calculations when direct trains are unavailable.
- 🚉 **Multi-Station Querying:** Search across multiple origin and destination terminals simultaneously using comma-separated station codes (e.g., `NDLS,NZM` → `MMCT,BDTS`).
- 🔀 **Unique Train Filtering:** Toggle off redundant intermediate hops to keep results clean and actionable.
- 📴 **100% Offline-First:** Works without an active internet connection after the initial page load.
- 🛡️ **Zero Tracking & Bloat:** No ads, no analytics trackers, no logins, and minimal battery consumption.

---

## 🏗️ Architecture & How It Works

- **Zero Dependencies:** Pure vanilla HTML, CSS, and JavaScript contained in a single `index.html` file.
- **No Build Tools or Backend:** No Node.js, Python, npm, bundlers, or servers needed.
- **In-Browser Routing Algorithm:** The transit routing algorithm and compressed timetable dataset run entirely inside the client's browser engine.

---

## 🚀 Quickstart & Usage

Because this project is a **single, standalone `index.html` file**, there are zero dependencies to install:

### Option 1: Just open `index.html`
- **macOS:**
  ```bash
  open index.html
  ```
- **Windows:**
  ```cmd
  start index.html
  ```
- **Linux:**
  ```bash
  xdg-open index.html
  ```
*(Or simply double-click `index.html` in your file manager).*

### Option 2: Deploy to any static host
Drag and drop `index.html` onto **Netlify Drop**, **GitHub Pages**, **Vercel**, or **Cloudflare Pages** — it works instantly out of the box.

---

## 🗺️ Roadmap & Contributing

Contributions are very welcome! Here are some high-impact areas to get involved:

- [ ] **Fuzzy Station Search:** Autocomplete station names (e.g., typing *"Bangalore"* automatically maps to `SBC`, `YPR`, `SMVB`).
- [ ] **Historical Punctuality Scoring:** Integrate 3–6 month historical arrival reliability data to score connection risks (🟢 High / 🟡 Risky / 🔴 Unlikely).
- [ ] **Web Workers:** Offload heavy multi-station graph traversal to background threads.
- [ ] **Modern Mobile UI:** Add responsive cards and dark mode support.
- [ ] **Automated Data Pipeline:** GitHub Actions workflow to refresh timetable data periodically.

---

## 📊 Data Source & Attribution

- Train schedule and station data are compiled from public Indian Railways timetable releases for educational and informational use.
- **Disclaimer:** *This is an independent open-source project and is not affiliated with, maintained, or endorsed by Indian Railways, IRCTC, or NTES. For official bookings and live train tracking, visit [irctc.co.in](https://www.irctc.co.in).*

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
