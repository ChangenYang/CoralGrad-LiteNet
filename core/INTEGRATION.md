# Integration

This repository provides the released core modules for CoralGrad-LiteNet.

To integrate the model into a local Ultralytics environment:

1. Install a compatible `ultralytics` package.
2. Place `core/cg_litenet_core.py` into the target project.
3. Register the following classes in the local model parser:
   - `GSConv`
   - `VoVGSCSP`
   - `CSP_GA_HFFM`
   - `DADH`
4. Build the model with `configs/CG-LiteNet.yaml`.
