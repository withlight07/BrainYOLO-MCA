# BrainYOLO-MCA: An Improved YOLOv11 with Multi-Scale Channel Attention for Brain Tumor Detection

This is the official implementation of the paper "BrainYOLO-MCA: An Improved YOLOv11 with Multi-Scale Channel Attention for Brain Tumor Detection".

📖 Introduction

Brain tumor detection in magnetic resonance imaging (MRI) is crucial for early diagnosis and clinical treatment planning. However, it remains challenging due to blurred tumor boundaries, high visual similarity to normal brain tissue, and tiny early-stage lesions.
We propose BrainYOLO-MCA, an improved YOLOv11 architecture with a novel Multi-scale Channel Attention (MCA) mechanism. Our model achieves state-of-the-art performance on three public brain tumor datasets while maintaining a lightweight design (only 3.1M parameters) and high inference speed (146.2 FPS), making it highly suitable for real-time clinical deployment.

✨ Key Innovations

Multi-scale Channel Attention (MCA) module: Enhances recognition of boundary-blurred tumors by fusing multi-scale features from both average and max pooling branches

DySample dynamic upsampling: Preserves spatial details of tiny lesions

Additional high-resolution detection head: Improves sensitivity to early-stage small tumors

Sparse self-attention: Strengthens global contextual features without significant computational overhead

📄 Dataset Preparation

Download the three public datasets:

Br35H: https://universe.roboflow.com/hashira-fhxpj/br35h-::-brain-tumor-detection-2020

MBrT: https://www.kaggle.com/datasets/ahmedsorour1/mri-for-brain-tumor-with-bounding-boxes

Figshare: https://www.kaggle.com/datasets/ashkhagan/figshare-brain-tumor-dataset

</details>

<details open>
<summary>USE</summary>

### Python

BrainYOLO-MCA follows the exact same usage as YOLO and can be directly used in a Python environment

```python
import warnings
from torch.cuda import seed_all
warnings.filterwarnings('ignore')
from ultralytics import YOLO
if __name__ == '__main__':
	model = YOLO('ultralytics/cfg/models/11/BrainYOLO-MCA.yaml')  
	model.train(data='data_BrainTumor.yaml',   #数据集yaml文件
	            imgsz=640,
	            epochs=200,
	            batch=16,
	            workers=8,
	            device=0,
	            optimizer='SGD',
	)
```


</details>

🛠️ Environment Requirements

Its environmental dependencies are identical to those of the official YOLO release

Python 3.10+

PyTorch 2.0.0+

CUDA 12.1+

Ultralytics 8.0+


📝 Citation







