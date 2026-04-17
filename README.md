# Cross-View Dynamic Learning for Multi-Class Industrial Anomaly Detection

> **📢 News (2026-04-15):** Our paper has been accepted by **IEEE Transactions on Circuits and Systems for Video Technology (TCSVT)**! We are currently organizing the full code, pre‑trained models, and dataset preparation scripts to ensure reproducibility. The complete project (code, datasets, documentation) will be open‑sourced soon. Stay tuned! ⭐



This repository is the official implementation of our TCSVT paper **"Cross-View Dynamic Learning-Based Multi-Class Industrial Anomaly Detection"**. We propose a novel framework that jointly models multi‑scale and multi‑perspective feature interactions for high‑performance, unified anomaly detection and localization across diverse industrial product categories.

---

## ✨ Highlights

- **Unified Multi‑Class Framework** – One single model handles **30+ product categories** (Real‑IAD) without class‑specific fine‑tuning.
- **Cross‑View Dynamic Learning** – Dynamically fuses features from multiple views (global, local, orthogonal) to capture both subtle and structural anomalies.
- **State‑of‑the‑Art Performance** – Achieves superior image‑level and pixel‑level results on **MVTec‑AD**, **VisA**, and the challenging **Real‑IAD** benchmark.
- **Comprehensive Evaluation** – Provides 7 metrics (AUROC, AP, F‑max, AUPRO, and the novel **mAD**) for holistic assessment.
- **Reproducible** – Full code, pre‑trained weights, and dataset preparation scripts will be released.

---

## 📊 Datasets

We evaluate on three public industrial anomaly detection datasets:

| Dataset | Classes | Total Images | Resolution | Description |
|---------|---------|--------------|------------|-------------|
| **MVTec‑AD** | 15 | 5,354 | up to 1024×1024 | Classic benchmark |
| **VisA** | 12 | 10,821 | high‑res | Complex structures, multiple instances per class |
| **Real‑IAD** | 30 | 151,050 | 2k–5k | Large‑scale, challenging (0.01%–6.75% defect proportion) |

---

## 📈 Evaluation Metrics

We report both **image‑level** (detection) and **pixel‑level** (localization) metrics:

| Level | Metrics |
|-------|---------|
| Image‑level | AUROC, Average Precision (AP), F1‑max (F‑max) |
| Pixel‑level | AUROC, AP, F‑max, Area Under Per‑Region Overlap (AUPRO) |
| **Overall** | **mAD** (mean of all seven metrics above) |

Final performance is averaged across all classes within each dataset.

---

## 🚀 Getting Started

### 1. Environments

Create a new conda environment and install required packages:

```bash
conda create -n my_env python=3.8.12
conda activate my_env
pip install -r requirements.txt
