# LNDb v4 Reading Notes

## Main Contribution

LNDb v4 extends the original LNDb dataset by adding structured pulmonary nodule information extracted from real radiology reports and matching these report-derived nodules with manual CT annotations.

## Two Annotation Sources

### Manual CT annotations

- Have explicit 3D spatial coordinates
- Include segmentation and imaging characteristics
- May contain more small nodules because they were produced for research annotation

### Report-derived annotations

- Come from real clinical radiology reports
- Include coarse anatomical location, size, and characteristics
- Do not directly contain voxel-level coordinates
- May be more selective because radiologists report findings in a clinical workflow

## Matching

The matching process uses:

1. anatomical location
2. nodule size
3. nodule characteristics
4. candidate uniqueness and agreement

The final data include:

- matched nodules
- image-only nodules
- report-only nodules

## What the Paper Solved

The paper established and quantified correspondence between research CT annotations and real-world radiology report findings.

## What Remains Open

The paper did not directly investigate:

- neural multimodal representation learning
- image-report contrastive learning
- whether multimodal supervision improves downstream CT tasks
- whether multimodal pretraining helps in low-label settings
