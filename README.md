# CoralGrad-LiteNet: Diffusion Model-Enhanced Coral Identification

<p align="center">
  <img src="CoralGrad-LiteNet Diffusion Model-Enhanced Coral Identification.png" alt="CoralGrad-LiteNet Cover" width="640"/>
</p>

<p align="center">
  <b>A lightweight and efficient multi-scale framework for benthic imagery analysis</b><br/>
  enhanced with diffusion-based data augmentation for practical underwater coral monitoring.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Task-Coral%20Identification-0f766e?style=for-the-badge" alt="Task"/>
  <img src="https://img.shields.io/badge/Model-CG--LiteNet-1d4ed8?style=for-the-badge" alt="Model"/>
  <img src="https://img.shields.io/badge/Paper-EAAI%202026-f59e0b?style=for-the-badge" alt="Paper"/>
  <img src="https://img.shields.io/badge/License-Repository%20Included-16a34a?style=for-the-badge" alt="License"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Lightweight-2.1%20MB-0ea5e9" alt="Lightweight"/>
  <img src="https://img.shields.io/badge/FLOPs-~5.4G-9333ea" alt="FLOPs"/>
  <img src="https://img.shields.io/badge/Realtime-196--385%20FPS-ef4444" alt="Realtime"/>
  <img src="https://img.shields.io/badge/Datasets-3%20Benchmarks-14b8a6" alt="Datasets"/>
</p>

---

## Overview

Coral reefs support more than 25% of marine life while covering only 0.25% of the ocean surface. Efficient and accurate monitoring is essential for ecosystem conservation, yet underwater surveys remain labor-intensive and visually challenging in dense, texture-rich, and degraded environments.

**CoralGrad-LiteNet (CG-LiteNet)** is a lightweight, multi-scale, diffusion-enhanced coral detection framework developed for real-time underwater monitoring.

## Quick Navigation

- [Highlights](#highlights)
- [Architecture](#architecture)
- [Update Log](#update-log)
- [Paper Access](#paper-access)
- [Datasets](#datasets)
- [Performance Comparison](#performance-comparison)
- [Project Structure](#project-structure)
- [Quick Start](#quick-start)
- [Weights](#weights)
- [Citation](#citation)
- [Contact](#contact)

## Highlights

| Sticker | Detail |
| --- | --- |
| `🌊 Lightweight` | Designed for efficient deployment with only about **2.1 MB** parameters. |
| `⚡ Real-time` | Reaches roughly **196-385 FPS** under the reported settings. |
| `🧠 Multi-scale` | Combines lightweight backbone/neck design with hierarchical feature fusion. |
| `🪸 Coral-focused` | Targets dense coral scenes, complex textures, and underwater degradation. |
| `🧪 Diffusion-enhanced` | Incorporates diffusion-based augmentation to improve data diversity. |

## Architecture

The core design of CoralGrad-LiteNet includes:

- `🧩 GA-HFFM`: a gradient-aware hierarchical feature fusion module for enhanced global context modeling and fine-grained boundary perception.
- `🪶 Slim Backbone/Neck`: `GSConv + VoVGSCSP` for lightweight feature extraction and efficient multi-scale fusion.
- `🎯 DADH`: a dynamically anchored distribution-aware detection head for efficient multi-scale prediction.

### Snapshot

| Item | Value |
| --- | --- |
| Model name | `CoralGrad-LiteNet (CG-LiteNet)` |
| Primary task | Coral identification / underwater object detection |
| Design goal | Lightweight accuracy for practical deployment |
| Key strengths | Boundary awareness, multi-scale fusion, efficient inference |

## Update Log

- `🔜 To appear`: After formal publication of the paper, we will update the model detail figures, technical design illustrations, and the diffusion-based data augmentation scheme.
- `🎉 2026/03/31`: CoralGrad-LiteNet dataset and source code were officially released.
- `📘 2026/03/28`: The CoralGrad-LiteNet paper was officially accepted by *Engineering Applications of Artificial Intelligence (EAAI)*.
- `📝 2025/08/18`: The first public introduction to CoralGrad-LiteNet was released.

## Paper Access

- `Limited-time free access`: https://authors.elsevier.com/c/1msk~_LfeK81lN

## Datasets

The current release involves three datasets:

| Dataset | Scale | Description |
| --- | --- | --- |
| `Sanya-Coral Dataset` | 1,149 images | 8 coral species |
| `Sanya-Coral AI-Enhanced Dataset` | 2,097 images | diffusion-augmented coral dataset |
| `UODAC Dataset` | 7,782 images | 4 marine species for generalization |

### Dataset Access

- `📦 Share link`: https://pan.quark.cn/s/b853984488a5#/list/share
- `📬 Academic usage`: please contact the first author for dataset applications and comparison experiments.

### Taxonomy Note

Please use the latest and most rigorous biological names when reporting results, preparing annotations, or comparing categories. We have already made rigorous corrections in the main text of the paper; at present, only some dataset-related labels may still not have been fully updated. Please pay special attention to this point when conducting comparison experiments. The dataset labels below should be interpreted as follows:

| Original label | Recommended biological name |
| --- | --- |
| `Euphflfiaancora` | `Euphyllia` |
| `Favosites` | `Favites` |
| `Platygyra` | `Platygyra` |
| `WavingHand` | `Anthelia` |
| `Pachyclavularia` | `Pachyclavularia` |
| `Plerogyrasinuosa` | `Plerogyra` |
| `Acropora` | `Acropora` |
| `Brain Coral` | `Trachyphyllia` |

## Performance Comparison

The comparative results below were reported in the earliest public project version and are retained here in the current README for convenient reference.

| Model | Dataset | mAP50 | mAP50-95 | Params | FLOPs | FPS |
| --- | --- | --- | --- | --- | --- | --- |
| YOLOv8 | Sanya-Coral | 81.9 | 54.6 | 3.0 MB | 8.1G | 312 |
| YOLOv9 | Sanya-Coral | 81.1 | 54.2 | 1.97 MB | 7.6G | 232.5 |
| YOLOv10 | Sanya-Coral | 81.2 | 53.6 | 2.26 MB | 6.5G | 400 |
| YOLOv11 | Sanya-Coral | 81.2 | 54.5 | 2.58 MB | 6.3G | 153 |
| CG-LiteNet | Sanya-Coral | **84.8** | **57.3** | **2.1 MB** | **5.4G** | **196** |
| CG-LiteNet | Sanya-Coral AI-Enhanced | **87.1** | **63.6** | **2.1 MB** | **5.4G** | **384** |
| CG-LiteNet | UODAC | **83.5** | **70.7** | **2.1 MB** | **5.3G** | — |

## Project Structure

```bash
D:\CG-LiteNet_OpenSource
|-- README.md
|-- LICENSE
|-- requirements.txt
|-- configs
|   `-- CG-LiteNet.yaml
|-- core
|   |-- cg_litenet_core.py
|   `-- INTEGRATION.md
`-- weights
```

## Quick Start

### 1. Install dependencies

```bash
pip install -r requirements.txt
```

### 2. Register custom modules

Register the modules defined in `core/cg_litenet_core.py` in the local Ultralytics project.

### 3. Build the model

Use `configs/CG-LiteNet.yaml` as the model configuration entry.

## Weights

- `🏷️ Release weight`: `weights\CG-litenet-NoAIdataset.pt`

## Usage Notes

- `📌 Integration guide`: see `core/INTEGRATION.md`
- `📌 Config entry`: see `configs/CG-LiteNet.yaml`
- `📌 Weight notes`: see `weights/README.md`

## Citation

```bibtex
@article{yang2026coralgradlitenet,
  title={Diffusion Model-Enhanced Coral Identification: A Lightweight Multi-Scale Network for Benthic Imagery Analysis},
  author={Yang, Changen and et al.},
  journal={Engineering Applications of Artificial Intelligence},
  year={2026}
}
```

## License

See `LICENSE` for redistribution and derivative-use terms.

## Contact

For collaboration, dataset usage, or comparison experiments:

- **Changen Yang**
- **Email:** 24220855100020@hainanu.edu.cn
