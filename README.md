# Methods for Temporal Action Localization (TAL)

This repository collects state-of-the-art methods for Temporal Action Localization from top-tier conferences (CVPR, ICCV, ECCV, AAAI).

## Datasets

- **THUMOS14**: 20 action classes, commonly used benchmark
- **ActivityNet**: 200 action classes, large-scale dataset
- **EPIC-Kitchens**: Egocentric video dataset
- **HACS**: Large-scale dataset
- **Ego4D**: Egocentric video dataset

## Methods Overview

### Single-Stage Methods

| Method | Conference | Code | Description |
|--------|------------|------|-------------|
| [ActionFormer](./Actionformer) | ECCV 2022 | [GitHub](https://github.com/happyharrycn/actionformer_release) | Transformer-based single-stage TAL |
| [TemporalMaxer](./TemporalMaxer) | ICCV 2023 | [GitHub](https://github.com/TuanTNG/TemporalMaxer) | Maximize temporal context |
| [TriDet](./Trident) | CVPR 2023 | [GitHub](https://github.com/dingfengshi/TriDet) | Relative boundary modeling |
| [VideoMambaSuite](./VideoMambaSuite) | - | [GitHub](https://github.com/OpenGVLab/video-mamba-suite) | State space model for TAL |
| [AdaTAD](./AdaTAD) | CVPR 2024 | [GitHub](https://github.com/sming256/OpenTAD) | End-to-end with 1B parameters |

### Transformer/DETR-based Methods

| Method | Conference | Code | Description |
|--------|------------|------|-------------|
| [RTD-Net](./RTD-Net) | ICCV 2021 | [GitHub](https://github.com/MCG-NJU/RTD-Action) | First Transformer for TAL proposal |
| [TadTR](./TadTR) | - | [GitHub](https://github.com/xlliu7/TadTR) | DETR-based end-to-end detection |
| [UniMD](./UniMD) | ECCV 2024 | [GitHub](https://github.com/yingsen1/UniMD) | Unified moment retrieval and TAD |

### Two-Stage/Proposal Methods

| Method | Conference | Code | Description |
|--------|------------|------|-------------|
| [BMN](./BMN) | ICCV 2019 | [GitHub](https://github.com/JJBOY/BMN-Boundary-Matching-Network) | Boundary matching network |

### Weakly-Supervised Methods

| Method | Conference | Code | Description |
|--------|------------|------|-------------|
| [P-MIL](./P-MIL) | CVPR 2023 | [GitHub](https://github.com/RenHuan1999/CVPR2023_P-MIL) | Proposal-based MIL for WTAL |

## Performance on THUMOS14 (mAP@tIoU=0.5)

| Method | mAP@0.3 | mAP@0.4 | mAP@0.5 | mAP@0.6 | mAP@0.7 | Avg mAP |
|--------|---------|---------|---------|---------|---------|---------|
| ActionFormer | 75.5 | - | 71.0 | - | - | - |
| TemporalMaxer | - | - | - | - | - | - |
| TriDet | 82.9 | 79.4 | 74.3 | 66.0 | 55.1 | 71.5 |
| AdaTAD | 85.2 | 82.1 | 77.1 | 68.8 | 56.9 | 74.0 |

## Data Configuration

All methods are configured to use data from:
```
c:\Users\Administrator\Desktop\Code\deeplearning\Relatedwork\data\thumos\
├── annotations/
│   └── thumos14.json
└── i3d_features/
    ├── video_validation_*.npy
    └── video_test_*.npy
```

## Environment Setup

Each method has its own dependencies. Please refer to the individual README files:

- Python 3.8+
- PyTorch 1.10+
- CUDA 11.0+

## References

1. ActionFormer: Localizing Moments of Actions with Transformers (ECCV 2022)
2. TemporalMaxer: Maximize Temporal Action Localization (ICCV 2023)
3. TriDet: Temporal Action Detection with Relative Boundary Modeling (CVPR 2023)
4. RTD-Net: Relax Transformer Decoder for Temporal Action Proposal (ICCV 2021)
5. BMN: Boundary-Matching Network for Temporal Action Proposal Generation (ICCV 2019)
6. AdaTAD: End-to-End Temporal Action Detection with 1B Parameters (CVPR 2024)
7. UniMD: Unified Moment Retrieval and Temporal Action Detection (ECCV 2024)

## License

Each method retains its original license. Please refer to the individual repositories for details.
