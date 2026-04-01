# CoralGrad-LiteNet: Diffusion Model-Enhanced Coral Identification

<p align="center">
  <img src="CoralGrad-LiteNet Diffusion Model-Enhanced Coral Identification.png" alt="CoralGrad-LiteNet Cover" width="600"/>
</p>

<p align="center">
  <b>A lightweight and efficient multi-scale framework for benthic imagery analysis</b><br/>
  enhanced with diffusion-based data augmentation.
</p>

<div align="center">

[![Paper](https://img.shields.io/badge/Paper-CG--LiteNet-blue.svg)](#citation)
[![License](https://img.shields.io/badge/License-See%20Repository-green.svg)](#license)

</div>

---

## Project Background

Coral reefs support more than 25% of marine life while covering only 0.25% of the ocean surface. Efficient and accurate monitoring is essential for ecosystem conservation, yet underwater surveys remain labor-intensive and challenging in dense, texture-rich, and degraded visual environments.

## Project Overview

**CoralGrad-LiteNet (CG-LiteNet)** is a lightweight, multi-scale, diffusion-enhanced coral detection framework developed for real-time underwater monitoring.

The core design of CoralGrad-LiteNet includes:

- **GA-HFFM**: a gradient-aware hierarchical feature fusion module for enhanced global context modeling and fine-grained boundary perception.
- **Slim Backbone/Neck**: `GSConv + VoVGSCSP` for lightweight feature extraction and efficient multi-scale fusion.
- **DADH**: a dynamically anchored distribution-aware detection head for efficient multi-scale prediction.

## Update Log

- **🔜 [To appear]**: After formal publication of the paper, we will update the model detail figures, technical design illustrations, and the diffusion-based data augmentation scheme.
- **🎉 [2026/03/31]**: CoralGrad-LiteNet dataset and source code were officially released.
- **📘 [2026/03/28]**: The CoralGrad-LiteNet paper was officially accepted by *Engineering Applications of Artificial Intelligence (EAAI)*.
- **📝 [2025/08/18]**: The first public introduction to CoralGrad-LiteNet was released.

## Datasets

The current release involves three datasets:

- **Sanya-Coral Dataset** (1,149 images, 8 coral species)
- **Sanya-Coral AI-Enhanced Dataset** (2,097 images, augmented with diffusion models)
- **UODAC Dataset** (7,782 images, 4 marine species for generalization)

Dataset share link:

- https://pan.quark.cn/s/b853984488a5#/list/share

## Dataset Access and Usage

Dataset applications, academic use requests, and related questions are handled through the first author:

- **Changen Yang**
- **Email:** 24220855100020@hainanu.edu.cn

Support for comparison experiments is also available through author contact.

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

## Minimal Usage

```bash
pip install -r requirements.txt
```

Register the modules defined in `core/cg_litenet_core.py` in the local Ultralytics project, then build the model with `configs/CG-LiteNet.yaml`.

## Weight Release

- `weights\CG-litenet-NoAIdataset.pt`

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
