# DRRM City — Flood Defense (Isometric Prototype)

## 🧭 Overview
**DRRM City** is a browser-based educational simulation game designed to promote awareness and understanding of **Disaster Risk Reduction and Management (DRRM)** through interactive gameplay. It combines strategic planning, environmental awareness, and physics-based water simulation in an isometric environment inspired by *SimCity*, *Cities: Skylines*, and *Poly Bridge*.

The project was developed as part of the **DOST Level Up: Esports Game Dev Challenge**, under the **Disaster Risk Reduction and Management (DRRM)** theme.

---

## 🎯 Objective
Players act as city planners tasked to protect urban areas from floods. The goal is to build effective defenses, manage a limited budget, and minimize flood damage using environmental and structural interventions.

- Save at least **70% of the city tiles** to complete each level.
- Earn points based on city tiles saved and budget efficiency.

---

## 🧩 Core Features
### 🌍 Procedural Terrain Generation
- Uses **domain-warped fractal Brownian motion (fBm)** for realistic terrain.
- Smooth elevation transitions (inspired by Minecraft-style noise maps).
- Scenario-based terrain shaping:
  - **Riverine Barangay** — Flood from upland river sources.
  - **Coastal Storm Surge** — Water entry from coastline.
  - **Random** — Seeded terrain generation.

### 💧 Water Simulation
- Simplified **shallow-water model** with elevation bias.
- Supports edge drainage — water flows out naturally beyond map boundaries.
- Adjustable **flow style slider** (planned):
  - **Flood-like**: sheet flooding behavior.
  - **Stream-like**: lifelike directional river flow.

### 🏗️ Player Tools
| Tool | Description | Cost (₱) |
|------|--------------|-----------|
| 🧱 Wall/Levee | Raises terrain height, blocks water up to levee height | 800 |
| 🌳 Tree | Improves soil retention and slows flood spread | 300 |
| 🕳️ Canal | Directs water flow; has saturation capacity | 600 |
| 🪓 Erase | Removes placed item (40% refund) | — |

### 📊 Simulation Controls
- **Flood Duration** and **Settle Duration** (2–20 sec each)
- **Flood Strength** (1–8)
- **Spawn Side**: North, South, East, West
- **Levee Height** (1–5)
- **Flow Blend Slider** *(upcoming feature)*: Adjusts between flood-like and stream-like flow.

### 🎮 Game Loop
1. Generate map based on selected scenario and seed.
2. Player places defensive structures within a limited budget.
3. Start simulation — flood progresses for a timed duration.
4. Game evaluates performance:
   - City tiles saved
   - Budget spent
   - Score computed
5. Result modal appears — **Level Complete** or **Level Failed**.

---

## 🧱 Technical Implementation
| Component | Technology |
|------------|-------------|
| Rendering | HTML5 Canvas (Isometric 2D) |
| Language | JavaScript (single-file) |
| UI Styling | CSS3, custom theme |
| Procedural Terrain | Perlin Noise + Domain Warping (Quílez technique) |
| Water Physics | Simplified gradient descent model |
| Storage | URL parameters (seed, scenario) for reproducibility |

---

## 🧠 Educational Value
This game promotes **climate literacy** and **environmental responsibility**, reflecting Filipino values of **resilience** and **preparedness**. It aligns with:
- **UN SDG 11:** Sustainable Cities and Communities
- **UN SDG 13:** Climate Action

### Learning Outcomes
- Understanding flood dynamics and terrain influence.
- Decision-making under resource and time constraints.
- Awareness of eco-friendly and structural DRRM strategies.

---

## 🧾 Scoring System
| Metric | Description |
|---------|--------------|
| **City Tiles Saved** | Number of protected cells during flood simulation |
| **Budget Efficiency** | Lower spending increases bonus points |
| **Final Score** | = (Saved Tiles × 250) − (Spent × 0.2) |

Players pass a level if **≥ 70% of city tiles** remain dry.

---

## 🎨 Visual Style
- **Perspective:** Isometric 2.5D
- **Palette:** Earth tones for land, blue gradients for water, green city tiles.
- **Canals:** Magenta/purple outlines for visibility.
- **Low-poly minimalistic style** to emphasize educational clarity.

---

## 🧪 Testing and Debug Tools
- Built-in **🧪 Run Tests** button validates:
  - Canvas readiness
  - Element existence
  - Terrain smoothness heuristic
  - Isometric coordinate accuracy

---

## 🚀 How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/drrm-city.git
   ```
2. Navigate to the project folder:
   ```bash
   cd drrm-city
   ```
3. Open the HTML file in your browser:
   ```bash
   open index.html
   ```
   *(or drag-and-drop into Chrome/Edge)*

---

## 🔮 Future Plans
- Add **flow-style slider** (flood ↔ stream behavior)
- Refine **canal overflow** and **terrain erosion**
- Add **AI-assisted terrain design** (river routing)
- Leaderboards and scenario sharing
- Mobile-friendly UI

---

## 👥 Developers
**Project Lead:** [Your Name]  
**Affiliation:** College of Computer Studies  
**Mentor:** [Faculty Coach Name]  
**Competition:** DOST Level Up: Esports Game Dev Challenge 2025

---

## 📄 License
This project is open-source under the **MIT License**.

---

> *“Disaster readiness through simulation — building smarter, safer Filipino cities.”*
