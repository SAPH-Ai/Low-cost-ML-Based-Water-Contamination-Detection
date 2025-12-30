# 💧 Cheap & Rapid Water Contamination Detection System

![Status](https://img.shields.io/badge/Status-Prototype-orange)
![ML](https://img.shields.io/badge/AI-TensorFlow_Lite-FF6F00)
![Hardware](https://img.shields.io/badge/Hardware-Raspberry_Pi_4-C51A4A)
![License](https://img.shields.io/badge/License-MIT-green)


---

## 📖 Overview

Access to clean water is a critical issue in rapidly urbanizing nations like Bangladesh. Traditional water testing is expensive, time-consuming, and often fails to detect modern pollutants like microplastics.

This project introduces an **AI-powered Modular Device** that inspects water samples using a macro camera and computer vision. It achieves **~90% accuracy** in identifying contaminants and suggests immediate treatment methods.

---

## ✨ Key Features

* **🔍 Micro-Pollutant Detection:** Specifically trained to detect **Microplastics (PET)**, **Microfibers (Polyester)**, and **Iron** particles which traditional sensors often miss.
* **⚡ Real-Time Analysis:** Uses **TensorFlow Lite** (SSD MobileNet V2) to process images on-edge, providing results in seconds rather than days.
* **💰 Ultra-Low Cost:** Target production cost is **2,000–4,000 BDT ($18–$46 USD)**, making it accessible for average consumers and rural communities.
* **📱 Modular & Portable:** Designed as a handheld unit with a 3D-printed body, rechargeable battery, and built-in display.

---

## ⚙️ How It Works



1.  **Image Capture:** A high-resolution **Macro Camera** with LED flash captures microscopic images of the water sample.
2.  **AI Processing:** The image is fed into a **Raspberry Pi 4** (or SBC) running a custom-trained **SSD MobileNet V2** model.
3.  **Detection:** The model identifies specific contaminants (e.g., "Microplastic Score: 97%").
4.  **Actionable Output:** The device displays the contamination type and suggests purification methods (e.g., UV disinfection, Filtering).

---

## 🛠️ Tech Stack

### Software
* **Framework:** TensorFlow Lite Object Detection API
* **Architecture:** SSD MobileNet V2 FPN Lite 320
* **Language:** Python
* **Tools:** LabelImg (Annotation), Google Colab (Training)

### Hardware (Prototype)
* **Core:** Raspberry Pi 4 (4GB)
* **Optics:** Macro Camera + Custom Lens + LED Flash
* **Display:** SPI Screen
* **Power:** 1000mAh 2S LiPo Battery + DC-DC Buck Converter (5V)



[Image of Raspberry Pi 4 pinout]


---

## 📊 Performance & Results

We trained the model on **500+ annotated images** and tested it against 702 real-world samples.

| Metric | Result | Notes |
| :--- | :--- | :--- |
| **Accuracy** | **~90%** | Comparable to high-end lab models. |
| **Sensitivity** | **92%** | High true positive rate (629/687). |
| **Cost** | **~3,000 BDT** | vs. ~24,000 BDT for equivalent Lab Tests. |
| **Time** | **Real-Time** | vs. 7-10 days for Lab Reports. |



*Figure: Successful detection of Microplastics (left) and Iron (right) with high confidence scores.*

---

## 🌍 Use Cases

### 🏡 Consumer
A generic handheld device for checking drinking water quality at home via a built-in screen or Smartphone App.

### 🏭 Industrial Integration
The detection module can be installed at the intake of **Wastewater Treatment Plants (WTPs)**. It controls "Miniature Treatment Chambers" to pre-treat specific contaminants, saving energy and chemicals by only treating what is present.

---

## 🚀 Future Roadmap
* [ ] **Custom SBC:** Transition from Raspberry Pi to a custom ARM-based board to lower cost.
* [ ] **Expanded Dataset:** Train model on Bacteria (E. Coli), Arsenic, and biological waste.
* [ ] **Sensor Fusion:** Integrate pH, Turbidity, and TDS sensors for hybrid data analysis.

---

## 👥 Authors
* **Abrar Abir**
* **A Z M Emtenan Kabir**
* *Dhaka Residential Model College, Bangladesh*

---
