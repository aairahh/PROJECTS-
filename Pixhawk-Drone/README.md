# Autonomous Drone Navigation System — Pixhawk + Raspberry Pi 🚁🛰️

This project demonstrates an *AI-enabled autonomous drone* that executes *GPS-based rescue missions* triggered by SOS alerts received from the *Jeevan Setu Mobile App*.

A Raspberry Pi acts as the *Companion Computer, sending commands to the **Pixhawk Flight Controller* using MAVLink/DroneKit to automatically navigate, drop payloads, and return safely.

This README explains how the drone software works.

---

## 🎯 Purpose of the Code

The code is responsible for:

✔ Receiving GPS coordinates from the SOS app backend  
✔ Creating a mission with waypoints  
✔ Arming and launching the drone automatically  
✔ Flying to the target location  
✔ Activating payload-drop mechanism (servo/winch)  
✔ Returning to Launch (RTL) after mission completion  
✔ Updating mission status back to app  

All without manual pilot control 🚫🕹️

---

## 🧠 Tech Stack & Hardware

| Component | Purpose |
|----------|---------|
| *Raspberry Pi 4* | Runs mission planning Python scripts |
| *Pixhawk PX4 Flight Controller* | Handles autopilot flight operations |
| *MAVLink / DroneKit* | L1 Communication between Pi ↔ Pixhawk |
| *Flask* | Receives SOS request from mobile app |
| *GPS Module* | Mission navigation |
| *Servo Motor* | Payload release mechanism |
| *QGroundControl* | Flight visualization and configuration |

---

## 🔁 System Workflow

```mermaid
sequenceDiagram
Victim ->> App: Press SOS
App ->> Flask Backend: Send GPS Location
Flask ->> Raspberry Pi: Trigger AI Drone Mission
Raspberry Pi ->> Pixhawk: Set Mission Waypoint
Pixhawk ->> Drone Motors: Takeoff & Navigate
Drone ->> Victim: Drop Payload
Drone ->> Base: Return to Launch (RTL)
Raspberry Pi ->> App: Mission Completed Update
