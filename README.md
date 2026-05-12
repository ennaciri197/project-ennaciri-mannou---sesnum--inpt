# Temperature Dashboard: Real-Time IoT Monitoring System

**Course Assignment** **Team Members:** ENNACIRI ABDERRAHIM & MAROUAN MANNOU

---

##  Project Overview
The **Temperature Dashboard** is a real-time monitoring system designed to display and analyze the evolution of temperature and humidity in a room. 

A DHT11 sensor continuously measures environmental data and sends it to a Raspberry Pi server. The system processes, stores, and organizes this data in a relational database, allowing for structured visualization through a web-based dashboard with real-time graphs.

##  System Architecture
The system follows a modular, containerized architecture composed of three main layers:

1.  **IoT Sensing Layer (DHT11):** * Continuously measures room temperature and humidity.
    * Communicates via GPIO pins to the Raspberry Pi.
2.  **Server & Storage Layer (Raspberry Pi / MariaDB):** * **Python Backend:** Handles raw data acquisition and error correction.
    * **MariaDB Database:** Stores values for historical tracking and analysis.
3.  **Web Dashboard Layer:** * **PHP/Apache:** Bridges the database to the frontend.
    * **JavaScript/Chart.js:** Displays real-time data and historical evolution using interactive graphs.

##  Objective
The goal of this project is to build a robust IoT monitoring system that allows users to:
* **Monitor** room temperature and humidity in real time.
* **Analyze** historical environmental data.
* **Visualize** trends through dynamic, moving-window graphs.

##  Technologies Used
* **Hardware:** Raspberry Pi 3B, DHT11 Sensor.
* **DevOps:** Docker & Docker Compose (Containerization).
* **Backend:** Python 3.11 (CircuitPython/Blinka), PHP 8.2.
* **Database:** MariaDB (optimized for 32-bit ARMv7).
* **Frontend:** HTML5, CSS3, JavaScript (jQuery), Chart.js.

##  Data Flow
1.  **Sensing:** The DHT11 sensor reads ambient data.
2.  **Transmission:** Python script captures data and handles connection retries.
3.  **Storage:** Data is structured and saved in the MariaDB `SensorData` table.
4.  **Retrieval:** The Web Dashboard requests the latest records via AJAX.
5.  **Visualization:** Charts are generated and updated every 5 seconds.

##  Features
* **Real-time display:** Immediate visualization of current readings.
* **Continuous collection:** Automated data gathering without manual intervention.
* **Historical tracking:** View data evolution over time.
* **Clean Interface:** Organized and responsive dashboard for easy observation.

##  Important Note
This project is **monitoring-only**. The web interface is used solely to observe and analyze temperature evolution in a structured way; it does not control external hardware or cooling/heating devices.

---

##  Project Structure
```text
dht_dashboard/
├── docker-compose.yml         # Container orchestration
├── db_init/
│   └── init.sql               # Database schema
├── sensor/
│   ├── Dockerfile             # Hardware drivers & Python environment
│   └── collect.py             # Data acquisition script
└── web_root/
    ├── Dockerfile             # Web server & PHP extensions
    ├── index.html             # Chart.js frontend
    └── data.php               # Database bridge
