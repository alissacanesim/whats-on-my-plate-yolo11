# What's on My Plate? — YOLO11

YOLO11-based food component detection system that identifies 10 visible food categories in meal images.

## Project Overview

This project uses object detection to identify visible food components in complete meal images. The system returns bounding boxes, class labels, and confidence scores for each detected component.

## Dataset

**Source:** [Food Recognition 2022 — Kaggle](https://www.kaggle.com/datasets/sainikhileshreddy/food-recognition-2022)

The original dataset contained 85 food categories. These categories were mapped into 10 broader food component classes.

**Final dataset size:** 4,183 images

- Train: 2,928 images
- Validation: 836 images
- Test: 419 images

The original bounding boxes were unreliable, so new bounding boxes were calculated from the segmentation polygons. Invalid annotations, selected multi-polygon cases, and duplicate labels were also removed.

## Classes

- bread
- rice
- potato
- egg
- cheese
- tomato
- carrot
- cucumber
- salad
- fruit

## Model

A pretrained YOLO11n model was fine-tuned through transfer learning using Ultralytics and PyTorch.

**Training configuration:**

- Image size: 640 × 640
- Epochs: 50
- Batch size: 16
- Hardware: NVIDIA Tesla T4

## Results

- Precision: 0.768
- Recall: 0.610
- mAP50: 0.674
- mAP50-95: 0.478

## Repository Structure

- `notebooks/` — complete project notebook
- `demo/` — notebook used to demonstrate model inference
- `results/` — metrics, predictions, training plots, and model weights
- `presentation/` — final project presentation
- `requirements.txt` — required Python packages
- `AI_USAGE_LOG.md` — description of AI assistance used during the project
