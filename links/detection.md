---
layout: default
---

# 2D Object Detection and Animal Tracking

## Detection Models

Overview of commonly used object detection and segmentation models, including CNN-based and transformer-based architectures.

| Model | Type | Architecture | Notes |
|-------|------|--------------|-------|
| [YOLOv8](https://github.com/ultralytics/ultralytics) | Detection / Segmentation | CNN | Fast real-time detection; widely used for animal tracking pipelines |
| [YOLOv9](https://github.com/WongKinYiu/yolov9) | Detection | CNN | Improved gradient flow via GELAN architecture |
| [YOLOv10](https://github.com/THU-MIG/yolov10) | Detection | CNN | NMS-free end-to-end detection |
| [RT-DETR](https://github.com/lyuwenyu/RT-DETR) | Detection | Transformer (DETR) | Real-time transformer detector; competitive with YOLO at high accuracy |
| [SAM 2](https://github.com/facebookresearch/segment-anything-2) | Segmentation | Transformer (Hiera) | Promptable segmentation and tracking in images and video |
| [Grounding DINO](https://github.com/IDEA-Research/GroundingDINO) | Detection | Transformer (DINO) | Open-set detection from text prompts; useful for zero-shot animal detection |
| [DINO / DETR](https://github.com/IDEACVR/DINO) | Detection | Transformer (DETR) | High-accuracy transformer detector; strong baseline for fine-tuning |
| [Detectron2](https://github.com/facebookresearch/detectron2) | Detection / Segmentation | CNN (ResNet/FPN) | Modular framework supporting Faster R-CNN, Mask R-CNN, and more |
| [MMDetection](https://github.com/open-mmlab/mmdetection) | Detection / Segmentation | CNN + Transformer | Large model zoo covering classical and modern architectures |

## Code and software

- Add GitHub repositories, packages, or tools here.

## Notes for contributors

Keep additions concise, clearly labeled, and beginner-friendly.
