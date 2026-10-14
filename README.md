# Ecnn graphs mineral

Novo link https://drive.google.com/drive/folders/1PFo1AklBpse2Tg4RbjPkNxztqyD_DMNY?usp=sharing


#### Article:   <small><strong>Interval-quota matchings in chain graphs</strong>  <a href=""><img src="https://cdn.simpleicons.org/doi/2dd4bf" alt="DOI" height="14" align="absmiddle"></a>  <a href=""><img src="https://cdn.simpleicons.org/zenodo/2dd4bf" alt="Zenodo" height="14" align="absmiddle"></a>  <a href="https://drive.google.com/drive/folders/1HGzCo9WKmTU7dlOZhaCHo8pxqkh0ZxLk?usp=sharing"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/google/google-original.svg" alt="Google Drive" height="14" align="absmiddle"></a></small>

We study exact quota-constrained matchings in Ferrers-ordered chain graphs. QuotaMatch gives integral flow for laminar quotas, a canonical $O(n+m)$ prefix construction, a shortest-path envelope for crossing intervals, and an $O(r+\ell)$ procedure for $r$ threshold classes and $\ell$ rise blocks. Labeled lifting takes $O(n)$ time including output. Feasibility is NP-complete when quota sets may use at most two intervals, even with universal neighborhoods, unit quotas, and two-element sets. The study comprises $193$ configurations, $20$ seeds, and $15{,}440$ method executions. QuotaMatch is compared with HiGHS-LP, HiGHS-MILP, and CP-SAT on $80$ prefix, $65$ interval, and $48$ laminar configurations. All four methods agree on feasibility in $3{,}860$ cases. For crossing intervals at $(n,m)=(8192,16384)$, QuotaMatch reduces mean wall time by $87.6\%$, $88.5\%$, and $99.9\%$ against HiGHS-LP, HiGHS-MILP, and CP-SAT, respectively. Each execution uses two untimed warm-ups and five measured repetitions, retaining the median wall time. In the largest plotted interval case, QuotaMatch averages $0.0487$ s with $139.5$ MiB mean process peak resident set size. On a balanced binary laminar tree with $n=1024$ and zero slack, all three solvers are faster than QuotaMatch.

#### Dependencies

* Python 3.11
* NumPy 1.26.4
* SciPy 1.13.1
* Matplotlib 3.9.2
* OR-Tools 9.6
* Protobuf 4.21.12
* PyYAML 6.0.2

#### Installation

```bash
docker compose -f docker/compose.yml build
docker compose -f docker/compose.yml run --rm quota
```

#### License (MIT)

* Copyright (c) alancampos-ai
* Code released under the MIT License.
