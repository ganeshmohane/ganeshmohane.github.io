---
title: "Privacy AI Models"
excerpt: "Rebuilt privacy-computer-vision pipeline with face and license plate detection, TensorRT inference, multi-GPU support, and production APIs targeting under 200 ms per frame."
collection: portfolio
stack:
  - Computer Vision
  - PyTorch
  - TensorRT
  - CUDA
  - Multi-GPU
  - Flask
  - MLOps
header:
  image: /images/privacy-ai-project.svg
  teaser: /images/privacy-ai-project.svg
---

## Overview

I redesigned and rebuilt the privacy AI pipeline when the earlier face and license plate detection system became unreliable and difficult to scale. The previous implementation had become too slow and too fragmented, so I rebuilt the pipeline and surrounding deployment infrastructure from scratch.

The new system processes video frames end to end, detecting faces and license plates, applying privacy protection, and exposing the inference workflow through production services.

## What I built

- New face detection and license plate detection models
- A rebuilt detection and privacy-processing pipeline
- PyTorch-to-ONNX model conversion
- TensorRT engine creation and deployment
- FP16 inference optimization for NVIDIA GPUs
- Multi-GPU support for increased throughput
- Preprocessing, batching, inference, and postprocessing integration
- Flask-based application endpoints
- Structured logging, monitoring, and alerting

## Performance and deployment

The rebuilt pipeline was profiled and optimized at the complete inference level. It was designed to process frames in under 200 ms while supporting multiple NVIDIA GPUs.

The production design also includes engine validation, deployment configuration, runtime monitoring, and operational logs so model behavior and infrastructure performance remain observable after release.
