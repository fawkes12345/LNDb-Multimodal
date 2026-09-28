# LNDb-Multimodal
Multimodal representation learning for pulmonary nodules using 3D CT and radiology-report-derived semantics from LNDb v4.
# LNDb-Multimodal

## Project Goal

This project investigates whether semantic information derived from real radiology reports can provide useful supervision for 3D pulmonary CT representation learning.

Using LNDb v4, we aim to align 3D pulmonary nodule representations with report-derived semantic information through multimodal contrastive learning.

## Research Questions

1. Can neural networks learn meaningful correspondence between 3D CT nodules and report-derived semantic information?
2. Does multimodal image-report pretraining improve downstream CT representation learning compared with image-only training?
3. Is multimodal pretraining particularly useful when only a small amount of manually labeled CT data is available?

## Dataset

LNDb v4 provides:

- 3D low-dose chest CT scans
- Manual pulmonary nodule annotations
- Structured information extracted from radiology reports
- Image-report nodule correspondence

Dataset:
https://zenodo.org/records/8348419

Paper:
https://www.nature.com/articles/s41597-024-03345-6

## Planned Pipeline

```text
3D CT Nodule
      ↓
Image Encoder
      ↓
Image Embedding
      ↘
       Contrastive Alignment
      ↗
Semantic Embedding
      ↑
Semantic Encoder
      ↑
Report-derived Information
