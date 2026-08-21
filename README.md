
    # 🚆 RailHop — Offline Train & Interchange Search
    
    [![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
    [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](#contributing)
    [![Offline First](https://img.shields.io/badge/Offline-First-orange.svg)](#)
    [![Search Speed](https://img.shields.io/badge/Search%20Time-~10ms-brightgreen.svg)](#)
    
    > A lightweight, client-side transit search engine for Indian Railways that discovers both **direct trains** and **multi-hop connecting routes** in under 20 milliseconds — completely offline.
    
    🔗 **Live Demo:** https://railwaysearch.netlify.app
    
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

    1. **Pre-compiled Static Dataset:** Train schedules and station matrices are compressed into lightweight static assets.
    2. **In-Browser Routing Algorithm:** Uses a client-side transit routing algorithm to find valid transfers within specified layover windows.
    3. **PWA & Static Hosting:** Hosted as a static application on Netlify with zero server maintenance costs.

    ---

    ## 🚀 Quickstart & Local Setup

    Because this project is 100% client-side and serverless, getting started takes less than a minute:

    ### 1. Clone the repository
    ```bash
    git clone https://github.com/your-username/railhop.git
    cd railhop

  ### 2. Run locally

  You can serve the directory using any static file server:

    # Using Python
    python3 -m http.server 8000

    # OR using Node
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
  ──────
  ## 📊 Data Source & Attribution

  • Train schedule and station data are compiled from public Indian Railways timetable releases for educational and informational use.
  • Disclaimer: This is an independent open-source project and is not affiliated with, maintained, or endorsed by Indian Railways, IRCTC, or NTES. For official bookings and live train tracking, visit irctc.co.in https://www.irctc.co.in.
  ──────
  ## 📄 License

  This project is open source and available under the MIT License /LICENSE.


    ---

    ### 📜 **3. `LICENSE` (Raw Content for Direct Copy & Paste)**

    ```text
    MIT License

    Copyright (c) 2026 Soham Mirikar

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.

    ---
    Data Disclaimer:
    The transit schedules and station datasets in this repository are sourced from 
    publicly available timetables for educational and informational purposes. 
    This project is an unofficial tool not affiliated with or endorsed by Indian Railways or IRCTC.
