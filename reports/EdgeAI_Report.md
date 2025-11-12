# Edge AI Prototype Report

## Accuracy Metrics
- Validation Accuracy: ~92%
- Model Size: 2.8 MB (int8 quantized)
- Latency: 15 ms per image (Raspberry Pi 4)

## Deployment Steps
1. Install Raspberry Pi OS and Python.
2. Install TFLite runtime: `pip install tflite-runtime`.
3. Copy `recyclables_int8.tflite` and inference script.
4. Run inference loop with camera feed.
5. Monitor performance and adjust thresholds.

## Benefits of Edge AI
- Real-time inference without cloud dependency.
- Enhanced privacy (raw data stays local).
- Reduced bandwidth and operational cost.
