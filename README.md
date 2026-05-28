# AI-Assisted Flow-Based Intrusion Detection System (IDS)

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Scapy](https://img.shields.io/badge/Scapy-Networking-green)
![Streamlit](https://img.shields.io/badge/Streamlit-Dashboard-red)
![Machine Learning](https://img.shields.io/badge/ML-IsolationForest-orange)
![Status](https://img.shields.io/badge/Status-Active-success)

A real-time flow-based intrusion detection system designed to analyze live network traffic and identify suspicious behavioral patterns using machine learning-driven anomaly detection.

The system captures live packets, aggregates them into network flows, extracts statistical traffic features, and applies Isolation Forest anomaly detection to identify unusual traffic behavior such as abnormal packet bursts, high-throughput communication, and scanning activity.

Built with a detection engineering mindset, the project simulates lightweight SOC-oriented threat analysis workflows by combining behavioral traffic analytics, anomaly scoring, and interactive visualization dashboards.

---

# Features

* Real-time packet capture using Scapy
* Flow-based traffic analysis
* Isolation Forest anomaly detection pipeline
* Behavioral traffic analytics
* Interactive Streamlit + Plotly dashboard
* Suspicious flow inspection and anomaly triage
* Statistical feature extraction from live traffic
* Lightweight SOC-style workflow simulation
* Detection of abnormal traffic spikes and burst behavior
* Analyst-oriented anomaly visualization

---

# Why Flow-Based Detection?

Traditional packet-level inspection can become noisy and computationally expensive in dynamic network environments.

This project focuses on flow-based behavioral analysis to:

* identify anomalous communication patterns,
* detect suspicious traffic behavior over time,
* reduce dependence on static signatures,
* and support scalable anomaly-oriented monitoring workflows.

Flow-based analytics allow the IDS to capture behavioral relationships between packets rather than treating packets as isolated events.

---

# Detection Pipeline

```text
Live Packet Capture
        ↓
Flow Aggregation
        ↓
Feature Extraction
        ↓
Isolation Forest Analysis
        ↓
Anomaly Scoring
        ↓
Visualization Dashboard
        ↓
Suspicious Flow Inspection
```

---

# System Architecture

The IDS operates using a behavioral flow-analysis pipeline rather than isolated packet inspection.

## 1. Packet Capture

Network packets are captured in real time using Scapy from active interfaces.

## 2. Flow Aggregation

Packets are grouped into logical communication flows using:

* Source IP
* Destination IP
* Source Port
* Destination Port
* Protocol
* Session timing

## 3. Feature Engineering

The system extracts behavioral traffic statistics including:

* Flow duration
* Total packets
* Total bytes
* Packets per second
* Bytes per second
* Average packet size
* Packet size variance
* SYN / ACK / FIN activity

## 4. Anomaly Detection

An Isolation Forest model analyzes network-flow behavior and identifies statistical outliers representing potentially suspicious traffic activity.

## 5. Visualization & Triage

Detected anomalies are visualized through an analyst-oriented dashboard to support lightweight SOC-style traffic inspection and anomaly triage workflows.

---

# Dashboard Preview

## Detection Analytics Dashboard

<img width="1913" height="889" alt="dashboard" src="https://github.com/user-attachments/assets/0a3b4da0-fa7e-4db9-a093-609bb9a01350" />


The dashboard provides real-time behavioral traffic analytics for anomaly-oriented monitoring workflows.

Visualizations include:

* flow duration distributions,
* traffic intensity analysis,
* anomaly ratios,
* and byte-versus-packet outlier detection.

The interface is designed to simulate lightweight SOC-style traffic inspection and anomaly triage workflows.

---

# Suspicious Flow Analysis

## Top Suspicious Flows

<img width="1863" height="351" alt="suspicious" src="https://github.com/user-attachments/assets/b178f9fc-b5e3-4e39-a845-bc9080fddaa5" />


The suspicious flow analysis module surfaces statistically anomalous network flows using behavioral traffic indicators such as:

* abnormal packet throughput,
* unusually large byte-transfer volumes,
* high packets-per-second activity,
* sustained burst communication,
* and irregular TCP communication patterns.

This enables analyst-oriented inspection of potentially malicious or abnormal network behavior.

---

# Example Detection Output

```bash
[ALERT] Potential Anomalous Flow Detected

Source IP: 192.168.1.15
Destination IP: 192.168.1.1
Flow Duration: 4.99s
Packets/sec: 2020.83
Bytes/sec: 4262951.38
Anomaly Score: -0.42
Classification: Suspicious Burst Activity
```

---

# Simulated Attack Scenarios

The IDS was tested against simulated abnormal traffic conditions including:

* ICMP flood traffic
* Port scanning behavior
* High-frequency packet bursts
* Abnormal connection spikes
* Rapid traffic generation
* Sustained high-throughput communication

These simulations were used to evaluate anomaly visibility and behavioral traffic differentiation.

---

# Security Relevance

This project explores practical concepts used in:

* detection engineering,
* SOC monitoring,
* anomaly-based intrusion detection,
* behavioral traffic analytics,
* and AI-assisted network defense systems.

The workflow aligns with modern defensive-security approaches focused on behavioral anomaly identification rather than purely signature-based detection.

---

# Detection Engineering Focus

This project focuses on:

* Behavioral traffic analysis
* Anomaly-based intrusion detection
* Lightweight SOC-oriented workflows
* Flow-level threat analytics
* Statistical anomaly detection
* AI-assisted security analytics
* Detection engineering experimentation

The platform is intended as an educational and research-oriented environment for exploring modern network-detection workflows.

---

# Tech Stack

## Languages & Frameworks

* Python

## Networking & Traffic Analysis

* Scapy

## Machine Learning

* Scikit-learn (Isolation Forest)

## Visualization

* Streamlit
* Plotly

## Data Processing

* Pandas
* NumPy

---

# Installation

## Clone Repository

```bash
git clone https://github.com/joshua-byte/Anomaly-Detection-IDS.git
cd Anomaly-Detection-IDS
```

## Install Dependencies

```bash
pip install -r requirements.txt
```

## Run IDS Dashboard

```bash
sudo streamlit run app.py
```

---

# Project Structure

```text
Anomaly-Detection-IDS/
│
├── app.py
├── capture.py
├── features.py
├── model_utils.py
├── visualization.py
├── logs.csv
└── README.md
```

---

# Future Improvements

* Real-time alert streaming
* Threat classification models
* SIEM integration
* Multi-model anomaly detection
* Adaptive threshold tuning
* Distributed traffic monitoring
* ATT&CK-aligned event categorization
* Detection rule correlation
* Automated reporting pipeline
* Real-time network alert notifications

---

# Educational Disclaimer

This project is intended for:

* cybersecurity education,
* detection engineering experimentation,
* behavioral traffic analytics research,
* and defensive security learning purposes only.

The system should only be deployed in authorized and controlled environments.

---

# Author

Joshua Jesuraj Sanctus

Cybersecurity • Detection Engineering • VAPT • AI-Assisted Threat Analytics
