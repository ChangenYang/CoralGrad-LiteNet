# Integration Note

This is a core-only release, not a full fork.

To use this model with Ultralytics:

1. Install a compatible `ultralytics` package.
2. Copy `core/cg_litenet_core.py` into your custom project.
3. Import and register these classes in your local model parser:
   - `GSConv`
   - `VoVGSCSP`
   - `CSP_GA_HFFM`
   - `Detect_Efficient`
4. Build the model with `configs/CG-LiteNet.yaml`.

Release naming note:

- original local name: `PMSFA`
- released name: `GA_HFFM`
