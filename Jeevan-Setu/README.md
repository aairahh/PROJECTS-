# Jeevan Setu — SOS Emergency Communication App 🚑📱

Jeevan Setu is a disaster-response SOS mobile application designed to instantly connect people trapped in remote or calamity-affected areas with rescue drones and emergency teams.

Via a *single SOS tap, the app sends accurate **GPS coordinates* of victims, enabling *AI-powered autonomous drones* to deliver critical supplies like medicines, first-aid kits, food, and water.

This app acts as a *communication bridge* between:
*Victims → Rescue Command Center → Autonomous Drone System*

---

## 🌍 Problem We Solve

In disaster zones:
Roads are destroyed 🚫
Communication infrastructure collapses 📵
Rescue teams struggle to reach victims in time ⏱️

This delay can cost lives.  
Jeevan Setu ensures *immediate communication* and *quick action*.

Victims only need their *smartphone + GPS* to ask for help.

---

## ✨ Key Features

| Feature | Description |
|--------|-------------|
| 📍 One-tap SOS Trigger | Sends emergency alert with live GPS |
| 🛰 Automated Drone Dispatch | Activates AI drone mission via backend |
| 🔄 Mission Status Updates | App shows progress: Sent → Delivered → Returned |
| 👥 Rescue Control Dashboard (future) | For NGOs & responders |
| ⛰ Works in remote terrain | Uses minimal internet |
| 🔐 Secure & private | Location shared *only* in emergencies |

---

## 🧠 System Workflow

```mermaid
graph LR
A[SOS App] --> B{GPS Location Acquired}
B --> C[Send Alert to Backend (Flask)]
C --> D[Raspberry Pi Mission Planner]
D --> E[Pixhawk Flight Controller]
E --> F[Drone Takes Off]
F --> G[Autonomous Payload Delivery]
G --> H[Return to Base]
C --> I[Mission Status Updates to App]
