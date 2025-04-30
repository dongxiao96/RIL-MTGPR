# RIL-MTGPR (Robust Impact Localisation - Multi-task Gaussian Process Regression)
# Impact Localization Dataset for Composite Panels using TDOA and GPR

This repository contains a subset of experimental data and code associated with the paper submitted to the journal *Structural Health Monitoring*, titled:

**"Robust impact localisation on composite aerostructures using kernel design and Bayesian-inspired model averaging under environmental and operational uncertainties"**

## Overview

The data provided here supports the development and validation of a Multi-task Gaussian Process Regression (GPR)-based impact localization framework using Time-Difference-of-Arrival (TDOA) features from guided wave signals. All experiments were conducted on a flat composite panel using piezoelectric (PZT) sensors.

This repository includes:

- Selected impact datasets (TDOA features only)
- Reference code for a baseline GPR method using the RBF kernel

## Dataset Description

The following cases are included:

| Code | Description                       | Condition         | 
|------|-----------------------------------|-------------------|
| `REF`| 35 distributed impacts (training) | Room temp, 6 PZTs | 
| `HEI`| 35 impacts with varied height     | Room temp, 6 PZTs | 
| `ANG`| 35 impacts with varied angle      | Room temp, 6 PZTs | 
| `TEM`| 35 impacts at increased temperature | 80°C, 6 PZTs    |

### Data Format
All TDOA data are stored in `.mat` files organized by case:
- `TDOA_*.mat` files include:
  - `TTDOAs`: A matrix of shape `(N_impacts x N_features)`
  - `implocs`: Impact location coordinates (in mm), shape `(N_impacts x 2)`
  - `senlocs`: Sensor locations, shape `(N_sensors x 2)`


## Code
- `GPR_impact_localisation.ipynb`: A baseline GPR model using the radial basis function kernel, for reproducibility.

> **Note:** Full source code for the proposed method is not included to protect intellectual property. For transparency, pseudocode and a flowchart are provided in the manuscript.

## Usage Instructions

1. Clone the repository:

```bash
git clone https://github.com/dongxiao96/RIL-MTGPR.git
cd RIL-MTGPR
```

## Citation

If you use this dataset or code, please cite the paper once published. Preprint or DOI will be added here.


## License
This dataset is shared under the CC BY-NC 4.0 License. For academic, non-commercial use only.