# Threat-Intelligence-Aggregator-Dashboard-with-AI-Powered-Threat-Monitoring-System
This project is a prototype Threat Intelligence Dashboard that gathers cyber threat data, applies NLP for analysis, predicts future risks, and visualizes results in an interactive dashboard.
Here’s a **complete report** on your project files (`threat_aggregator.py`, `readme.md`, and `Untitled-1.html`):

---

# 📄 Threat Intelligence Aggregator – Report

## 1. Project Overview

The **Threat Intelligence Aggregator** is a hackathon project (Sep 13, 2025) designed to **collect, analyze, and visualize cyber threat intelligence** from multiple sources. It demonstrates how cybersecurity data can be automatically aggregated, processed with NLP, and forecasted using predictive models.

The solution produces:

* **Console logs**: fetched threats, extracted entities, and forecasts.
* **dashboard.html**: an interactive dashboard with charts and threat summaries.
* **README.md**: documentation with setup and usage instructions.
* **threat\_aggregator.zip**: packaged project files.

---

## 2. Components

### a) **threat\_aggregator.py**&#x20;

This is the main script. It contains four major stages:

1. **Data Collection**

   * **AlienVault OTX Pulses** (if API key is provided).
   * **RSS Feeds** (from *Krebs on Security*).
   * **Mock X (Twitter) posts** representing cyber trends in 2025.
   * Collects up to 15 recent threats.

2. **NLP Processing**

   * Uses **spaCy** (`en_core_web_sm`) to extract named entities (e.g., organizations, countries, groups).
   * Summarizes each threat description into 1–2 sentences.

3. **Trend Prediction**

   * Uses **ARIMA time-series forecasting** to predict cyber threats for the next **7 days**.
   * Risk levels (Low, Medium, High) are assigned based on thresholds.

4. **Visualization & Output**

   * Generates a **dashboard** with:

     * Bar chart: Threats by Sector.
     * Line chart: 7-Day Threat Forecast.
     * Table of recent threats + extracted entities.
   * Saves results as:

     * `dashboard.html` (interactive dashboard).
     * `README.md` (documentation).
     * `threat_aggregator.zip` (all files).

---

### b) **readme.md**&#x20;

Provides documentation:

* **Overview** – Aggregates threat data from OTX, RSS, and mock X posts. Uses spaCy, ARIMA, and Plotly.
* **Setup Instructions** – Install dependencies, download spaCy model, set `OTX_API_KEY`, and run script.
* **Outputs** – Console logs, interactive dashboard, zip package.
* **Resources** – External link for developer deals (Dealsbe).
* **Notes** – Python 3.8+ required, works online/offline (mock data fallback).
* **Last updated:** Sep 13, 2025.

---

### c) **dashboard.html**&#x20;

This is the generated **interactive threat dashboard**, containing:

1. **Threats by Sector** (bar chart):

   * Finance: 1
   * General: 4
   * Healthcare: 1
   * IoT: 1

2. **Recent Threats Table**
   Examples:

   * *AI Phishing Surge #CyberSec* – Deepfake phishing targeting banks (Finance).
   * *IoT Zero-Day Alert* – APT28 exploiting smart cameras (IoT).
   * *Ransomware Hits Healthcare* – 25% increase in attacks (Healthcare).

   Total threats fetched: **15**, with **General** as the top sector.

3. **7-Day Forecast (ARIMA model)**

   * Predicted daily threats range from **18.0 → 17.4**, labeled as **High risk**.

---

## 3. Key Features

* ✅ **Multi-source aggregation** (OTX, RSS, social media).
* ✅ **Natural Language Processing** for entity extraction.
* ✅ **Predictive modeling** (ARIMA for trend forecasts).
* ✅ **Interactive visualization** with Plotly (bar + line charts).
* ✅ **Export & packaging** (zip, dashboard, README).
* ✅ **Hackathon-ready MVP** – can run offline with mock data.

---

## 4. Strengths

* Simple, modular Python script.
* Works with/without API keys (flexible for demos).
* Uses modern libraries: `spaCy`, `pandas`, `statsmodels`, `plotly`.
* Auto-generates documentation and dashboard.

---

## 5. Limitations

* OTX integration depends on a valid **API key**.
* RSS parsing limited to **Krebs on Security** only.
* Mock X posts are **not live data** (static examples).
* Forecast is based on **mock counts**, not real threat volume.
* No database support – data isn’t stored historically.

---

## 6. Future Improvements

* 🔹 Add real-time Twitter/X API integration.
* 🔹 Expand RSS feeds (e.g., CERT, CISA, ThreatPost).
* 🔹 Store historical threat data in a **database**.
* 🔹 Improve forecasting with **LSTM or Prophet**.
* 🔹 Add authentication & role-based access for multi-user use.
* 🔹 Deploy as a **web app** (Flask/Django + hosted dashboard).

---

## 7. Conclusion

The **Threat Intelligence Aggregator** is a functional MVP for cybersecurity monitoring. It aggregates threat data from multiple sources, applies NLP for context, predicts short-term threat activity, and provides an interactive dashboard for quick insights. While currently built for hackathon/demo use, it has potential to evolve into a production-grade **Threat Intelligence Platform (TIP)** with enhancements.


