# AI Travel Planner Agent ✈️🤖

An AI-powered travel planning assistant built using *Flask* and *IBM WatsonX*.  
Users enter travel preferences such as *destination, **number of days, **budget, and **interests*, and the system generates a personalized day-wise travel itinerary.

This project is designed as a backend service that can be connected to any web or mobile frontend.

---

## 🧩 Problem Statement

Planning a trip manually is time-consuming:
Searching places to visit
Choosing what to do each day
Balancing time, cost, and interests

The *AI Travel Planner Agent* automates this by using a *large language model (IBM WatsonX Granite)* to create human-like travel plans in a few seconds.

---

## ✨ Features

*Intelligent Itinerary Generation*
  Takes user input (destination, days, preferences) and generates a structured plan.

*IBM WatsonX Granite-13B Integration*
  Uses IBM’s Granite chat model for high-quality, natural language responses.

*Flask-based REST API*
  Easy to plug into any UI (web app, mobile app, or chatbot).

*Secure Configuration via .env*
  API keys and sensitive values are never hard-coded.

*JSON Responses*
  Travel plan is returned in a clean JSON format that the frontend can render nicely.

*Extensible*
  Can be extended to include hotel suggestions, transport options, and cost estimates.

---

## 🧠 Tech Stack

*Language:* Python
*Web Framework:* Flask
*AI Platform:* IBM WatsonX (Granite LLM)
*Environment Management:* python-dotenv
*HTTP / JSON:* Flask request & response APIs

---

## 🏗️ Project Structure  (example)

```bash
AI-Travel-Agent-Planner/
├── file.py or travel_planner.py   # Main Flask application
├── requirements.txt               # Python dependencies
├── .env                           # Environment variables (NOT committed)
├── templates/                     # (Optional) HTML templates for UI
│   └── index.html
└── README.md
