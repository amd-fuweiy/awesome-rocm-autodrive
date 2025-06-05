# 📋 Supported Models in Awesome ROCm AutoDrive

This page tracks the current status, features, and notes for each supported or planned model in this repository.

> ✅ = Fully supported & tested on ROCm  
> ⚠️ = Partially supported / under development  
> ⛔️ = Not yet supported or blocked by framework

---

## ✅ Summary Table

| Model           | Task                    | ROCm Status | MMCV Required | ROCm-Specific Notes |
|------------------|-------------------------|-------------|----------------|----------------------|
| ResNet-50        | Image Backbone          | ✅ Supported | ❌ No           | Works with torchvision models |
| EfficientNet-B7  | Image Backbone          | ✅ Supported | ❌ No           | Ongoing performance tuning on DWConv  |
| PointPillars     | 3D Object Detection     | ✅ Supported | ✅ Yes          | ROCm version mmcv needed to get better performance |
| MapTR            | Vector Prediction       | ✅ Supported | ✅ Yes          |    |
| FlashOcc         | Occupancy Prediction    | ✅ Supported | ✅ Yes          |    |
| Sparse4D         | Sparse 3D Detection     | ✅ Supported | ✅ Yes          | |
| BEVFormer        | BEV Perception          | ✅ Supported | ✅ Yes          | |

---

## 📌 Per-Model Details

### 🧠 ResNet-50

- **Repo**: [examples/resnet50](../examples/resnet50)
- **Training**: Single & multi-GPU tested
- **Precision**: FP32 & AMP (float16)
- **Known Issues**: None

---

### 🧠 EfficientNet-B7

- **Repo**: [examples/efficientnetb7](../examples/efficientnetb7)
- **Training**: AMP works; batch size tuning may be needed
- **Dependency**: [timm](https://github.com/huggingface/pytorch-image-models)
- **Known Issues**: DWConv have performance issue

---

### 🧠 PointPillars

- **Repo**: [examples/pointpillars](../examples/pointpillars)
- **Training Framework**: mmdetection3d
- **Known Issues**: None after patching

---

### 🧠 MapTR

- **Repo**: [examples/maptr](../examples/maptr)
- **Training Framework**: mmdetection + mmengine
- **Known Issues**: None 

---

### 🧠 FlashOcc

- **Repo**: [examples/flashocc](../examples/flashocc)
- **Framework**: OpenOcc
- **Known Issues**: None 

---

### 🧠 Sparse4D

- **Repo**: [examples/sparse4d](../examples/sparse4d)
- **Framework**: Custom
- **Known Issues**: None 

---

### 🧠 BEVFormer

- **Repo**: [examples/bevformer](../examples/bevformer)
- **Framework**: mmdetection3d
- **Known Issues**: None

---

## 📊 Legend

- **ROCm Status**: Whether this model has been successfully trained on AMD ROCm stack
- **MMCV Required**: Whether the model depends on mmcv/mmengine (needs patching for ROCm)
- **Mixed Precision**: AMP support tested
- **ROCm Notes**: Any patches, workarounds, or performance observations

---

## 📬 Contributions Welcome

Want to add a model or improve ROCm support? Feel free to submit a pull request or open an issue. We especially welcome:

- Porting new autonomous driving models
- Adding benchmark results
- Submitting patches for ROCm compatibility


