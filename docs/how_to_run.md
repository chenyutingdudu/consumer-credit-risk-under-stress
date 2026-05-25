# How to Run

## 1. Install dependencies

```bash
pip install -r requirements.txt
```

## 2. Run the full pipeline

```bash
python run_all.py
```

## 3. Outputs

Results:

```text
results/dataset_summary.csv
results/model_metrics.csv
results/predictions_with_features.csv
results/stress_test_metrics.csv
results/subgroup_metrics.csv
results/bootstrap_loss_ci.csv
results/model_calibration.csv
results/threshold_sweep.csv
results/threshold_optimization.csv
results/model_comparison_bootstrap.csv
```

Figures:

```text
figures/model_accuracy.png
figures/expected_loss.png
figures/false_approval_rate.png
figures/stress_loss_comparison.png
figures/subgroup_loss.png
figures/bootstrap_loss_ci.png
figures/optimal_thresholds.png
figures/calibration_ece.png
```

## 4. Important Note

The first run attempts to download the real dataset from OpenML.
If network is unavailable, the pipeline automatically falls back to a synthetic credit-like dataset so experiments remain reproducible.

## 5. Restricted Environment Tip

In restricted environments, run with single-thread settings:

```bash
OMP_NUM_THREADS=1 MKL_NUM_THREADS=1 OPENBLAS_NUM_THREADS=1 NUMEXPR_NUM_THREADS=1 python run_all.py
```

## 6. Build a Distributable Release

After results and figures are generated:

```bash
python scripts/build_release_package.py
```

This creates:

- `release_bundle/` (organized copy of the project)
- `CREDIT_RISK_RESEARCH_PACKAGE_YYYYMMDD_HHMMSS.zip`