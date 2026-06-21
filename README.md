# BEETL Competition 2021 Motor Imagery Dataset A — transfer learning benchmark

## Overview

Beetl2021-A is a preprocessed motor imagery EEG dataset from the BEETL Competition Task 2 (NeurIPS 2021), comprising data from 3 healthy subjects collected during an online racing game (Cybathlon2020IC). The dataset contains 63-channel EEG recordings at 500 Hz with four-class motor imagery tasks (rest, left hand, right hand, feet) and serves as a benchmark for evaluating transfer learning and domain adaptation methods across heterogeneous EEG datasets and subjects. This dataset is part of a larger competition focused on advancing transfer learning for subject independence and cross-dataset generalization in brain-computer interfacing.

## Dataset Summary

| Property | Value |
|---|---|
| Subjects | 4 |
| Channels | 63 |
| Classes | 4 |
| Trial length | 4 s |
| Sampling frequency | 500 Hz |
| Sessions | 1 |
| Total trials | 1490 |
| Paradigm | MotorImagery |

## Data Collection Methods

EEG data were acquired at 500 Hz from 63 channels using standard 1005 montage during an online BCI racing game (Cybathlon2020IC) with visual feedback. The experimental protocol comprised 5 training races and 10 testing races per subject, with each trial lasting 4 seconds. Motor imagery tasks included four classes: rest, left hand, right hand, and feet. Online preprocessing included 1-100 Hz bandpass filtering and 50 Hz notch filtering. Data underwent offline preprocessing with identical bandpass (1-100 Hz) and notch (50 Hz) filtering before release. The dataset was part of the BEETL Competition Task 2, which focused on transfer learning from multiple source datasets (Cho2017, BNCI2014, PhysionetMI) to target datasets with different EEG setups and electrode configurations.

## How to Access via MOABB

Install MOABB and load this dataset directly:

```python
from moabb.datasets import Beetl2021_A
from moabb.paradigms import MotorImagery
paradigm = MotorImagery()

dataset = Beetl2021_A()
X, y, metadata = paradigm.get_data(dataset)
```

For more details see the [MOABB documentation](https://moabb.neurotechx.com/) and the
[MOABB dataset page](https://moabb.neurotechx.com/docs/generated/moabb.datasets.Beetl2021_A.html).

## Citation

If you use this dataset please cite the primary publication:

> DOI: [10.48550/arXiv.2202.12950](https://doi.org/10.48550/arXiv.2202.12950)

## NEMAR / MOABB Benchmark Collection

This BIDS-formatted dataset was converted from the original data using the
[MOABB](https://moabb.neurotechx.com/) pipeline and re-hosted on
[NEMAR](https://nemar.org/) as part of the MOABB benchmark collection.
The original data and license terms apply — see `dataset_description.json` for details.
