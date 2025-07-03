# 🚁️ SatMil GPS: Satellite & Drone Tactical Routing + AI Terrain Detection Simulation

**SatMil GPS** is a simulation platform for modeling satellite-based drone navigation and tactical decision-making in **military** and **disaster relief** environments. It simulates **GNSS jamming**, **fallback routing**, **telemetry**, and now includes **AI/ML-based feature detection** from multi-source satellite imagery.

---

## 🎯 Project Objective

SatMil GPS is designed to simulate real-time satellite and drone navigation in GNSS-contested or high-risk environments. The project supports tactical decision-making with fallback routing, AI-driven terrain feature extraction, and signal resilience analytics — applicable to both **military operations** and **disaster relief** (e.g., **flooded urban zones**, **glacial outburst detection**, and **inaccessible terrains**).

---

## 🚀 Features

* 🛰️ **Graph-based routing engine** with fallback under jamming
* 🎮 **PyQt6 GUI dashboard** to visualize paths, status, and telemetry
* 🧠 **AI/ML detection** of glacial lakes, roads, and urban drainage from satellite imagery
* 📡 **Telemetry + signal logging** for signal strength and mission history
* 📈 Performance analytics for route health, latency, and dropouts
* 🔁 ROS 2 (optional) integration for GNSS & drone node communication

---

## 🌍 Use Cases

* Tactical battlefield drone routing
* GNSS signal jamming and fallback testing
* Satellite-assisted terrain intelligence
* AI-driven geospatial mapping
* **Disaster relief operations** (e.g., flood zone routing, blocked urban paths)

---

## 🏗️ System Architecture

```
Satellite Imagery → [AI/ML Detector]
                          ↓
Geo Features → [Graph Generator / Map Updater]
                          ↓
Backend Routing Engine → GUI Dashboard
                          ↓
Telemetry Logger + Analytics
```

---

## 📂 Project Structure

```
satmil_gps/
├── app.py                      # Main launcher
├── mission_sim.py             # Simulation orchestrator
├── requirements.txt           # Dependencies
├── README.md                  # This file

├── backend/                   # Core simulation logic
│   ├── graph_engine.py        # Dijkstra/A*, graph construction
│   ├── jamming_simulation.py # Jamming zone logic
│   ├── routing_manager.py    # Manages routing logic
│   └── telemetry_queue.py    # Signal logging system

├── frontend/                  # PyQt6 GUI
│   ├── ui_main.py             # Main dashboard
│   ├── map_window.py          # Map viewer
│   ├── dashboard_panel.py     # Status panel
│   └── style.qss              # UI styling

├── data/                      # Input/output data
│   ├── battlefield_map.csv    # Terrain graph
│   ├── satellites.json        # Satellite positions
│   ├── units.csv              # Troop positions
│   └── logs/
│       ├── signal_log.csv
│       └── route_history.json

├── analytics/                 # Metrics & evaluation
│   ├── performance_metrics.py
│   └── signal_health.py

├── models/                    # CAD models, dynamics
│   ├── cansat.SLDPRT
│   ├── cubesat.SLDPRT
│   └── flight_dynamics.pdf

├── tests/                     # Testing
│   ├── test_graph_engine.py
│   └── test_ui_responsiveness.py

├── ai_module/                 # AI/ML Feature Detection
│   ├── detect_features.py     # Runs segmentation / model inference
│   ├── generate_graph.py      # Converts detections into map/graph
│   └── pretrained_models/     # Folder for ML weights

└── docs/                      # Docs and report
    ├── project_report.pdf
    ├── presentation.pptx
    └── system_architecture.drawio
```

---

## ⚙️ Installation & Setup

### Requirements:

* Python 3.9+
* `networkx`, `pandas`, `PyQt6`, `matplotlib`
* (Optional for AI): `torch`, `opencv-python`, `rasterio`, `geopandas`

### Setup

```bash
git clone https://github.com/your-username/satmil_gps.git
cd satmil_gps
python -m venv venv
source venv/bin/activate      # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

---

## ▶️ Run Simulation (CLI or GUI)

```bash
python mission_sim.py   # For CLI simulation
python app.py           # For GUI dashboard
```

You will see the GUI displaying:

* Route from source to target
* Logs for fallback if jamming is triggered
* Signal strength per node (telemetry)

---

## 🤖 AI Feature Detection (Optional)

```bash
python ai_module/detect_features.py --image_path="input/satellite.png"
python ai_module/generate_graph.py --mask="output/mask.png"
```

Outputs a new battlefield map CSV that is used for routing.

Example: AI detects **flooded zones** in urban satellite images, and the generated graph avoids those nodes in pathfinding.

---

## 📊 Logs & Analytics

Output files:

* `data/logs/signal_log.csv`
* `data/logs/route_history.json`

Use `analytics/` scripts to generate stats on signal loss, dropouts, fallback success.

---

## 🧠 Skills Demonstrated

* Graph Algorithms (Dijkstra/A\*)
* PyQt6 GUI Programming
* ROS 2 nodes (optional)
* Geospatial AI from satellite imagery
* Signal health and telemetry analysis
* Test-driven Python development

---

## 📜 License

MIT License – free to use, modify, and distribute with attribution.

---

## ✉️ Contact

**Author**: *Shree Chaturvedi*
📧 *[shreechaturvedi2004@gmail.com](mailto:shreechaturvedi2004@gmail.com)*
🌐 GitHub: `https://github.com/`Shreechaturvedi20

---

Ready to simulate satellite-routing and build AI-powered terrain systems!

