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




















