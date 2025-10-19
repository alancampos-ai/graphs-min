# airm-spd-kmeans-dti
Implementation and experiments for DTI segmentation using k-means on the SPD manifold with AIRM, Log-Euclidean, Euclidean, and a hybrid AIRM–Log-Euclidean metric.

<div align="center">
  <img src="airm_kmeans.png" alt="Banner do perfil" width="100%">
</div>

## Repository layout (expected)
- `src/`: core algorithms (`kmeans.py`, `utils.py`, `metrics.py`, `segment_dti.py`)
- `scripts/`: experiment runners (`build_dataset.py`, `sweep_alpha_dense.py`, `iteration_convergence.py`)
- `tests/`: statistical analysis and sanity checks (`wilcoxon_paired.py`, leakage checks, y-scramble)
- `results/` and `figures/`: generated artifacts (not tracked by git ideally)

## Environment
Use the provided `environment.yml`.

conda env create -f environment.yml
conda activate ned-loso
python -c "import numpy,scipy,sklearn,nibabel; print('ok')"
