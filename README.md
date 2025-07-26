
# 📊 TRAI Telecom QoS Simulation Dashboard (Python + Streamlit)

This project is a **simulation-based Quality of Service (QoS) analytics dashboard** developed using **Python and Streamlit**, designed during my internship at the **Telecom Regulatory Authority of India (TRAI)** under the **Regional Office – QoS Department**.

The dashboard simulates real-time telecom performance metrics (KPIs) such as **CSSR, DCR, Jitter, MOS**, etc., across various telecom providers and regions. It was created to demonstrate how drive test data can be digitally visualized, analyzed, and reported for monitoring telecom service quality.

---

## 🧭 Objective

To develop a scalable, visual, and easily understandable simulation of **real-time network QoS** using either:
- 📄 Actual KPI data from TRAI Independent Drive Test (IDT) reports
- 🔁 Synthetic/random KPI streams for demo/testing

This dashboard helps in understanding:
- Which operator is underperforming in which region
- Where threshold violations (poor network conditions) occur
- How KPIs vary across urban, rural, highway, and hotspot zones

---

## 🎯 Features

✅ Simulate and visualize key KPIs:
- **Call Setup Success Rate (CSSR)**
- **Call Drop Rate (DCR)**
- **Call Setup Time (CST)**
- **Jitter**
- **Mean Opinion Score (MOS)**
- **Handover Success Rate (HSSR)**  
- **Packet Loss, Latency, Throughput (optional)**

✅ Detection of poor performance using TRAI-defined thresholds  
✅ Operator-wise and region-wise visualization  
✅ Real-time graphs and dynamic bar charts using Streamlit  
✅ Modular architecture for future data integration (MQTT, REST, ESP32, etc.)

---

# 📊 TRAI Telecom QoS Simulation Dashboard

This project simulates and visualizes **telecom network Quality of Service (QoS)** using Python and Streamlit. It was developed during my internship at **TRAI (Regional Office – QoS Department)** to demonstrate real-time monitoring of key KPIs like **CSSR**, **DCR**, and **Jitter** across multiple telecom providers and regions.

---

## 📄 Key Files

- **`app.py`**  
  The main Streamlit dashboard script. It loads the KPI data, displays charts, and shows alerts for poor network conditions.

- **`data_generator.py`**  
  Generates simulated QoS data (CSSR, DCR, etc.) for multiple operators and locations, useful when real TRAI report data is unavailable.

- **`kpi_detection.py`**  
  Implements logic to detect poor network performance using threshold values and highlights problem areas by operator and region.

---

## 🚀 How to Run

bash
pip install -r requirements.txt
streamlit run app.py




## 📺 Sample Screenshots

### 📊 KPI Trend Dashboard  
![dashboard_sample](images/dashboard_sample.png)

---

## ⚙️ How It Works

1. The app reads from either:
   - A real TRAI IDT report converted to CSV
   - Or synthetic simulated data (generated via `data_generator.py`)

2. KPIs are plotted across:
   - **Operators** (e.g., Airtel, Jio, Vi)
   - **Regions** (Urban, Suburban, Highway, etc.)

3. Thresholds are checked:
   - e.g., CSSR < 95%, DCR > 2% triggers “Poor Network” alert

4. Visual indicators highlight network issues with colored bar plots or tables




## 🧪 Future Extensions

* Integrate with live hardware sensor (ESP32) using MQTT/REST
* Deploy on cloud (e.g., Streamlit Cloud or Heroku)
* Add map-based heatmaps for geo-tagged visualization
* Include time-based historical trend logs

---

## 👨‍💻 Author

**Sandeep Kumar**
🎓 Final Year B.Tech – Electronics and Communication Engineering
🛠️ Interned at TRAI (Regional Office – QoS Dept.)
🔗 [LinkedIn Profile](https://www.linkedin.com/in/sandychoudhary/)

---

## 🪪 License

This project is licensed under the **MIT License**. See the `LICENSE` file for full terms.

---

> ⚠️ **Disclaimer**: This is a simulated prototype created for academic and demonstration purposes. It does not replace certified telecom drive test or QoS tools used by official auditing teams.

