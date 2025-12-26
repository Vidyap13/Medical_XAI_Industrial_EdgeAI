# Medical_XAI_Industrial_EdgeAI
This portfolio explores two critical frontiers in modern Artificial Intelligence: **Explainable AI (XAI)** for high-stakes medical decision-making and **Edge AI** for real-time industrial automation.

---

## 🏥 Part I: Explainable AI in Medical Imaging

### Objective

Address the "Black Box" nature of deep learning to build clinician trust in automated pneumonia detection.

### Project Overview

- **Model**: Fine-tuned a high-performance ResNet50 classifier

- **Performance**: Achieved 87% overall diagnostic accuracy with a 94% recall rate for pneumonia

- **XAI Integration**: Compared two distinct methods to provide visual justifications for predictions:
  - **Grad-CAM**: A white-box method using internal gradients to produce high-resolution heatmaps
  - **LIME**: A black-box, model-agnostic method that perturbs images to identify influential superpixel regions

### Key Insights

- **Grad-CAM** excels in consistency (9/10) and speed, making it ideal for rapid triage
- **LIME** provides more intuitive, region-based justifications for detailed reviews
- **Recommendation**: A dual-analysis approach maximizes clinical trust by combining precise localization with intuitive clarity

---

## 🏭 Part II: Edge AI for Industry 4.0

### Objective

Optimize deep learning models for local deployment on high-speed automotive assembly lines.

### Project Overview

- **Scenario**: Instant vehicle verification (Car vs. Truck) to route units to finishing bays at >10 FPS

- **Model**: Compressed a pre-trained MobileNetV2 for deployment on NVIDIA Jetson Nano

- **Optimization Techniques**:
  - **Iterative Pruning**: Utilized L2 energy-based and Taylor gradient-based methods to reach 50% sparsity
  - **Quantization**: Reduced inference time from ~85ms to ~60ms while lowering power draw to ~7W

### Performance Results

- **Accuracy Retention**: Taylor Iterative pruning maintained 95.2% accuracy (only a 0.2% drop from baseline) at 50% sparsity
- **Efficiency**: Size reduced from 8.9 MB to 6.1 MB, ensuring the system stays within the 10W power limit of the Jetson Nano
- **Reliability**: Local processing ensures 24/7 operation despite internet outages and protects proprietary design data

---

## 🛠️ Technical Stack

- **Frameworks**: TensorFlow/PyTorch, OpenCV
- **Explainability**: Grad-CAM, LIME
- **Edge Hardware**: NVIDIA Jetson Nano
- **Inference Engine**: TensorRT

---

## 📊 Results Summary

| Project | Key Metric | Achievement |
|---------|------------|-------------|
| Medical Imaging (XAI) | Pneumonia Recall | 94% |
| Medical Imaging (XAI) | Overall Accuracy | 87% |
| Edge AI (Industry 4.0) | Accuracy at 50% Sparsity | 95.2% |
| Edge AI (Industry 4.0) | Inference Time | ~60ms |
| Edge AI (Industry 4.0) | Power Consumption | ~7W |

---

## 🚀 Future Directions

- Expand XAI techniques to additional medical imaging modalities
- Explore federated learning for privacy-preserving model training
- Implement real-time model monitoring and drift detection
- Scale Edge AI solutions to multi-model ensemble deployments

---

## 📝 License

This project is available under the [MIT License](LICENSE).

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

---

**Note**: All medical imaging work follows HIPAA compliance guidelines and uses publicly available datasets. Industrial deployment scenarios are based on standard Industry 4.0 requirements.
