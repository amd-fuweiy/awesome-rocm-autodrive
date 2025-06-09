# awesome-rocm-autodrive
A curated and practical collection of training examples, tools, and ROCm optimizations for key autonomous driving models. It aims to accelerate the deployment of deep learning models on AMD GPUs by providing out-of-the-box training support, Docker environments, and performance tuning utilities.

## 🔧 Supported Models (Initial Release)

| Model           | Type            | Repo Link                     | README for ROCm | Notes                              |
|------------------|------------------|--------------------------|---------------|-------------------------------------|
| ResNet-50        | Backbone         | https://github.com/amd-fuweiy/vision | [example/backbone](examples/backbone/readme.md)   |    |
| EfficientNet-B7  | Backbone         | https://github.com/amd-fuweiy/vision |    | Currently have performance issue with DWConv    |
| PointPillars     | Point Cloud      |  |    | Need ROCm mmcv to get better performance          |
| MapTR            | Vector Prediction|  |  |  |
| FlashOcc         | Scene Occupancy  |  |  |         |
| Sparse4D         | Sparse Detector  | https://github.com/binding7012/Sparse4D |[examples/detection/sparse4d](examples/detection/sparse4d) | |
| BEVFormer        | Multi-view       |  |  |        |


---

## 🚀 Quick Start

1. Clone the repo:

```bash
git clone https://github.com/YOUR_ORG/awesome-rocm-autodrive.git
cd awesome-rocm-autodrive



