# awesome-rocm-autodrive
A curated and practical collection of training examples, tools, and ROCm optimizations for key autonomous driving models. It aims to accelerate the deployment of deep learning models on AMD GPUs by providing out-of-the-box training support, Docker environments, and performance tuning utilities.

## 🔧 Supported Models (Initial Release)

| Model           | Type            | Repo Link                     | ROCm Support | Notes                              |
|------------------|------------------|--------------------------|---------------|-------------------------------------|
| ResNet-50        | Backbone         |  | ✅ Supported   |    |
| EfficientNet-B7  | Backbone         |  | ✅ Supported   | Currently have performance issue with DWConv          |
| PointPillars     | Point Cloud      |  | ✅ Supported   | Need ROCm mmcv to get better performance          |
| MapTR            | Vector Prediction|  | ✅ Supported |  |
| FlashOcc         | Scene Occupancy  |  | ✅ Supported |         |
| Sparse4D         | Sparse Detector  |  | ✅ Supported | |
| BEVFormer        | Multi-view       |  | ✅ Supported  |        |

See full list in [registry/MODELS.md](registry/MODELS.md)

---

## 🚀 Quick Start

1. Clone the repo:

```bash
git clone https://github.com/YOUR_ORG/awesome-rocm-autodrive.git
cd awesome-rocm-autodrive



