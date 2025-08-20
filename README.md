# CoralGrad-LiteNet: Diffusion Model-Enhanced Coral Identification

<p align="center">
  <img src="CoralGrad-LiteNet Diffusion Model-Enhanced Coral Identification.png" alt="CoralGrad-LiteNet Cover" width="600"/>
</p>

A lightweight and efficient multi-scale network for benthic imagery analysis, enhanced with diffusion-based data augmentation.

<div align="center">
  
[![Paper](https://img.shields.io/badge/Paper-CG--LiteNet-blue.svg)](#-citation)  
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](#-license)  

</div>

---

## 📌 Project Background
**Project Background**：Coral reefs support more than 25% of marine life but cover only 0.25% of the ocean surface. Monitoring their health is critical for marine ecosystem balance. Traditional manual underwater surveys are inefficient, and existing AI models struggle with densely overlapping corals, complex textures, and deployment on edge devices.

## 📝 Project Overview
**CoralGrad-LiteNet (CG-LiteNet)** is a **lightweight, multi-scale, diffusion model–enhanced coral detection framework** designed for real-time monitoring in underwater environments. It addresses the challenges of dense coral distribution, complex textures, and underwater degradation by introducing:
- **GA-HFFM** (*Gradient-Aware Hierarchical Feature Fusion Module*): improves global modeling and fine-grained boundary perception.  
- **Slim Backbone/Neck** (*GSConv + VoV-GSCSP*): reduces parameters and FLOPs while preserving representation power.  
- **DADH** (*Dynamically Anchored Distribution-aware Head*): balances coupled/decoupled heads with grouped conv, multi-scale fusion, and dynamic anchoring.  
- **Wise-IoU v2 Loss**: stabilizes regression with dynamic gradient reallocation.  
- **Diffusion Model Data Augmentation** (*LoRA + ControlNet on FLUX.1*): addresses class imbalance and limited samples.  

**Key results:**  
with only **2.1 MB parameters** and **~5.4 GFLOPs**, running at **196–385 FPS**.
- On **UODAC Dataset**: AP50 = **83.5%**  
- On **Sanya-Coral Dataset**: mAP50 = **84.8%**  
- On **Sanya-Coral AI-Enhanced Dataset**: mAP50 = **87.1%**  

---
## 📅 Recent Updates  
- **[2025/08/18]**: We have uploaded an introduction to CoralGrad-LiteNet. After submission, we will make the dataset public, and if accepted, we will make the source code public！！！
---

## 🚀 Performance Highlights
- **Lightweight & Efficient**: only 2.1 MB, 5.4 GFLOPs.  
- **Enhanced Global Modeling**: better boundary and context perception (ERF & CAM visualizations).  
- **Diffusion-Augmented Training**: +82.5% data expansion improves underrepresented coral classes.  

---


## 📊 Datasets

We use three datasets:

* **Sanya-Coral Dataset** (1,149 images, 8 coral species)
* **Sanya-Coral AI-Enhanced Dataset** (2,097 images, augmented with diffusion models)
* **UODAC Dataset** (7,782 images, 4 marine species for generalization)

📥 **Download Links:** Coming soon.


## 📈 Performance Comparison of CG-LiteNet with SOTA Models

| Model      | Dataset     | mAP50    | mAP50-95 | Params | FLOPs | FPS |
| ---------- | ----------- | -------- | -------- | ------ | ----- | --- |
| YOLOv8    | Sanya-Coral | 81.9 | 54.6   | 3.0MB | 8.1G  | 312 |
| YOLOv9    | Sanya-Coral | 81.1 | 54.2   | 1.97MB | 7.6G  | 232.5 |
| YOLOv10   | Sanya-Coral | 81.2 | 53.6   | 2.26MB | 6.5G  | 400 |
| YOLOv11    | Sanya-Coral | 81.2 | 54.5   | 2.58MB | 6.3G  | 153 |
| CG-LiteNet | Sanya-Coral | **84.8** | **57.3** | **2.1MB**  |**5.4G** | 196 |
| CG-LiteNet | AI-Enhanced|**87.1**|**63.6**|**2.1MB**|**5.4G**|**384**|
| CG-LiteNet | UODAC       | **83.5** | **70.7** | **2.1MB** | **5.3G** | —   |

## 🧩 Framework
Diffusion Model Data Augmentation（Generate images）
▼
Input 
▼
Slim Backbone
▼
Slim Neck
▼
DADH Head ├──► Classification
                      └──► Regression (Wise-IoU v2）

## 📂 Project Structure

```bash
CoralGrad-LiteNet/(to be added)
```
## ⚙️ Installation

```bash
Will be published after our article is accepted.
```

## 🏋️ Training

```bash
Will be published after our article is accepted.
```

## 🔍 Evaluation

```bash
Will be published after our article is accepted.
```

## 🎥 Inference Demo

```bash
Will be published after our article is accepted.
```

## 📚 Citation

If you use **CoralGrad-LiteNet** in your research, please cite:

```bibtex
@article{yang2025coralgradlitenet,
  title={Diffusion Model-Enhanced Coral Identification: A Lightweight Multi-Scale Network for Benthic Imagery Analysis},
  author={Yang, Changen and et al.},
  journal={...},
  year={...}
}
```

## 📜 License

This project is released under the [MIT License](LICENSE).

## 🤝 Acknowledgements

* Built on **YOLOv11** framework.
* LoRA + ControlNet for diffusion-based augmentation.
* Supported by **Sanya National Coral Cultivation Experimental Center**.

---

🔗 Official paper: [Diffusion Model-Enhanced Coral Identification](https://github.com/yangchangen-s/CoralGrad-LiteNet)
