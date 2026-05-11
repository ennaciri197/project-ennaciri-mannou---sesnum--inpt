# PROJECT-ENNACIRI-MANNOU---SESNUM--INPT
# Temperature Dashboard

## Project Overview 

The Temperature Dashboard is a real-time monitoring system that displays the evolution of temperature in a room using a web interface.

A temperature sensor continuously measures the room temperature and sends the data to a Raspberry Pi acting as a server. The server processes, stores, and organizes the data in a database, allowing the system to visualize temperature changes over time using graphs.

---

## System Architecture

The system is composed of three main parts:

### Temperature Sensor (IoT device)
- Continuously measures room temperature  
- Sends data to the Raspberry Pi  

### Raspberry Pi (Server)
- Receives sensor data  
- Stores values in a database  
- Processes data for visualization  

### Web Dashboard
- Displays real-time temperature  
- Shows historical data using graphs  
- Provides organized visualization of temperature evolution  

---

## Features

- Real-time temperature display  
- Continuous data collection  
- Data storage in a database  
- Graphical visualization of temperature evolution  
- Clean and organized dashboard interface  
- Historical temperature tracking  

---

## Important Note

This project is monitoring-only:

The web interface does not control any device.  
It is only used to observe and analyze temperature evolution in a structured and visual way.

---

## Technologies Used (Planned)

- Raspberry Pi  
- Temperature sensor (DHT11)  
- Python (backend)  
- SQLite / MySQL (database)  
- HTML / CSS / JavaScript (frontend)  
- Chart.js (graphs)

---

## Data Flow

1. Temperature sensor reads data  
2. Data is sent to Raspberry Pi  
3. Server stores data in database  
4. Web dashboard requests data  
5. Graphs are generated and displayed  

---

## Objective

The goal of this project is to build a simple IoT monitoring system that allows users to:

- Monitor room temperature in real time  
- Analyze historical temperature data  
- Visualize data using graphs  

---

## Team Members

- ENNACIRI ABDERRAHIM  
- MAROUAN MANNOU 

---

## Future Improvements

- Add humidity monitoring  
- Add alert system for extreme temperatures  
- Improve graph interactivity    
 
