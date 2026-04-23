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
