
    # 🚆 RailHop — Offline Train & Interchange Search

    [![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
    [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
    [![Offline First](https://img.shields.io/badge/Offline-First-orange.svg)](#)
    [![Performance](https://img.shields.io/badge/Search%20Time-~10ms-brightgreen.svg)](#)

    > A lightweight, client-side transit search engine for Indian Railways that discovers both **direct trains** and **multi-hop connecting routes** in under 20 milliseconds — completely offline.

    🔗 **Live Demo:** https://railwaysearch.netlify.app

    ---

    ## ✨ Features

    - ⚡ **Instant Client-Side Computation:** Computes routes in **7–40 ms** directly in the browser with zero API latency or backend server roundtrips.
    - 🔄 **Smart Connecting Train Routing:** Automatically discovers 1-hop interchange journeys with layover calculations when direct trains are unavailable or full.
    - 🚉 **Multi-Station Querying:** Search across multiple origin and destination terminals simultaneously using comma-separated station codes (e.g., `NDLS,NZM` $\to$ `MMCT,BDTS`).
    - 🔀 **Unique Train Filtering:** Toggle off redundant intermediate hops to keep results clean and actionable.
    - 📴 **100% Offline-First:** Works without an active internet connection after the initial page load.
    - 🛡️ **Zero Tracking & Bloat:** No ads, no tracking cookies, no logins, and minimal battery consumption.

    ---

    ## 🏗️ How It Works

    ```mermaid
    flowchart LR
        A["Compressed Timetable Data<br/>(Stations & Schedules)"] --> B["In-Memory Graph Index"]
        B --> C["Client-Side Routing Engine<br/>(CSA / RAPTOR Algorithm)"]
        C --> D["Fast Result Table<br/>(Route, Changes, Layovers)"]

  1. Pre-compiled Static Dataset: Train schedules and station matrices are compressed into lightweight static assets.
  2. In-Browser Routing Algorithm: Uses a client-side transit routing algorithm (such as Connection Scan Algorithm / shortest path graph search) to find valid transfers within specified layover windows.
  3. PWA & Static Hosting: Hosted as a static application with zero server maintenance costs.
  ──────
  ## 🚀 Quickstart & Local Setup

  Because this project is 100% client-side and serverless, getting started takes less than a minute:

  ### 1. Clone the repository

    git clone https://github.com/your-username/railhop.git
    cd railhop

  ### 2. Run locally

  You can serve the directory using any static file server:

    # Using Python
    python3 -m http.server 8000

    # OR using Node (npx)
    npx serve .

  Open http://localhost:8000 in your browser.
  ──────
  ## 🗺️ Roadmap & Contributing

  Contributions are very welcome! Here are some high-impact areas to get involved:

  [ ] Fuzzy Station Search: Autocomplete station names (e.g., typing "Bangalore" automatically maps to SBC, YPR, SMVB).
  [ ] Historical Punctuality Scoring: Integrate 3–6 month historical arrival reliability data to score connection risks (🟢 High / 🟡 Risky / 🔴 Unlikely).
  [ ] Web Workers: Offload heavy multi-station graph traversal to background threads.
  [ ] Modern Mobile UI: Add responsive cards and dark mode support.
  [ ] Automated Data Pipeline: GitHub Actions workflow to refresh timetable data periodically.

  Please check out CONTRIBUTING.md to get started!
  ──────
  ## 📊 Data Source & Attribution

  • Train schedule and station data are compiled from public Indian Railways timetable releases for educational and informational use.
  • Disclaimer: This is an independent open-source project and is not affiliated with, maintained, or endorsed by Indian Railways, IRCTC, or NTES. For official bookings and live train tracking, visit irctc.co.in https://www.irctc.co.in.
  ──────
  ## 📄 License

  This project is open source and available under the MIT License /LICENSE.
