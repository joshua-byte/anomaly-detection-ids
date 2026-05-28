# AI-Assisted Flow-Based Intrusion Detection System

A real-time network intrusion detection system using **Isolation Forest** for anomaly detection.  
This project captures live traffic, converts packets into flows, and analyzes behavioral patterns to detect suspicious activity.

---

## Features
-  Live packet capture using Scapy  
-  Flow-based traffic analysis (not packet-level)  
-  Anomaly detection using Isolation Forest  
-  Interactive dashboard with Plotly (Streamlit)  
-  Detection of abnormal traffic patterns (e.g., spikes, scans)

---

##  How It Works
1. Capture live network packets  
2. Group packets into flows (based on IP, port, protocol)  
3. Extract statistical features (duration, packet rate, etc.)  
4. Train Isolation Forest on traffic  
5. Detect anomalies and visualize results  

---

##  Run the Project

sudo streamlit run app.py

---

##  Example Use
- Monitor live traffic  
- Simulate attacks (ping flood / port scan)  
- Stop capture → run analysis → view anomalies  

---

##  Tech Stack
- Python  
- Scapy  
- Scikit-learn  
- Streamlit  
- Plotly  

---

##  Note
- Requires **root/sudo** privileges for packet capture  
- Designed for educational and demonstration purposes  

---

## 📌 Future Improvements
- Real-time anomaly alerts  
- Attack classification (DDoS / Scan)  
- Logging & reporting  
