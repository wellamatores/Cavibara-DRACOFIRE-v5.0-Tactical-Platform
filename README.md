# 🦖 Cavibara + DRACOFIRE v5.2

**Tactical Geospatial Platform** — A full-featured browser-based GIS with 3D planet, 2D map, and terrain simulator for tactical analysis and mission planning.

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Requirements](#-requirements)
- [Installation & Usage](#-installation--usage)
- [Keyboard Shortcuts](#-keyboard-shortcuts)
- [API Reference](#-api-reference)
- [Screenshots](#-screenshots)
- [License](#-license)

---

## 🌍 Overview

**Cavibara + DRACOFIRE v5.2** is a powerful web-based geospatial intelligence platform designed for military, emergency response, surveying, and analytical applications. It combines:

- **3D Planet** (Three.js) with cities and air traffic
- **2D Map** (Leaflet) with marker clustering
- **Full 3D Terrain Simulator** with 12 tactical objects
- **Tactical Tools**: NATO symbology, BFT, MGRS, LOS, Zone Analysis
- **Navigation Modules**: Dead Reckoning, Pace Count, Offline Mode
- **Analysis Tools**: Measurements, Routes, Analytics with charts

---

## 🎯 Features

### 🗺️ Cartography
| Feature | Description |
|---------|-------------|
| **3D Planet** | Rotating planet with cities, lighting, and air traffic |
| **2D Map** | Interactive OpenStreetMap with marker clustering |
| **Terrain Sim** | Full 3D terrain model with mountains, rivers, and lakes |

### 🎯 Tactical Tools
| Feature | Description |
|---------|-------------|
| **NATO Library** | 14 tactical symbols (Friendly, Hostile, Helicopter, Aircraft, UAV, Logistics, Medical, Obstacle, Casualty, Objective, Boundary, Danger Zone) |
| **BFT** | Blue Force Tracking — unit movement emulation |
| **MGRS** | Military Grid Reference System coordinates |
| **LOS** | Line of Sight — visibility analysis between points |
| **Zone Analysis** | Engagement/visibility zone creation |

### 🧭 Navigation
| Feature | Description |
|---------|-------------|
| **Dead Reckoning** | Azimuth and distance navigation (manual + auto mode) |
| **Pace Count** | Step counting with distance, pace, and speed calculation |
| **Geolocation** | User location detection |
| **Auto-Tour** | Automated flyover of cities |

### 📐 Analysis Tools
| Feature | Description |
|---------|-------------|
| **Measurements** | Distance and area (click on map) |
| **Routes** | 5 types: Auto, Walk, Flight, Ship, Rail + animation |
| **Analytics** | Activity charts, KPI, weather, AQI |
| **Search** | Quick search for cities, countries, and landmarks |

### 💾 Data Management
| Feature | Description |
|---------|-------------|
| **Offline Mode** | Map tile caching with IndexedDB |
| **Export** | Screenshot, GeoJSON, KML, CSV, Full Project (JSON) |
| **Import** | GeoJSON, KML, GPX, Full Project |
| **History** | Full action logging |

### 🎨 Interface
| Feature | Description |
|---------|-------------|
| **5 Access Tiers** | Civilian → Pro → Service → Tactical → Command |
| **Night Mode** | Color inversion for low-light operations |
| **Presentation Mode** | Hides all UI elements |
| **Responsive Design** | Desktop and mobile support |
| **Minimap** | Small orientation map in corner |

### 🌍 Terrain Sim — 12 Objects on Terrain
1. 🏘️ **Settlement** — village with 60 houses
2. 💧 **Lake** — water body
3. 🏞️ **River** — flowing waterway
4. 🌲 **Forest** — 600 trees
5. ⛏️ **Mine** — shaft with tower
6. 🏚️ **Bunker** — fortified structure
7. 🌊 **Sea Coast** — shoreline
8. 🚧 **Checkpoint** — road control point
9. 🏰 **Military Base** — with vehicles and soldiers
10. 🚩 **Command Post** — headquarters
11. 📍 **Waypoint** — beacon with pulsing ring
12. 💨 **Dust Particles** — atmospheric effects

---

## 💻 Requirements

| Requirement | Minimum |
|-------------|---------|
| **Browser** | Chrome 90+, Firefox 88+, Edge 90+, Safari 15+ |
| **Internet** | Required for library and tile loading |
| **RAM** | 512 MB+ |
| **WebGL** | WebGL 1.0+ support |

---

## 🚀 Installation & Usage

### Quick Start
1. Download `index.html`
2. Open in your browser
3. Wait for loading

### For Development
```bash
# Clone repository
git clone https://github.com/your-username/cavibara-dracfire.git
cd cavibara-dracfire

# Open in browser
open index.html
# Or use Live Server in VS Code
```

---

## ⌨️ Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `1` | 3D Planet |
| `2` | 2D Map |
| `3` | Globe |
| `4` | Terrain Sim |
| `Ctrl+1-5` | Switch access tier |
| `H` | Home / Reset camera |
| `M` | Toggle menu |
| `F` | Fullscreen |
| `P` | Presentation mode |
| `R` | Auto-rotate planet |
| `T` | Auto-tour cities |
| `G` | Geolocation |
| `S` | Focus search |
| `N` | Night mode |
| `Escape` | Close all panels |

---

## 🔌 API Reference

Global API available after loading:

```javascript
// Core functions
Cavibara.flyTo(lat, lng, alt)          // Fly to coordinates
Cavibara.flyHome()                      // Reset camera
Cavibara.switchView('3d' | '2d' | 'globe' | 'terrain')
Cavibara.setTier(1-5)                   // Set access tier
Cavibara.toggleLayer('osm' | 'satellite' | 'terrain' | 'dark')

// Tactical tools
Cavibara.toggleMGRS()
Cavibara.toggleNATO()
Cavibara.toggleBlueForce()

// Export
Cavibara.exportScreenshot()
Cavibara.exportGeoJSON()
Cavibara.saveState()

// Dead Reckoning
Cavibara.dr.applyManual()               // Apply current settings
Cavibara.dr.startAuto()                 // Auto mode
Cavibara.dr.stop()
Cavibara.dr.reset()

// Pace Count
Cavibara.pace.addSteps(10)              // Add steps
Cavibara.pace.reset()

// Offline
Cavibara.offline.downloadRegion()       // Download current region
Cavibara.offline.clearCache()

// NATO Library
Cavibara.nato.applySymbol('SFGPUCP----------')

// LOS
Cavibara.los.calculate()
Cavibara.los.clear()

// Terrain
Cavibara.terrain.toggle()               // Open/close Terrain Sim
Cavibara.terrain.close()
Cavibara.terrain.status()               // Check status

// Utilities
Cavibara.getGeolocation()
Cavibara.notify('message', 'info' | 'success' | 'warning' | 'error')
Cavibara.state                         // Full state object
```

---

## 📸 Screenshots

| View | Description |
|------|-------------|
| 🌍 **3D Planet** | Rotating planet with cities and traffic |
| 🗺️ **2D Map** | Interactive map with marker clustering |
| 🏔️ **Terrain Sim** | Full 3D terrain with 12 objects |
| 🎯 **NATO Library** | 14 tactical symbols |
| 📊 **Analytics** | Charts, KPI, weather |

---

## 🛠️ Technologies Used

| Library | Version | Purpose |
|---------|---------|---------|
| [Three.js](https://threejs.org/) | r128 | 3D planet and Terrain Sim |
| [Leaflet](https://leafletjs.com/) | 1.9.4 | 2D map |
| [Chart.js](https://www.chartjs.org/) | 4.4.0 | Analytics charts |
| [milsymbol](https://github.com/spatialillusions/milsymbol) | 2.3.0 | NATO symbols |
| [mgrs](https://github.com/proj4js/mgrs) | 1.0.0 | MGRS coordinates |
| [Font Awesome](https://fontawesome.com/) | 6.5.0 | Icons |

---

## 📄 License

This project is distributed under the **MIT License**.

---

## 🙏 Acknowledgments

- [Three.js](https://threejs.org/) — 3D engine
- [Leaflet](https://leafletjs.com/) — mapping foundation
- [OpenStreetMap](https://www.openstreetmap.org/) — map data
- [Spatial Illusions](https://github.com/spatialillusions) — milsymbol library

---

## 📞 Contact

- **Version:** 5.2.0 FULL
- **Developer:** Wellamatores Labs
- **Email:** wellamatores@gmail.com

---

<div align="center">
  <sub>Built with ❤️ for tactical geospatial analysis</sub>
</div>
