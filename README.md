# Autonomous AI Data Platform

## Overview
Autonomous AI Data Platform is an advanced enterprise-style utility intelligence project that combines PySpark-based feature engineering, anomaly detection, FAISS-powered historical retrieval, AI-generated root-cause explanations, adaptive feedback loops, and Airflow-to-Databricks orchestration.

This project is designed to simulate a next-generation energy and utility AI system where the platform does not just process data, but continuously evaluates and improves its own outputs.

---

## Key Idea
Most data platforms stop after data processing or anomaly detection.

This platform goes further:
- detects abnormal utility patterns
- retrieves similar historical incidents
- generates AI-style root-cause explanations
- evaluates explanation quality and retrieval quality
- updates its own operating thresholds using feedback logic
- supports enterprise orchestration using Airflow and Databricks

---

## Architecture
Airflow (Orchestration)  
→ Databricks / PySpark Processing  
→ Feature Engineering  
→ Hybrid Anomaly Detection  
→ FAISS Vector Retrieval  
→ AI Root-Cause Explanation  
→ Evaluation Layer  
→ Adaptive Feedback Rules

---

## Problem Statement
In utility environments, abnormal behavior such as voltage drops, usage spikes, equipment stress, and outage-related patterns are often difficult to analyze because data is spread across smart meter systems, asset systems, weather feeds, and outage records.

Traditional systems detect anomalies, but they do not explain them well and they rarely improve automatically.

This platform addresses that gap by combining data engineering, anomaly intelligence, retrieval, and self-improving AI logic.

---

## Core Features

### 1. Utility Data Simulation
The project generates realistic interconnected utility datasets:
- smart meter readings
- asset master data
- meter-to-asset mapping
- regional weather data
- outage history
- feedback rule configuration

### 2. PySpark Processing Layer
The Spark pipeline:
- joins meter, asset, and weather datasets
- creates baseline behavior per meter
- derives usage and voltage anomaly indicators
- adds contextual risk hints
- builds retrieval-ready text features

### 3. Hybrid Anomaly Detection
The anomaly layer combines:
- business thresholds
- machine learning anomaly scoring using Isolation Forest

This produces a more realistic anomaly detection strategy than a simple fixed-rule system.

### 4. Historical Incident Retrieval
FAISS is used to:
- index historical outage incidents
- search similar cases for live anomalies
- support AI reasoning with historical context

### 5. AI Root-Cause Explanation
The platform generates business-friendly AI explanations including:
- likely root cause
- recommended action
- confidence level
- historical incident context

### 6. Autonomous Evaluation and Feedback Loop
The platform evaluates:
- explanation quality
- retrieval quality

If quality drops, it updates its own rules and thresholds, making the platform adaptive rather than static.

### 7. Airflow to Databricks Trigger
An Airflow DAG is included to demonstrate enterprise orchestration where:
- Airflow acts as the controller
- Databricks acts as the execution engine

---

## Project Structure

```text
Autonomous-AI-Data-Platform/
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── output/
│
├── vector_store/
│
├── config/
│
├── autonomous_ai_data_platform_airflow_databricks.py
└── notebooks / generated artifacts
