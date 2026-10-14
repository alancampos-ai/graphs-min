# Graph min

#### Article: <small><strong>E-CNN</strong></small>  <a href="https://doi.org/10.1016/j.cam.2026.117584"><img src="https://cdn.simpleicons.org/doi/2dd4bf" alt="DOI" height="14" align="absmiddle"></a>  <a href="https://doi.org/10.1016/j.cam.2026.117584"><img src="https://cdn.simpleicons.org/zenodo/2dd4bf" alt="Zenodo" height="14" align="absmiddle"></a>  <a href="https://drive.google.com/drive/folders/1YBVxdJ12ujfiddyKyu-Z6pwpmwWGmsDr?usp=drive_link"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/google/google-original.svg" alt="Google Drive" height="14" align="absmiddle"></a></small>

Experiments on six-channel symmetric tensor-field datasets evaluate conventional, group-equivariant, continuous-equivariant, and gauge-equivariant encoder-decoder CNNs under a common computational setting. The implementation includes four conventional variants: `plain`, composed of two-convolution GroupNorm-SiLU blocks; `plain_rot`, the same architecture trained with rotational augmentation; `plain++`, a nested architecture with dense multiscale skip paths; and `plain++_rot`, its rotationally augmented counterpart.

The discrete equivariant family comprises the cyclic variants `c4_norm`, `c4_pointwise`, `c5_norm`, `c6_norm`, `c7_norm`, `c8_norm`, `c8_pointwise`, `c8_quotient`, and `c16_norm`, together with the dihedral variants `d4_norm`, `d4_pointwise`, `d8_norm`, `d8_pointwise`, and `d8_quotient`. The networks use `escnn` equivariant convolutions with regular or quotient representations and norm-based or pointwise nonlinearities.

The continuous equivariant family includes `so2_norm` and `so2_gated` for (SO(2)), as well as `o2_norm`, `o2_gated`, `o2_induced_norm`, and `o2_induced_gated` for (O(2)). The architectures combine pure or induced representations with norm-based or gated nonlinearities.

The `gauge` architecture constructs local frames from the order-two tensor components, modulates geometric connections using frame confidence, and applies residual `GemConv` blocks with parallel-transport pooling and unpooling. The implementation also includes gauge-confidence ablations.

The experimental scripts support cross-validation over configurable data subsets, multiple random seeds, deterministic internal validation partitions, probability ensembles, rotational test-time augmentation, and validation-based temperature scaling. Evaluation includes IoU, F1/Dice, Precision, Recall, Accuracy, predictive entropy, expected calibration error, negative log-likelihood, Brier score, variance across seeds, AURC, EAURC, execution time, peak memory usage, and the selected training epoch. Additional scripts evaluate equivariance deviations for cyclic, dihedral, (SO(2)), (O(2)), and gauge-equivariant networks, together with tensor-field consistency and gauge-isotropy stability.

#### Dependencies

* Python >= 3.9
* numpy
* scipy
* nibabel
* dipy
* matplotlib
* torch
* escnn
* torch-geometric
* torch-scatter
* torch-cluster
* torch-sparse
* tqdm
* opt-einsum
* trimesh
* pytorch-ignite
* openmesh

#### Bash

```bash
pip install numpy scipy nibabel dipy matplotlib escnn
pip install torch
pip install torch-geometric torch-scatter torch-cluster torch-sparse
pip install tqdm opt-einsum trimesh pytorch-ignite openmesh
pip install -e src
```

#### License (MIT)

* Copyright (c) alancampos-ai
* Code released under the MIT License.
 
