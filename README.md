# AI-Assisted Flow-Based Intrusion Detection System (IDS)

A real-time flow-based intrusion detection system designed to analyze live network traffic and identify suspicious behavioral patterns using machine learning-driven anomaly detection.

The system captures live packets, aggregates them into network flows, extracts statistical traffic features, and applies Isolation Forest anomaly detection to identify unusual traffic behavior such as abnormal packet bursts, high-throughput communication, and scanning activity.

Built with a detection engineering mindset, the project simulates lightweight SOC-oriented threat analysis workflows by combining behavioral traffic analytics, anomaly scoring, and interactive visualization dashboards.

---

# Features

* Real-time packet capture using Scapy
* Flow-based network traffic analysis
* Isolation Forest anomaly detection pipeline
* Behavioral traffic analytics
* Interactive Streamlit + Plotly dashboard
* Detection of suspicious traffic spikes and abnormal flow activity
* Analyst-oriented suspicious flow inspection
* Statistical feature extraction from live network traffic
* Lightweight SOC-style anomaly triage workflow

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

The IDS operates using a flow-based behavioral analysis pipeline rather than isolated packet inspection.

## 1. Packet Capture

Network packets are captured in real time using Scapy from active network interfaces.

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

An Isolation Forest model analyzes flow behavior and identifies statistical outliers representing potentially suspicious traffic patterns.

## 5. Visualization & Triage

Detected anomalies are visualized through an interactive dashboard to support lightweight SOC-style analysis workflows.

---

# Dashboard Preview

## Detection Analytics Dashboard

![Traffic Behavior Dashboard](sus.png)

The dashboard visualizes:

* Flow duration distributions
* Traffic intensity anomalies
* Packet-rate spikes
* Byte-transfer outliers
* Anomaly classification ratios
* Behavioral traffic patterns

The dashboard is designed to simulate analyst-oriented traffic inspection workflows for anomaly triage and behavioral threat analysis.

---

# Suspicious Flow Analysis

## Top Suspicious Flows



The system surfaces anomalous flows using behavioral indicators such as:

* Extremely high packets-per-second rates
* Unusually large byte-transfer volumes
* Abnormal packet-size distributions
* Sustained burst traffic
* Deviations from baseline flow behavior
* Unusual TCP flag activity

Example behavioral indicators:

* High-throughput burst communication
* Rapid connection spikes
* Abnormal ACK/SYN patterns
* Potential scan-like behavior
* Suspicious flow intensity anomalies

---

# Example Detection Output

<img width="1863" height="351" alt="table" src="https://github.com/user-attachments/assets/bc191d34-b3c3-4502-be6b-b28e7b7a0509" />
<img width="1913" height="889" alt="sus" src="https://github.com/user-attachments/assets/12df2708-1ebe-44c9-8aca-2aed6b14ad2e" />



---

# Simulated Attack Scenarios

The IDS was tested against simulated abnormal traffic conditions including:

* ICMP flood traffic
* Port scanning behavior
* High-frequency packet bursts
* Abnormal connection spikes
* Rapid traffic generation
* Sustained high-throughput flows

These simulations were used to evaluate anomaly visibility and behavioral traffic differentiation.

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

The project is designed as an educational and research-oriented platform for exploring modern network detection workflows.

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

# Run the Project

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
│
├── images/
│   ├── dashboard.png
│   └── suspicious_flows.png
│
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
