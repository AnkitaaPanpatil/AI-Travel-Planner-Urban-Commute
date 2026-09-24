# 🌐 NexusVoyage AI — Smart Urban Commute & Tourism Optimization Engine

[![Status](https://img.shields.io/badge/Status-Active-emerald.svg)](#)
[![Stack](https://img.shields.io/badge/Tech-HTML5%20%7C%20TailwindCSS%20%7C%20Leaflet.js-teal.svg)](#)
[![AI](https://img.shields.io/badge/AI-Google%20Gemini-indigo.svg)](#)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](#)

NexusVoyage AI is a client-side, multi-modal urban transit routing and tourism planning platform designed to solve urban mobility bottlenecks. By combining real-time traffic analysis, carbon-emission trade-offs, interactive geospatial visualization, and generative AI concierge services, it streamlines daily commutes and curates intelligent city itineraries.

---

## 🚀 Key Features

### 1. 🚆 Interactive Multi-Modal Routing Engine
* **Holistic Mobility Comparison:** Evaluates and contrasts subway, light rail, city bus, active micromobility (e-bikes, scooters, walking), ferries, and electric rideshares side-by-side.
* **Multi-Metric Scoring:** Real-time calculation of:
  * **ETA & Reliability:** Predicts arrival times and risk of peak congestion delays.
  * **Financial Cost:** Accurately estimates transit fares versus rideshare surge pricing.
  * **Eco-Footprint ($CO_2$):** Compares emissions against baseline solo gasoline driving to promote green urban transit choices.

### 2. 🗺️ Interactive Geospatial Map (Leaflet.js)
* **Dark-Mode Cartography:** Powered by high-contrast CartoDB Dark Matter tiles tailored for modern UI dashboards.
* **Dynamic Route Waypoints:** Visualizes origin, destination, transfers, and route segments with color-coded multi-line paths.
* **Live Environmental Layers:**
  * Toggleable real-time traffic congestion corridors (Clear, Moderate, Heavy).
  * Key landmark points of interest (POIs) and transit hubs.
* **Commute Simulation:** One-click animated vehicle / commuter path simulation along selected route corridors (`Simulate Commute`).

### 3. 🏛️ Personalized Urban Tourism Planner
* **Tailored Sightseeing:** Builds sequenced, turn-by-turn travel itineraries filtered by:
  * **Duration:** Half-Day (4 hrs), Full-Day (8 hrs), Evening & Nightlife (4 hrs), or 2-Day exploration.
  * **Traveler Vibe:** Art & History, Street Food & Hidden Cafes, Architecture & Views, or Budget/Parks.
* **Sequential Navigation:** Arranges attractions logically to minimize transit overhead while providing local insider tips and recommended transit passes.

### 4. 🤖 Gemini AI Urban Assistant
* **Context-Aware Transit Concierge:** Real-time natural language query assistant for:
  * Airport transfer advice during morning and evening rush hours.
  * Local contactless payment tips (OMNY, Suica, Oyster, Navigo, etc.).
  * Off-the-beaten-path culinary and architecture walking routes.
  * Safety advisories and micromobility guidelines.

### 5. 🌍 Multi-City Global Hubs
* Built-in default geographic profiles, landmarks, and transit archetypes:
  * 🇺🇸 **New York City** (MTA Subway, CitiBike, East River Ferry, Rideshare)
  * 🇯🇵 **Tokyo** (Tokyo Metro, JR Yamanote Line, Harajuku/Asakusa routes)
  * 🇬🇧 **London** (Underground/Tube, Thames Clipper, Borough Market)
  * 🇫🇷 **Paris** (RER, Métro, Montmartre, Seine corridors)
  * 🇮🇳 **Mumbai** (Local Suburban Rail, Metro Line 3, Coastal promenades)
* Fully customizable origins and destinations for any location worldwide.

---

## 🛠️ Technology Stack

| Layer | Technologies |
|---|---|
| **Frontend Framework** | Pure Vanilla HTML5 & JavaScript (ES6+) |
| **Styling & UI** | Tailwind CSS (CDN), Font Awesome 6.4, Glassmorphism UI |
| **Geospatial & Mapping** | Leaflet.js 1.9.4 + CartoDB Dark Matter Vector Tiles |
| **AI Integration** | Google Gemini API (`gemini-2.5-flash` / `gemini-3-flash`) |
| **Architecture** | Single-File Standalone Architecture (Zero Node/NPM dependencies required) |

---

## 📦 Quick Start & Installation

Because the application is built using a standalone single-file architecture, setup requires no package managers or build tools.

### Option 1: Direct Browser Launch
1. Clone or download this repository:
   ```bash
   git clone https://github.com/your-username/nexusvoyage-ai.git
   cd nexusvoyage-ai
   ```
2. Double-click or open `index.html` in any modern web browser (Chrome, Firefox, Edge, Safari).

### Option 2: Local HTTP Server (Recommended)
Running through an HTTP server ensures full compatibility with browser fetch calls and map asset caching:

```bash
# Using Python 3
python -m http.server 8000

# Or using Node.js npx
npx serve .
```
Navigate to `http://localhost:8000` in your browser.

---

## ⚙️ Configuration & API Key

The application contains built-in resilient offline heuristic fallbacks. To enable live dynamic generative AI capabilities:

1. Open `index.html`.
2. Locate the API key variable in the script section:
   ```javascript
   const apiKey = "YOUR_GEMINI_API_KEY_HERE";
   ```
3. Replace with your Google AI Studio API key.

> **Note:** If an API key is not supplied or network connectivity is unavailable, the application automatically engages its localized offline transit routing and tour heuristics.

---

## 📖 Usage Guide

```
+-------------------------------------------------------------+
|                     NexusVoyage AI Dashboard                |
+------------------------------+------------------------------+
| [Control Panel]              | [Interactive Map]            |
| - Commute Hub                | - CartoDB Dark Matter Canvas |
| - Tourism Planner            | - Traffic & Transit Layers   |
| - AI Urban Assistant         | - Live Simulation Marker     |
|                              | - Step-by-Step Schedule      |
+------------------------------+------------------------------+
```

1. **Plan a Commute:**
   * Open the **Commute Hub** tab.
   * Input starting location and destination.
   * Select your priority (Fastest, Lowest Carbon, Cost-Effective, Scenic).
   * Click **Generate Optimized Commute Options** and select any itinerary card to plot its path.
2. **Simulate Transit:**
   * After choosing a commute route, click **Simulate Commute** below the map to track animated movement across the waypoints.
3. **Curate Sightseeing:**
   * Switch to the **Tourism Planner** tab, select your hours and style vibe, and generate a scheduled route with insider tips.
4. **Consult the AI Copilot:**
   * Use the **AI Assistant** tab to ask specific questions regarding delays, airport routes, or transit passes.

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.