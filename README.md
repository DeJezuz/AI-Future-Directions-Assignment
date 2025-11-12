# AI Future Directions Assignment: Pioneering Tomorrow’s AI Innovations 🌐🚀

---

## Part 1: Theoretical Analysis Summary

* **(Note:** The full answers to Q1 and Q2 are provided in the `Theoretical_Analysis.pdf` file.)
* **Key takeaway from Q1 (Edge AI):** [Brief summary of your latency/privacy points.]
* **Key takeaway from Q2 (Quantum AI):** [Brief summary of Quantum AI’s benefits in optimization.]

---

## Part 2, Task 1: Edge AI Prototype (Recyclable Item Classification)

This task involved training a lightweight image classifier and converting it to the TFLite format for edge deployment. The full code is in `edge_ai_prototype.ipynb`.

### 1. Model Architecture and Metrics
* **Base Model:** [e.g., MobileNetV2, EfficientNet-Lite]
* **Quantization Method:** [e.g., Post-training dynamic range quantization]
* **Final Accuracy (Test Set):** [e.g., 91.5%]
* **Model Size Reduction:** [e.g., Reduced from 25 MB to 6.2 MB]

### 2. Deployment Steps (The "How-to")
The following steps outline how the `model.tflite` can be deployed onto a Raspberry Pi or similar embedded device:

1.  **Dependencies:** Install the necessary libraries (e.g., `tflite_runtime` or `tensorflow`).
2.  **Model Loading:** Load the `model.tflite` file into the TFLite Interpreter.
3.  **Input Preparation:** Capture a new image (e.g., from a camera) and resize/normalize it to the model's expected input shape ([e.g., 224x224, normalized to 0-1]).
4.  **Inference:** Call the interpreter's `invoke()` method to execute the model locally.
5.  **Post-Processing:** Read the output tensor and map the highest probability index to the corresponding class label (e.g., 0=Plastic, 1=Glass).
6.  **Action:** [e.g., Send a signal to a robotic arm for sorting.]

---

## Part 2, Task 2: AI-Driven IoT Concept (Smart Agriculture)

This section details the conceptual design for an AI-driven smart agriculture system. The data flow sketch is in `iot_data_flow_diagram.png`.

### 1. Required Sensors 🌾
| Sensor Type | Specific Measurement | Purpose in AI System |
| :--- | :--- | :--- |
| **Soil Moisture** | Volumetric Water Content | Fine-tuning irrigation scheduling. |
| **Soil NPK** | Nitrogen, Phosphorus, Potassium | Determining precise fertilization needs. |
| **Temperature/Humidity** | Air Conditions | Predicting disease risk and optimal growth windows. |
| **NDVI Camera** | Near-Infrared Reflectance | Assessing plant health and stress levels. |
| **[Add more sensors as needed]** | [Measurement] | [Purpose] |

### 2. Proposed AI Model and Rationale 🧠
* **Model:** **LSTM (Long Short-Term Memory)** or **Gradient Boosting Machine (GBM)** (e.g., XGBoost).
* **Rationale:** The model must handle **time-series data** as crop yield depends on accumulated conditions over weeks/months. An **LSTM** is ideal because it excels at learning long-term dependencies (e.g., the effect of low NPK 5 weeks ago) to accurately predict final crop yield and recommend resource adjustments in real-time.
* 
