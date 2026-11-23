# InSAR Railway Change-Point Detection

Code developed for a master's thesis on detecting changes in
railway ground deformation using EGMS InSAR displacement time series
and a Temporal Convolutional Network (TCN).

## Overview

The workflow includes:
- Preprocessing and detrending of EGMS Level 2b time series.
- Synthetic time-series generation with Gaussian change-point targets.
- TCN training and per-observation change-point scoring.
- Evaluation using event-level precision, recall, and F1.

## Model

The TCN uses 32 channels, five residual blocks with dilations
`[1, 2, 4, 8, 8]`, and a kernel size of `5`. A sigmoid output head
produces one change-point score per observation.

## Data

The study uses EGMS Calibrated (Level 2b) line-of-sight displacement
time series. Input datasets are not included in this repository.

## Reproducibility

Refer to the release or commit cited in the thesis for the
implementation used in the reported experiments.

## Author

Shafi Nikzada
