# TinyML & Edge AI – Hands-on Experiments and Demos

This repository focuses on **TinyML and Edge AI concepts**, demonstrating how **machine learning models can run directly on low-power microcontrollers** without relying on cloud connectivity.

It is designed for **students, researchers, and beginners** who want practical exposure to **on-device AI**, especially in **resource-constrained environments**.

---

## 📌 What This Repository Covers

- Conceptual material on **Edge AI & TinyML**
- End-to-end **TinyML pipeline** (training → optimization → deployment)
- **On-device ML inference** on microcontrollers
- Real-time **risk / anomaly indication using LED alerts**
- 🇮🇳 Focus on **Indian use cases** (low power, low cost, poor connectivity)

---

## Key Concepts

### Edge AI:
Edge AI refers to running **AI inference directly on the device** (sensor, microcontroller, gateway) instead of sending raw data to the cloud.

**Why Edge AI?**
- ⚡ Low latency
- 📶 Works offline
- 💰 Reduced cloud & data costs
- 🔒 Improved privacy

---

### TinyML:
TinyML is a subset of ML that enables **ultra-lightweight models** to run on **microcontrollers with very limited memory and power**.

**Typical Constraints**
- RAM: 2 KB – 256 KB  
- Flash: < 1 MB  
- Power: milliwatts  

**Key Techniques**
- Model quantization (int8)
- Feature reduction
- Lightweight architectures
- TensorFlow Lite Micro

---

## Demonstration Project: TinyML Risk Indicator

### Project Overview
A **logistic regression–based TinyML model** is deployed on an **SPDuino microcontroller** to act as a **real-time health risk indicator**.

**Input**
- 8 numerical features entered via Serial Monitor

**Output**
- Probability score
- HIGH / LOW risk classification
- LED alert for HIGH risk

---

## Hardware Used

- **SPDuino Board** (Arduino-compatible, AVR-based)
- LED + 220Ω resistor
- Breadboard
- USB cable
- Serial Monitor (9600 baud)

**Board Capabilities**
- 8-bit MCU (ATmega328P class)
- Flash: 32 KB  
- SRAM: 2 KB  
- Suitable for lightweight ML inference

---

## TinyML Pipeline (Step-by-Step) 👇

### 1️⃣ Data Preparation
- Load dataset
- Clean and preprocess
- Feature scaling (mean & standard deviation)

---

### 2️⃣ Model Training
- Train Logistic Regression / lightweight NN
- Use Python / TensorFlow
- Extract:
  - Weights
  - Bias
  - Scaler values

---

### 3️⃣ Model Optimization
- Keep model lightweight
- Quantization (int8 where applicable)
- Convert to TinyML-compatible format

---

### 4️⃣ Deployment on Microcontroller
- Arduino IDE setup
- Implement:
  - Dot product
  - Bias addition
  - Sigmoid activation
- Upload sketch to SPDuino

---

### 5️⃣ On-Device Inference
- Inputs via Serial Monitor
- Local computation only
- No internet / cloud dependency

---

### 6️⃣ Alert Mechanism
- `probability ≥ 0.5` → **HIGH RISK (LED ON)**
- `probability < 0.5` → **LOW RISK (LED OFF)**

---

## 🔧 Role of TensorFlow in This Project

- Model building & training
- Feature normalization
- Model optimization
- Conversion to TensorFlow Lite / TinyML format
- Ensures **consistent predictions** from PC → device

---

## 🇮🇳 Why Edge AI & TinyML Matter (Indian Context)

- Poor or intermittent connectivity
- Unreliable power supply
- Cost-sensitive deployments
- Data privacy concerns

**Edge + TinyML provides:**
- Low power
- Low latency
- Low cost
- Low connectivity dependency

---

## Applications & Use Cases

- Smart healthcare monitoring
- Wearable devices
- Smart agriculture
- Industrial IoT (predictive maintenance)
- Automotive intrusion detection
- Rural & remote AI deployments

---

## 🛠️ Technologies Used

- Python
- TensorFlow / TensorFlow Lite
- Arduino IDE
- SPDuino (Arduino-compatible MCU)
- Serial communication
- Embedded systems

---

## Who Should Use This Repo?

- Engineering students (AI / IoT / Embedded / Cloud)
- Faculty for demonstrations
- Beginners exploring TinyML
- Researchers working on Edge AI
- Hackathon & project teams

---

## 📌 Notes

- This repository is **educational**
- Models are intentionally lightweight
- Ideal for **lab demos and learning**
- Cloud is used only for **training**, not inference

---

## Support & Connect

If you find this repository helpful:
- ⭐ Star the repo
- 🍴 Fork it
- 📢 Share with peers

---

### 🔗 Follow Me Here

Stay connected for more content on **TinyML, Edge AI, Cloud, and Engineering Labs**:

- 📌 **YouTube:** https://youtube.com/@theengineeringcodex  
- 📌 **Instagram:** https://www.instagram.com/engineering_codex  
- 📌 **Blogger:** https://engineeringcodex1325.blogspot.com/  
- 📌 **LinkedIn:** https://www.linkedin.com/in/sarah-rachel-65532720b  

---
