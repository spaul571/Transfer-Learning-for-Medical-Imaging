# Transfer Learning for Medical Imaging

Fine-tuning versus training from scratch for pneumonia detection on chest radiographs.

**Course:** CSE-638: Deep Learning — Daffodil International University
**Topic E** — Group / Team No. 5

| Group Member | Student ID |
| --- | --- |
| Shrikanta Paul | 261-25-017 |
| Md. Nurol Amin | 261-25-021 |
| Animesh Dey | 261-25-019 |
| Kazi Meherunnesa Eva | 261-25-033 |
| Fardin Ahmed Alvi | 261-25-034 |
| Anika Tahsin Prova | 252-25-016 |

## What this project does

Pneumonia is classified from chest X-ray images under three settings, so that the
effect of transfer learning can be isolated from the effect of class balance:

1. **Imbalanced baseline** — models trained on the original split, where pneumonia
   outnumbers normal cases roughly 2.7 : 1.
2. **Balanced, from scratch** — the same architectures trained on a class-balanced
   split with randomly initialised weights.
3. **Balanced, fine-tuned** — the same architectures initialised from ImageNet
   weights and fine-tuned, then explained with Grad-CAM, LIME, and SHAP.

Architectures compared: SimpleCNN, ResNet50, VGG16, MobileNetV2.

## Dataset

Chest X-Ray Images (Pneumonia), Kermany et al. (2018) —
<https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia>

5,856 pediatric anteroposterior radiographs labelled NORMAL or PNEUMONIA. The images
are not stored in this repository.

## Contents

| Path | Contents |
| --- | --- |
| `01-imbalanced-baseline.ipynb` | Phase 1 — imbalanced baseline |
| `02-balanced-scratch.ipynb` | Phase 2 — balanced data, trained from scratch |
| `03-finetuned-gradcam.ipynb` | Phase 3 — ImageNet fine-tuning and explainability |
| `results1/`, `results2/`, `results3/` | Plots produced by each notebook, one folder per phase |
| `report/` | LaTeX source, figures, and compiled PDF of the report |

Every figure in the report is a verbatim output of these notebooks.
