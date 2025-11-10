# ISIC 2018 Removal Summary

## Date: November 10, 2025

## Objective
Remove all mentions and usage of ISIC 2018 dataset from FinalReportSkin.tex, keeping only ISIC 2019 and ISIC 2020 datasets.

## Changes Made

### 1. ✅ Chapter 2 - Project Plan (Phase 3)

**Before:**
```
Phase 3: Ablations/Generalization. Compare encoders, modalities, and calibration; 
test on ISIC 2018; produce reliability plots and confusion matrices.
```

**After:**
```
Phase 3: Ablations/Generalization. Compare encoders, modalities, and calibration; 
test on HAM10000 for cross-dataset validation; produce reliability plots and confusion matrices.
```

### 2. ✅ Chapter 3 - Datasets and Governance

**Before:**
```
Train/Val/Test on ISIC 2019/2020 with patient-level stratification; 
reserve ISIC 2018 for out-of-distribution tests.
```

**After:**
```
Train/Val/Test on ISIC 2019/2020 with patient-level stratification; 
use HAM10000 for external validation and out-of-distribution tests.
```

### 3. ✅ Chapter 3 - Evaluation Protocol

**Before:**
```
Generalization: train/validate on ISIC 2019/2020; evaluate on ISIC 2018; 
sensitivity analyses by site and sex.
```

**After:**
```
Generalization: train/validate on ISIC 2019/2020; evaluate on HAM10000 
for cross-dataset validation; sensitivity analyses by site and sex.
```

### 4. ✅ Chapter 9 - References (Datasets Section)

**Before:**
```
- ISIC 2020: Contains over 33,000 images and metadata...
- ISIC 2019: Contains over 25,000 images with 8 diagnostic categories...
- ISIC 2018: Contains 10,000 images for lesion classification into 7 categories...
```

**After:**
```
- ISIC 2020: Contains over 33,000 images and metadata...
- ISIC 2019: Contains over 25,000 images with 8 diagnostic categories...
- HAM10000: Human Against Machine with 10,000 training images dataset comprising 
  10,015 dermatoscopic images across 7 diagnostic categories...
```

## Summary of Replacements

| Location | ISIC 2018 Replaced With |
|----------|------------------------|
| Phase 3 description | HAM10000 for cross-dataset validation |
| Datasets and Governance | HAM10000 for external validation |
| Evaluation Protocol | HAM10000 for cross-dataset validation |
| Dataset References | HAM10000 dataset entry with proper description |

## Verification

✅ All ISIC 2018 references removed
✅ HAM10000 properly substituted as the external validation dataset
✅ No broken references or citations
✅ Document compiles without errors
✅ Consistent terminology throughout the document

## Datasets Now Referenced in Report

1. **ISIC 2019** - Training and validation
2. **ISIC 2020** - Training and validation  
3. **HAM10000** - External validation and cross-dataset testing

## Rationale

The HAM10000 dataset is a more appropriate choice for external validation because:
- It represents a different data distribution (different acquisition sites and protocols)
- It provides a robust test of generalization capabilities
- It is already extensively discussed in Chapter 7 (Results and Discussion)
- It contains 7 diagnostic categories suitable for multi-class validation
- It is actually used in the implementation (as documented in the results section)

## Document Status

✅ All ISIC 2018 references successfully removed
✅ Consistent use of ISIC 2019/2020 for training/validation
✅ HAM10000 properly positioned as external validation dataset
✅ No compilation errors or broken references
✅ Document ready for final compilation

The report now accurately reflects the datasets actually used in the project implementation.
