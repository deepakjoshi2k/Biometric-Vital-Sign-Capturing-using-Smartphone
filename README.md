# Biometric-Vital-Sign-Capturing-using-Smartphone
Develop an AI-powered solution that captures and assesses vital biometric signs using standard camera devices and open-source datasets.

| **Status** | In Development |
| :--- | :--- |
| **Objective** | Affordable, accessible, camera-based healthcare diagnostics. |
| **Vital Signs** | Heart Rate (HR), Blood Pressure (BP), Blood Oxygen Saturation ($\text{SpO}_2$) |
| **Technology** | AI, Computer Vision, Remote Photoplethysmography (rPPG) |

## 💡 Project Objective

The primary objective is to **Develop an AI-powered solution that captures and assesses vital biometric signs using standard camera devices and open-source datasets.**

This innovation aims to deliver essential healthcare diagnostics to **underserved communities, especially in semi-urban and rural areas.**

***

## 🚨 Problem Statement & Purpose

### Problem Statement

Barriers to essential healthcare diagnostics exist in rural and semi-urban areas due to **high costs**, **reliance on specialized technology**, and **poorly resourced facilities**, underscoring the need for **affordable, accessible solutions.**

### Purpose

The project aims to leverage **AI-powered, camera-based biometric monitoring** to bridge healthcare accessibility gaps, providing underserved communities with **timely and affordable diagnostics.**

***

## 📋 Key Use Cases

1.  **Vital Sign Monitoring:** Enable camera-based monitoring of health metrics.
2.  **Telehealth Integration:** Enable telehealth platforms to remotely assess patient vitals.
3.  **Population Health Analytics:** Utilize anonymized data to advance public health research and interventions.

***

## 🔬 Vital Signs Model Development

The solution is focused on estimating key physiological parameters from video input.

### Target Measurements

* Heart Rate (HR) Estimation
* Blood Pressure (BP) Estimation
* Blood Oxygen Saturation ($\text{SpO}_2$) Estimation - Approximate
* Body Temperature (out of scope using video input)


### Physiological Measurement Techniques

| Vital Sign | Technique Overview |
| :--- | :--- |
| **Heart Rate (HR)** | Detect peaks in the **rPPG signal** and calculate heart rate using the peak intervals. |
| **Blood Pressure (BP)** | **Signal Morphology Analysis:** Analyze rPPG signal features (systolic/diastolic peaks). **Pulse Transit Time (PTT):** Calculate PTT by measuring the delay between rPPG and other signals. Use machine learning models trained on labeled data to predict BP values. |
| **Blood Oxygen Saturation ($\text{SpO}_2$)** | Extract red and blue channel intensities. Compute the absorption ratio to estimate $\text{SpO}_2$ values. |

### Temperature Measurement Challenges

We are **not pursuing model development for temperature measurements** due to the lack of thermal imaging data. Most videos are captured using **RGB cameras**, which don't provide direct thermal information, requiring less accurate indirect estimation methods.

***

## 💾 Datasets for Vital Signs

The project relies on open-source datasets for model training and validation.

### Data Sources
Open source: **V-BPE, PPG, UBFC**

### Type of Data Collected
* **Image/Video Data:** Video, Image and PPG signals
* **Physiological Data:** Pulse, BP (Systolic & Diastolic BP)
* **Metadata:** Age, Height, Weight, Gender, BMI

### Dataset Details

| Dataset | Description |
| :--- | :--- |
| **V-BPE Dataset** | Has vitals such as Heart Rate and BP. Includes preprocessed videos and metadata. Videos filtered on dark skin tone, reducing size from 81 GB to 35.13 GB. |
| **PPG Dataset** | Has vitals such as Heart Rate and BP. Contains **Photoplethysmogram signal** instead of patient videos. |

### ⚠️ Challenges in Data Collection
* Less number of **open source datasets**.
* Dataset is limited to **research purposes** and not for **commercial usage**.
