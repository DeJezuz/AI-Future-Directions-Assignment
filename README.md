# AI Future Directions Assignment: Pioneering Tomorrow’s AI Innovations 🌐🚀

## 1. Project Overview
This repository contains the required deliverables for the "AI Future Directions" assignment, covering theoretical analysis of emerging trends and practical implementation of an Edge AI prototype and an AI-IoT concept.

---

## 2. Part 1: Theoretical Analysis (Q1 & Q2)
* **Full Answers:** Detailed essays for Q1 (Edge AI) and Q2 (Quantum AI) are contained in **`Theoretical_Analysis.pdf`**.

---

## 3. Part 2, Task 1: Edge AI Prototype (Image Classification)

The `edge_ai_prototype.ipynb` notebook details the process of training a lightweight model and converting it to TensorFlow Lite for on-device inference.

### Model Performance Summary
| Metric | Value (Float32 Keras Model) | Value (INT8 TFLite Model) |
| :--- | :--- | :--- |
| **Accuracy** | [e.g., 92.1%] | [e.g., 90.5%] |
| **Model Size** | [e.g., ~14.5 MB] | **[Check File Size]** [e.g., 3.8 MB] |
| **Avg. Inference Time** | [e.g., 50 ms] | **[Check Colab Output]** [e.g., 12 ms] |

### Deployment Steps (How to use `model.tflite`)
1.  **Environment Setup:** Install the `tflite_runtime` libraries on the target device (e.g., Raspberry Pi).
2.  **Load Model:** Instantiate the TFLite Interpreter using the **`model.tflite`** file path.
3.  **Prepare Input:** Capture an image and preprocess it by resizing to **224x224** and converting the data type to **UINT8 (0-255)**, matching the quantized model's expected input type.
4.  **Inference:** Call `interpreter.invoke()` to execute the model locally.
5.  **Output:** Dequantize the output tensor and map the highest probability to the corresponding recyclable item class.

---

## 4. Part 2, Task 2: AI-Driven IoT Concept (Smart Agriculture)

### AI Model Proposal
* **Scenario:** Predicting optimal crop yields and resource needs.
* **Proposed Model:** [e.g., LSTM or XGBoost].
* **Rationale:** [Explain why this model handles the time-series dependency of crop growth best, e.g., LSTMs capture long-term environmental history.]

### Sensor Requirements
| Sensor Type | Specific Measurement | Purpose in AI System |
| :--- | :--- | :--- |
| **Soil Moisture** | Volumetric Water Content | Fine-tuning irrigation scheduling. |
| **Soil NPK** | Nitrogen, Phosphorus, Potassium | Calculating fertilizer doses. |
| **NDVI Camera** | Plant Reflectance Index | Detecting early plant stress and health assessment. |
| [Add other key sensors] | [Measurement] | [Purpose] |

### Data Flow Diagram
The data flow concept is visualized in the file **`iot_data_flow_diagram.png`**.
