# IJIES EL-Fleet Reproducibility

This repository contains the panel-level analytical dataset and Python notebook prepared to reproduce the retained statistical and machine-learning analyses for the manuscript:

**From Correlation to Prediction: Electroluminescence-Based Indicators and Composite Health Scoring for Photovoltaic Power Loss Prediction in a 204-Panel Fleet**

## Repository contents

```text
IJIES-EL-PV-Fleet/
├── README.md
├── requirements.txt
├── IJIES_EL_PV_Fleet_204_Panels.csv
└── IJIES_EL_Fleet_Reproducibility.ipynb
```

### `IJIES_EL_PV_Fleet_204_Panels.csv`
Panel-level analytical dataset containing **204 PV-panel records** and the variables used by the reproducibility notebook.

### `IJIES_EL_Fleet_Reproducibility.ipynb`
Python/Jupyter notebook for the retained analytical workflow.

### `requirements.txt`
Python dependencies required to run the notebook.

## Scope of the reproducibility package

The notebook covers the retained panel-level workflow:

- dataset integrity and descriptive checks;
- Pearson and Spearman association analysis;
- 80/20 hold-out evaluation;
- 5-fold cross-validation;
- Linear Regression;
- Random Forest regression;
- Composite Health Score calculation;
- Health Score weight-sensitivity analysis; and
- comparison of association and internal predictive performance.

The package intentionally does not include post-review exploratory analyses outside the retained manuscript scope, such as bootstrap confidence intervals, repeated cross-validation, temporal validation, morphology ablation, or competing maintenance-ranking baselines.

## Analytical interpretation

The Composite Health Score is treated as a composite condition and maintenance-prioritisation index. Because its Power Performance Index component incorporates `Power_Loss`, the Health Score is not interpreted as an outcome-independent predictor of `Power_Loss`.

The hold-out and cross-validation results are internal validation within the available single-fleet dataset. They should not be interpreted as external validation across independent PV fleets, sites, module technologies, or environmental conditions.

## Main reproducibility settings

- Hold-out split: 80/20
- Cross-validation: 5-fold
- Linear Regression
- Random Forest: 300 trees
- Random Forest maximum depth: 5
- Random seed: 42

## How to run

1. Download or clone all repository files.
2. Keep `IJIES_EL_PV_Fleet_204_Panels.csv` and `IJIES_EL_Fleet_Reproducibility.ipynb` in the same directory.
3. Install the required Python packages:

```bash
pip install -r requirements.txt
```

4. Start Jupyter:

```bash
jupyter notebook IJIES_EL_Fleet_Reproducibility.ipynb
```

5. Run the notebook cells sequentially from top to bottom.

The notebook expects the following dataset filename:

```text
IJIES_EL_PV_Fleet_204_Panels.csv
```

## Citation

If this repository is used in academic work, please cite the associated IJIES article after its final bibliographic information becomes available.


## License

No reuse license is declared unless explicitly added by the authors. Please contact the corresponding author regarding reuse beyond reproducibility review.
