# VidSafe Anime Violence Dataset (v1)

## Overview
The VidSafe Anime Violence Dataset (v1) is a custom, frame-level annotated dataset
constructed to support research on visual violence detection and multimodal
content moderation in anime-style videos. The dataset was created to address
the lack of publicly available benchmarks for region-level violence detection
in animated and stylized video content.

This dataset is intended for **academic and non-commercial research purposes**
only.

---

## Dataset Statistics
| Attribute | Value |
|---------|-------|
| Total videos | **6** |
| Total extracted frames | **7,381** |
| Violent frames | **1,662** |
| Non-violent frames | **5719** |
| Annotation type | Frame-level bounding boxes |
| Number of classes | 1 (Violence) |
| Annotation tool | CVAT |

> **Note:** Raw anime videos are not redistributed due to copyright constraints.
Only extracted frames and annotations are provided.

---

## Label Definitions
| Class ID | Label | Description |
|--------|-------|-------------|
| 0 | Violence | Physical attacks, aggressive interactions, weapon usage |

---

## Annotation Process
All annotations were created manually using the Computer Vision Annotation Tool
(CVAT). Each violent region within a frame was labeled with a bounding box.
Annotations were reviewed to ensure consistency and accuracy, and only
violence-related labels were retained in the final dataset.

The dataset is designed as a **single-class object detection problem**, focusing
exclusively on the localization of violent actions.

---

## Dataset Structure
```plaintext
vidsafe-anime-dataset-v1/
├── images/
│   ├── train/
│   ├── val/
│   
│
├── annotations/
│   ├── train/
│   ├── val/
│   
│
├── metadata/
│   ├── dataset_summary.csv
│   └── label_definitions.json
│
├── splits/
│   └── train_val_test_split.json
│
├── samples/
    ├── violent_examples/
    └── non_violent_examples/
