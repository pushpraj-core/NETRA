> **Note:** This project was built quickly during a national level hackathon (achieving 3rd rank). The original repository crashed, so it was moved here for presentation purposes. Commit history may be sparse.
# NETRA — Autonomous Pothole Intelligence Platform

> **N**eural **E**ngine for **T**errain **R**ecognition & **A**nalysis

---

![NETRA Logo](https://img.icons8.com/color/96/road.png)

## 🚀 What is NETRA?
NETRA is a real-time, edge-optimized AI platform for detecting, segmenting, measuring, and triaging road potholes and anomalies from dash-cam video, drone footage, and citizen uploads. It combines deep learning, predictive analytics, and interactive web dashboards to transform road safety and maintenance.

---

## 🧠 Core Features

- **Deep Learning Dashcam Pipeline**
  - YOLOv8 instance segmentation for pothole/crack detection
  - MiDaS monocular depth estimation for severity scoring
  - Temporal tracking and repair verification
  - 3D mesh and point cloud export
- **Predictive Early-Warning Engine**
  - Live weather vulnerability index (OpenWeatherMap API)
  - Degradation risk forecasting and ROI metrics
- **Interactive Web Dashboard**
  - React + Vite frontend with live maps, analytics, and citizen portal
  - Persistent AI Copilot (Google Gemini LLM integration)
- **API & Data Sync**
  - Node.js REST API for pothole records, complaint tracking, and CPGRAMS sync
  - MongoDB backend
- **Synthetic Demo Runner**
  - Generate synthetic road frames for end-to-end pipeline testing

---

## 🏗️ Architecture Overview

```
+-------------------+      +-------------------+      +-------------------+
|   Dashcam Video   | ---> |   AI Pipeline     | ---> |   Web Dashboard   |
+-------------------+      +-------------------+      +-------------------+
        |                        |                        |
        v                        v                        v
  YOLOv8 Segmentation   MiDaS Depth Estimation   React + Gemini Copilot
        |                        |                        |
        v                        v                        v
  Temporal Tracking     Severity Scoring         Live Map & Analytics
        |                        |                        |
        v                        v                        v
  GPS Geotagging        Repair Verification      Citizen Portal
        |                        |                        |
        v                        v                        v
  3D Mesh Export        API Sync & Alerts        Complaint Tracker
```

---

## 🏁 Quick Start

1. **Install Python dependencies:**
   ```bash
   pip install -r NETRA-AI/requirements.txt
   ```
2. **Run the AI pipeline on a video:**
   ```bash
   cd NETRA-AI
   python pipeline.py --source ../video/sample.mp4
   ```
3. **Launch the web dashboard:**
   ```bash
   cd netra-web
   npm install
   npm run dev
   ```
4. **Start the API server:**
   ```bash
   cd netra-api
   npm install
   npm start
   ```

---

## 🧩 Project Structure

- **NETRA-AI/** — Python AI pipeline, models, demo scripts
- **netra-web/** — React + Vite frontend, live map, analytics, chatbot
- **netra-api/** — Node.js REST API, MongoDB integration
- **archive/** — CSV datasets for accidents, vehicles, casualties
- **video/** — Sample videos, deep-dive docs

---

## 🌟 Unique Selling Points

- Multi-format ingestion: video, images, citizen uploads
- Automated PDF report generation for contractors
- Proactive asset management with predictive alerts
- Conversational AI Copilot for admin and citizen support
- 3D mesh export for drone micro-scan workflows

---

## 📚 Documentation & Demos

- [Deep Dive Architecture & Features](video/README.md)
- [AI Pipeline Details](NETRA-AI/README.md)
- [Web Dashboard Features](netra-web/README.md)

---

## 🤝 Contributing

We welcome contributions! Please open issues, pull requests, or join our discussion forum for feature requests and bug reports.

---

## 🏆 Credits

- Developed by the NETRA Team
- Powered by YOLOv8, MiDaS, React, Node.js, MongoDB, Gemini LLM

---

> **Ready to make roads safer, smarter, and more resilient? Dive in and run NETRA today!**

---

[![Star](https://img.shields.io/github/stars/netra-ai/netra?style=social)](https://github.com/netra-ai/netra)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
