# CG-LiteNet Core Open Source

This repository is a **core-only release** for CG-LiteNet.

It intentionally does **not** include the full training framework fork. Instead, it only keeps the minimum content that is useful for open-source release:

- the released model YAML
- the custom core modules used by the model
- a lightweight integration note
- a placeholder directory for checkpoints

## Scope

Included:

- `configs/CG-LiteNet.yaml`
- `core/cg_litenet_core.py`
- `core/INTEGRATION.md`
- `weights/`

Excluded:

- datasets
- logs and experiment outputs
- the full local Ultralytics fork
- the `samsoft` branch

## GA-HFFM Naming

In this open-source package, the original `PMSFA` block is released under the name **GA_HFFM**.

The model YAML has been updated accordingly:

- original internal name: `CSP_PMSFA`
- released open-source name: `CSP_GA_HFFM`

This keeps the release cleaner while preserving the same parameter layout for checkpoint compatibility.

## Minimal Usage

1. Install base dependencies:

```bash
pip install -r requirements.txt
```

2. Register the modules from `core/cg_litenet_core.py` in your own Ultralytics project.

3. Use `configs/CG-LiteNet.yaml` as the model config.

## Weight-Only Release

If you later decide to publish only the weights, you can keep this repository structure and only add your checkpoint file into `weights/`, for example:

- `weights/best.pt`

## License

This release keeps the upstream `AGPL-3.0` license in `LICENSE` because it is derived from Ultralytics-based code.
