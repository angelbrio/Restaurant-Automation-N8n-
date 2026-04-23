# 🍽️ AI-Powered Restaurant Inventory & Ordering Automation (n8n)

> End-to-end automation system that simulates restaurant orders, manages inventory in real-time, and predicts supplier orders using AI.

---

## 🚀 Overview

This project demonstrates a **fully automated restaurant workflow** built with **n8n**, integrating:

- 📲 Simulated order intake (Webhook / HTTP)
- 🧾 Recipe processing
- 📦 Real-time inventory management (Airtable)
- 🧠 AI-driven purchase prediction (OpenAI)
- 📊 Historical tracking of orders

The system mimics how a real restaurant backend could operate — from order intake to stock management and intelligent restocking decisions.

---

## 🧠 Key Features

### 🔹 1. Order Simulation (Webhook API)
- Receives incoming orders via HTTP (simulating a PDA / POS system)
- Example payload:
```json
{
  "id_comanda": "CMD-001",
  "plato": "Ensalada",
  "cantidad": 1
}
```

 ### 🔹 Order Intake (Webhook API)
 Maps dishes into ingredients and consumption.
 Dish | Ingredients

Ensalada | Lechuga (1), Tomate (2), Atún (1)

Pasta | Pasta (1), Atún (1)

 ### 🔹 Order Intake (Webhook API)
Inventory Management (Airtable)
* Automatically deducts ingredients from stock
* Ensures real-time synchronization
Example table:

Ingrediente | Cantidad

Lechuga 500

Tomate 400

Atún 300

 ### 🔹 Historical Tracking
 Stores all orders for analytics and forecasting.
 Plato | Cantidad | Fecha

Ensalada | 1 | …

 ### 🔹 AI-Based Purchase Prediction 🤖
 Uses OpenAI to determine how much stock should be reordered.
 Inputs:

* Current stock
* Consumption rate
* Order history
* Seasonal context

Output example:
```json
{
  "cantidad_a_anadir": 2,
  "motivo": "Stock is low and demand is expected to increase"
}
```
### ⚙️ System Architecture
graph TD
    A[HTTP Request Simulator] --> B[Webhook]
    B --> C[Recipe Engine]
    C --> D[Stock Update]
    C --> E[Historical Storage]
    D --> F[AI Prediction]
    F --> G[Order Update]

### 🔄 Workflows
## 🟦 Main Workflow (Production)
Webhook → Recipe → Stock → History → AI → Order Update
## 🟩 Simulator Workflow (Testing)🟩 Simulator Workflow (Testing)
Manual Trigger → HTTP Request → Webhook

### 🧩 Tech Stack
* ⚡ n8n → Workflow automation
* 🧠 OpenAI API → AI decision making
* 🗂️ Airtable → Database
* 🌐 HTTP/Webhooks → Integration layer







 
