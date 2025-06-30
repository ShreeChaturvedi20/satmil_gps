# 🚁️ SatMil GPS: Satellite & Drone Tactical Routing Simulation

**SatMil GPS** is a simulation platform that models satellite-based navigation and drone control in **military environments** with potential **GNSS jamming**, **fallback routing**, and **real-time telemetry visualization**.

Built using:

* 🧠 Python (DSA: Graph Algorithms)
* 🎮 PyQt6 GUI
* 🧵 ROS 2 (GNSS, jamming, drone control nodes)
* 🗌 Battlefield maps via CSV
* 📊 Telemetry & analytics logging

---

## 🌍 Use Case

This project simulates **tactical battlefield routing** where:

* Satellites provide GPS coordinates
* Drones must navigate across nodes
* **Jamming zones** trigger alternate routes
* GUI dashboard visualizes drone position, signal health, route efficiency

---

## 🏗️ System Architecture

```
ROS 2 Nodes (GPS + Jamming)
       ↓
 [Routing Manager]
       ↓
Backend (Graph Engine: Dijkstra / A*)
       ↓
Frontend (PyQt6 GUI Dashboard)
       ↓
Analytics & Logs
```

---

## 📂 Project Structure

```
satmil_gps/
├── app.py                      # Main launcher
├── mission_sim.py             # Simulation orchestrator
├── README.md                  # This file
├── requirements.txt           # Dependencies

├── backend/                   # Core routing and jamming logic
│   ├── graph_engine.py
│   ├── routing_manager.py
│   ├── telemetry_queue.py
│   └── jamming_simulation.py

├── frontend/                  # PyQt6 GUI components
│   ├── ui_main.py
│   ├── map_window.py
│   ├── dashboard_panel.py
│   └── style.qss

├── data/                      # Battlefield map, units, logs
│   ├── battlefield_map.csv
│   ├── satellites.json
│   ├── units.csv
│   └── logs/
│       ├── signal_log.csv
│       └── route_history.json

├── models/                    # CAD models (CanSat, CubeSat)
│   └── flight_dynamics.pdf

├── analytics/                 # Route efficiency and signal metrics
│   ├── performance_metrics.py
│   └── signal_health.py

├── tests/                     # Unit and functional tests
│   ├── test_graph_engine.py
│   └── test_ui_responsiveness.py

└── docs/                      # Presentation and reports
    ├── project_report.pdf
    └── presentation.pptx
```

---

## 🚀 Quick Start

### 🔧 Requirements

* Python 3.9+
* ROS 2 (Humble/Foxy)
* PyQt6, pandas, networkx, matplotlib

### ⚙️ Installation

```bash
git clone https://github.com/your-username/satmil_gps.git
cd satmil_gps
pip install -r requirements.txt
```

---

### ▶️ Run Simulation (Standalone)

```bash
python app.py
```

You will see:

* A PyQt6 window with route status
* Terminal output with current path
* Simulation of jamming + fallback routing

---

### 🚁️ ROS 2 Integration (Optional)

```bash
# Source your ROS 2 workspace
source ~/satmil_gps_ws/install/setup.bash

# Run GPS simulator node
ros2 run gps_simulator gps_simulator_node.py

# Run drone controller node
ros2 run drone_control drone_controller_node.py
```

---

## 📊 Logs & Analytics

All signal drops, telemetry, and route changes are logged in:

```
data/logs/signal_log.csv
data/logs/route_history.json
```

You can visualize metrics using the analytics module.

---

## 🎓 Skills Demonstrated

* Graph Algorithms (Dijkstra/A\*)
* ROS 2 Nodes & Communication
* PyQt6 GUI Development
* Military Navigation & Jamming Simulation
* Modular Software Architecture
* Git & Test-driven Development

---

## 📜 License

MIT License – free to use, modify, and distribute with credit.

---

## ✉️ Contact

**Author**: *\[SHREE CHATURVEDI]*
📧 *[shreechaturvedi2004@gmail.com](mailto:shreechaturvedi2004@gmail.com)*\\
