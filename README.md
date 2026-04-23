# Cross-View Dynamic Learning-Based Multi-Class Industrial Anomaly Detection

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

## 📊 Framework

<img width="1426" height="794" alt="image" src="https://github.com/user-attachments/assets/63363842-411f-45e9-ac1e-a4a414dc86e3" />


## 📊 Detailed structure 
CVDA
<img width="553" height="636" alt="image" src="https://github.com/user-attachments/assets/f855de51-bc46-44cb-a21e-d1941ff486ed" />

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


conda create -n my_env python=3.8.12
conda activate my_env
pip install -r requirements.txt

### 2.  Prepare Datasets

MVTec AD
Download the MVTec-AD dataset from [URL](https://www.mvtec.com/research-teaching/datasets/mvtec-ad). Unzip the file to ../mvtec_anomaly_detection.

|-- mvtec_anomaly_detection
    |-- bottle
    |-- cable
    |-- capsule
    |-- ....


VisA

Download the VisA dataset from [URL](https://github.com/amazon-science/spot-diff). Unzip the file to ../VisA/.

|-- VisA_pytorch
    |-- 1cls
        |-- candle
            |-- ground_truth
            |-- test
                    |-- good
                    |-- bad
            |-- train
                    |-- good
        |-- capsules
        |-- ....

Real-IAD
Contact the authors of Real-IAD [URL](https://realiad4ad.github.io/Real-IAD/) to get the net disk link.

Download and unzip realiad_1024 and realiad_jsons in ../Real-IAD. ../Real-IAD will be like:

|-- Real-IAD
    |-- realiad_1024
        |-- audiokack
        |-- bottle_cap
        |-- ....
    |-- realiad_jsons
        |-- realiad_jsons
        |-- realiad_jsons_sv
        |-- realiad_jsons_fuiad_0.0

### 3. Run Experiments

python mvtec_uni.py --data_path ../mvtec_anomaly_detection
python visa_uni.py --data_path ../VisA_pytorch/1cls
python realiad_uni.py --data_path ../Real-IAD



## 🚀Citation
"""
@ARTICLE{11488626,
  author={Zhou, Jingyu and Ma, Yunfeng and Jiang, Shuai and Wang, Yaonan and Liu, Min},
  journal={IEEE Transactions on Circuits and Systems for Video Technology}, 
  title={Cross-View Dynamic Learning-Based Multi-Class Industrial Anomaly Detection}, 
  year={2026},
  volume={},
  number={},
  pages={1-1},
  keywords={Feeds;Antennas;Frequency modulation;Radio broadcasting;Broadcasting;Broadcast technology;Circuits;Circuits and systems;Integrated circuits;Light emitting diodes;Cross-view dynamic attention;multi-class industrial anomaly detection;multi-view feature learning},
  doi={10.1109/TCSVT.2026.3685706}}
"""
