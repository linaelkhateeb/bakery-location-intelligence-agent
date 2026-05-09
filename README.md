# Bakery Location Intelligence: MCP AI Agent 🥖

[![Google Cloud](https://img.shields.io/badge/Tech-Google_Cloud-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)](https://cloud.google.com/)
[![MCP](https://img.shields.io/badge/Protocol-MCP-green?style=for-the-badge)](https://modelcontextprotocol.io/)
[![Gemini](https://img.shields.io/badge/Model-Gemini_1.5_Pro-blue?style=for-the-badge)](https://deepmind.google/technologies/gemini/)

## Project Overview
This repository features a custom AI Agent built using the **Model Context Protocol (MCP)**. I developed this agent to demonstrate how an LLM (Gemini) can autonomously bridge the gap between static enterprise data and real-world geospatial intelligence.

The agent solves a challenge: **Identifying the optimal location and pricing strategy for a premium sourdough bakery in Los Angeles.**

### The Logic
The agent doesn't just "guess." It performs a series of reasoned steps:
1. **Macro-Discovery:** Queries **BigQuery** to find zip codes with high morning foot traffic.
2. **Competitive Analysis:** Uses **Google Maps** to verify bakery density in those specific areas.
3. **Pricing Strategy:** Analyzes market trends to establish a premium price point (e.g., ~$18 for a sourdough loaf).
4. **Forecasting:** Runs sales projections based on historical data patterns.

---

## Architecture
![Architecture Diagram](architecture_diagram.png)

This project utilizes the **Google ADK (Agent Development Kit)** to orchestrate requests between the user and Google Cloud services via a remote MCP server.

---

## Repository Structure

```text
launchmybakery/
├── adk_agent/           # AI Agent Application (Logic & Tools)
│   └── agent.py         # Main agent definition and prompt logic
├── data/                # Synthetic datasets (Demographics, Prices, Traffic)
├── setup/               # Infrastructure automation (BigQuery & Env setup)
├── .env.example         # Template for required API keys and Project IDs
└── README.md            # Project documentation
