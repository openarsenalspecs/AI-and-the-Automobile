# TrueRoute

**Because the right route matters.**

TrueRoute is an open-source, vehicle-aware, offline-capable, real-time adaptive navigation and travel intelligence platform built on OpenStreetMap and modern geospatial infrastructure.

It replaces traditional GPS navigation with a modular system that understands your **vehicle, environment, preferences, and real-time conditions**, while turning every trip into a curated travel experience.

---

# 🌍 Core Vision

TrueRoute is not just a navigation app.

It is a **modular travel intelligence ecosystem** that combines:

- Vehicle-aware routing  
- Scenic exploration  
- Offline navigation  
- Real-time road intelligence  
- AI-powered trip planning  
- Continuous travel adaptation  

---

# 🚗 Full Feature List

## 🧭 Core Navigation System

### 🗺️ Vehicle-Aware Routing
- Accepts vehicle dimensions:
  - Height
  - Width
  - Length
  - Weight
- Avoids:
  - Low bridges
  - Narrow roads
  - Restricted routes
  - Unsafe terrain for vehicle type
- Supports:
  - Cars
  - SUVs
  - Vans
  - RVs
  - Trailers
  - Custom vehicles

---

### 🚦 Routing Modes
- Fastest route
- Safest route
- Scenic route
- Exploration route
- Balanced route

---

### 🧠 Dynamic Optimization
- Real-time rerouting
- Constraint-based pathfinding
- Multi-objective optimization:
  - Time
  - Safety
  - Scenic value
  - Vehicle compatibility

---

## 🌄 Exploration & Travel Experience

### 🧭 Exploration Mode
- Avoids highways by default
- Prioritizes scenic roads and byways
- Encourages detours for attractions
- Enhances rural and natural routing

---

### 🌍 Scenic Engine
- Elevation scoring
- Water proximity weighting
- Forest density analysis
- Scenic highway detection
- Route “beauty scoring”

---

### 📍 Travel Discovery System
- Roadside attractions
- Tourist landmarks
- Local hidden gems
- Nature viewpoints
- Cultural and historic sites

---

### 🧳 Trip Experience Builder
- Multi-stop journey creation
- Attraction clustering
- Rest stop optimization
- Day-by-day itineraries

---

## 📦 Offline & Survival Mode

### 🛰️ Offline Navigation
- Full map downloads (regional packs)
- Offline routing engine
- GPS-only navigation support
- Cached POI database

---

### 📡 No-Signal Mode
- Works without internet
- Offline rerouting
- Cached hazard + POI data
- Battery-optimized operation

---

### 🚨 Emergency Routing
- Finds nearest safe exit route
- Prioritizes highways or towns
- Safety-first override system

---

## 🚨 Real-Time Road Intelligence

### 🚧 Live Road Conditions
- Construction updates
- Road closures
- DOT data integration
- Community reports

---

### 🌦️ Weather-Aware Routing
- Storm avoidance
- Snow/ice routing adjustments
- Flood risk detection
- Wind hazard detection

---

### 🚨 Hazard Detection
- Accident-prone roads
- Sharp curve zones
- Wildlife crossings
- Low visibility areas

---

### 🧭 Adaptive Rerouting Engine
- Real-time route recalculation
- Safe reroute option
- Scenic reroute option
- Fast reroute option
- Stability-aware rerouting control

---

### 📡 Community Road Network
- User-submitted road reports
- GitLab-based moderation
- Verified issue tracking
- Reputation scoring system

---

## 🤖 AI Trip Planning System

### 🧠 Natural Language Planning
- Converts text into full trip plans:
  - “Plan a 3-day scenic RV trip avoiding highways”

---

### 🗺️ Multi-Stop Trip Generator
- Full itinerary creation
- Stop scheduling
- Route segmentation
- Travel time optimization

---

### 🚐 Vehicle-Aware Planning
- Applies vehicle constraints automatically
- Ensures route safety for vehicle type

---

### 🌄 Experience Builder
- Scenic vs transit segmentation
- Planned detours
- Highlighted journey moments

---

### 📦 Trip Packaging System
- Complete travel bundles:
  - Routes
  - POIs
  - Itineraries
  - Offline maps

---

## 🧠 AI Expansion Layer (Real-Time Copilot)

### 🗣️ Conversational Driving Assistant
- Real-time commands:
  - “Avoid highways”
  - “Find a scenic stop”
  - “Reroute me somewhere interesting”
- Context-aware adjustments while driving

---

### 🧭 Intent Rewriting Engine
- Converts vague intent into structured routing logic:
  - “Make it relaxing” → low-stress scenic routing
  - “Show me something interesting” → exploration mode activation

---

### 🌍 Context-Aware Intelligence
- Detects:
  - Nearby POIs
  - Traffic changes
  - Weather shifts
  - Road conditions
- Provides proactive suggestions

---

### 🌄 Dynamic Experience Shaping
- Adjusts route behavior in real time:
  - Scenic intensity
  - Stop frequency
  - Exploration level
  - Driving comfort

---

### 🧬 Route Memory System
- Learns user behavior:
  - Scenic vs fast preference
  - Reroute patterns
  - Ignored suggestions
- Personalizes future routing

---

### 🔄 Continuous Trip Replanning
- Updates trip while driving
- Responds to:
  - Weather changes
  - Traffic shifts
  - User input
  - New discoveries

---

## 🧠 Data & Intelligence Layer

### 🌍 Global Scenic Index
- Global road beauty ranking system
- Community-driven scoring
- Dynamic route attractiveness evaluation

---

### 🧬 Route Memory Graph
- Travel history visualization
- Heatmaps of exploration
- Suggested unexplored regions

---

## 🧩 Modular System Design

### 🔌 Plugin Architecture
- Routing plugins
- POI providers
- Scenic scoring systems
- Hazard detection modules
- UI extensions

---

### 🧱 Fully Modular Design
- Independent system modules
- Replaceable components
- Device-agnostic architecture
- Offline + cloud hybrid support

---

## 📱 Device Support

### 💻 Web
- Full navigation + planning interface

### 📱 Mobile
- Offline-first navigation
- GPS + sensor integration

### 🚗 In-Vehicle
- Minimal distraction UI
- Voice-first navigation

### 🧠 Edge Devices
- Offline routing engines
- Remote-area support

---

## 🗺️ Mapping & Data System

### 🗺️ Map Engine
- OpenStreetMap integration
- MapLibre rendering

---

### 📍 POI System
- OpenTripMap
- Wikidata / Wikivoyage
- OSM POIs
- Community submissions

---

### 🗄️ Spatial Database
- PostgreSQL + PostGIS
- High-performance geospatial queries

---

## ⚙️ Backend & Infrastructure

### 🚦 Routing Engine
- GraphHopper (open-source core)
- Vehicle constraint system
- Scenic weighting engine

---

### ⚙️ Backend Services
- Node.js (Fastify)
- Redis caching
- Docker microservices

---

### 🧰 DevOps
- GitLab CI/CD
- Issue-driven development
- Merge request workflow

---

# 📦 Installation (WIP)
This project is in active development. Setup instructions will be added as core modules stabilize.

---

# 🧪 Development Status
TrueRoute is currently in early architectural development. Core systems are being designed for modular implementation across:

- Routing engine
- Map rendering
- AI trip planning
- Real-time intelligence layer

---

## Specification Branding License (SBL)
### Standard
- Fully AGPL-3.0+ compliant system
- Copyleft enforced for network deployments
- Required attribution:
  - Roxanne Ardary
  - https://www.roxanneardary.com/

### Optional

- **Specification Branding License (SBL)**
  - Attribution-free commercial deployment
  - Pricing based on scale, usage, and deployment scope
  - [https://roxanneardary.com/trueroute/](https://roxanneardary.com/trueroute/)  

---

# 📜 License & Notice Requirements

TrueRoute is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- TrueRoute specificiations are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
---

# 🌍 Summary

TrueRoute is:

> A modular, open-source navigation ecosystem that combines vehicle-aware routing, scenic exploration, offline resilience, real-time road intelligence, and AI-driven trip planning into a single adaptive system that runs on any device.

---

**Built in the open. Designed for the road ahead.**  
