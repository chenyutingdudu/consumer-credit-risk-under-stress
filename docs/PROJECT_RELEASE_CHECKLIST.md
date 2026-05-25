# Project checklist (technical)

Use before tagging a release or archiving a frozen copy of results.

## A. Research artifacts

- [ ] References and notation are consistent  
- [ ] Hypotheses and limitations match the final analysis  

## B. Code and data

- [ ] `src/` runs end-to-end without debug-only code paths  
- [ ] `requirements.txt` installs in a clean environment  
- [ ] `data/uci_credit_card_default.csv` is present or data acquisition steps are documented  
- [ ] `docs/how_to_run.md` matches current behavior  

## C. Experimental outputs

- [ ] `results/model_metrics.csv`  
- [ ] `results/stress_test_metrics.csv`  
- [ ] `results/subgroup_metrics.csv`  
- [ ] `results/bootstrap_loss_ci.csv`  
- [ ] `results/model_calibration.csv`  
- [ ] `results/threshold_sweep.csv`  
- [ ] `results/threshold_optimization.csv`  
- [ ] `results/model_comparison_bootstrap.csv`  

## D. Figures

- [ ] `figures/model_accuracy.png`  
- [ ] `figures/expected_loss.png`  
- [ ] `figures/false_approval_rate.png`  
- [ ] `figures/stress_loss_comparison.png`  
- [ ] `figures/subgroup_loss.png`  
- [ ] `figures/bootstrap_loss_ci.png`  
- [ ] `figures/optimal_thresholds.png`  
- [ ] `figures/calibration_ece.png`  

## E. Documentation

- [ ] `README.md` is accurate for a first-time reader  

## F. Archive (optional)

- [ ] Run `python scripts/build_release_package.py` to produce `release_bundle/` and a timestamped zip in the project root  
