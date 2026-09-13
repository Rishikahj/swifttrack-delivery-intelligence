# 🚚 SwiftTrack — AI-Powered Delivery Performance & Cost Intelligence

Analyzes e-commerce delivery data to identify SLA breach patterns, quantify their estimated cost impact, and generate an AI-written daily ops brief — turning raw delivery data into a business-ready recommendation.

## 📸 Dashboard

[![SwiftTrack Dashboard](dashboard_screenshot.png)](dashboard_screenshot.png)

## 🎯 Business Problem

E-commerce logistics teams often only discover delivery delays after a customer complains, and rarely quantify what those delays actually cost the business. This project identifies delay hotspots early and estimates their business impact — before it reaches the customer.

## 🛠️ Tools

| Tool | Purpose |
|---|---|
| Python (Pandas) | Data cleaning, delay calculation, aggregation |
| SQL | State-level delay hotspot analysis |
| Power BI | Delay rate, cost impact, and AI-brief visualization |
| Groq API (Llama 3.3) | Auto-generated plain-language daily ops brief |

## 📁 Dataset

[Olist Brazilian E-Commerce Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) (Kaggle, public) — 96,000+ orders with promised vs. actual delivery dates across Brazilian states.

## ⚙️ What It Does

- Calculates delivery delay (promised vs. actual date) across 96,000+ orders
- Identifies delay hotspots by Brazilian state using SQL-style aggregation
- Estimates cost at risk from late deliveries
- Integrates the Groq API (LLM) to auto-generate a plain-language daily ops brief
- Visualizes delay rates, cost impact, and the AI brief in a Power BI dashboard

## 🔍 Key Findings

- **Alagoas, Maranhão, and Sergipe had the highest delivery delay rates** — 21.4%, 17.4%, and 15.2% respectively
- An estimated **$98,592 in cost at risk** from late deliveries across the full dataset, concentrated in 6,534 late orders
- Delay rates vary sharply by state, meaning a single national SLA policy under-serves high-risk regions and over-corrects for low-risk ones
- The AI-generated ops brief converts raw delay/cost numbers into a same-day, plain-language summary — closing the gap between "data exists" and "someone acts on it"

## 💡 Business Recommendations

1. Prioritize logistics partner audits in Alagoas, Maranhão, and Sergipe — the three highest delay-rate states
2. Set state-specific SLA buffers instead of one national delivery promise, since delay risk varies 3x+ across regions
3. Route the daily AI-generated ops brief directly to the logistics team each morning so delay hotspots are visible before customer complaints arrive
4. Flag orders in high-delay states for proactive customer communication (e.g. "your order may arrive later than expected") to reduce complaint volume
5. Track cost-at-risk as a recurring metric, not a one-time report, to measure whether interventions actually reduce the dollar impact over time
