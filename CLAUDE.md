# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a biomedical signal dataset repository containing ECG (Electrocardiogram) and PPG (Photoplethysmography) data. There is no application code — the repository is a data store for signal processing research.

## Datasets

| File | Rows | Description |
|------|------|-------------|
| `ecg.csv` | 4,998 | ECG signal samples, no header, one value per row |
| `ppg.csv` | 2,577 | PPG signal data, first row is a sequential index |

Both files are tracked via Git LFS (configured in `.gitattributes`).

## Working with the Data

Load in Python:

```python
import pandas as pd

ecg = pd.read_csv('ecg.csv', header=None)
ppg = pd.read_csv('ppg.csv', header=None)
```

Common use cases: heart rate extraction, frequency-domain analysis, ECG–PPG synchronization, feature engineering for ML pipelines.
