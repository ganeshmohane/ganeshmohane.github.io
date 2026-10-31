---
title: "Production ML Inference Optimization"
excerpt: "End-to-end workflow for converting trained models into deployable ONNX and TensorRT engines with measurable latency, throughput, and accuracy validation."
collection: portfolio
stack:
  - PyTorch
  - ONNX
  - TensorRT
  - CUDA
  - MLOps
header:
  image: /images/ml-inference-project.svg
  teaser: /images/ml-inference-project.svg
---

## Overview

I created an inference optimization workflow that moves computer vision models from working training or demo code into reliable production deployments. The goal is to improve GPU efficiency without trading away output correctness.

The workflow covers export, validation, engine building, precision selection, performance benchmarking, and deployment.

## Focus areas

- PyTorch model export to ONNX
- ONNX graph validation with ONNX Runtime
- TensorRT engine compilation
- FP16 and INT8 optimization research
- Dynamic batch and input shape testing
- GPU warm-up and CUDA event benchmarking
- Comparison of p50 and p95 latency
- Accuracy validation before deployment
- Engine rebuilds for target GPU hardware

## Engineering approach

Each optimization step is measured separately. A model is compared with the original outputs, its ONNX graph is validated, and the TensorRT engine is tested with representative production data before it is released.

This prevents a faster engine from masking conversion errors, unsupported operators, shape issues, or regression in model accuracy.
