# CSIRO-BIOMASS-COMPETITION
## Overview
This notebook implements a comprehensive ensemble approach combining:

1. **SigLIP Feature Extraction** with semantic features and advanced ensemble models
2. **DINOv3 Vision Transformer** with FiLM modulation for dual-stream processing
3. **Strategic Ensemble** with weighted combination for all targets

### Key Features
- Embedding caching for faster execution
- **Clover prediction ENABLED** (with threshold to remove noise)
- Mass balance reconciliation
- Test-time augmentation
- Optimized hyperparameters
- 10+ model architectures (Random Forest, Extra Trees, MLP, TabNet, Custom NN)

### IMPORTANT: Clover Prediction
**This version TRAINS models to predict Dry_Clover_g** (not fixed at 0)
- All models (LightGBM, CatBoost, RF, etc.) predict clover
- Threshold of 0.5g applied to remove noise
- Both SigLIP and DINOv3 contribute to clover predictions
- Adjust `CLOVER_THRESHOLD` in `post_process_biomass()` as needed
