# COMP9417-xRFM-Project

It is built for:

- official **xRFM** library integration

- at least **5 datasets** with assignment coverage checks

- baseline comparisons against **XGBoost / Random Forest / MLP**

- **AGOP** interpretability analysis

- **scaling experiments** on a large dataset

- reproducible, config-driven experiment runs

  

## Dataset coverage

This selection is intended to satisfy the project constraints:

- at least **5** tabular datasets
- at least **2 regression** tasks
- at least **2 classification** tasks
- at least **1 dataset with n > 10,000**
- at least **1 dataset with d > 50**
- at least **1 dataset with mixed feature types**



## Final dataset list

| Dataset                                                      | Task                         | n     | d    | Mixed Feature Type                  | Satisfied Requirements       | Target              |
| :----------------------------------------------------------- | ---------------------------- | ----- | ---- | ----------------------------------- | ---------------------------- | ------------------- |
| [Forest Fires](https://archive.ics.uci.edu/dataset/162/forest%2Bfires?utm_source=chatgpt.com) | Regression                   | 517   | 12   | Integer ,Categorical,Continuous     | Regression,mixed             | area                |
| [Metro Interstate Traffic Volume](https://archive.ics.uci.edu/dataset/492/metro+interstate+traffic+volume) | Regression                   | 48204 | 8    | Categorical,Continuous,Integer,Date | Regression,mixed,n>10000     | traffic_volume      |
| [Superconductivty](https://archive.ics.uci.edu/dataset/464/superconductivty+data) | Regression                   | 21263 | 81   | Continuous,Integer                  | Regression,n>10000,d>50      | critical_temp       |
| [NATICUSdroid (Android Permissions)](NATICUSdroid (Android Permissions)) | Classification               | 29333 | 86   | Integer                             | classification,n>10000,d>50  | Result              |
| [Secondary Mushroom Dataset](https://archive.ics.uci.edu/dataset/848/secondary%2Bmushroom%2Bdataset?utm_source=chatgpt.com) | Classification               | 61068 | 20   | Categorical,Continuous              | classification,mixed,n>10000 | class               |
|                                                              |                              |       |      |                                     |                              |                     |
| [AI4I 2020 Predictive Maintenance](https://archive.ics.uci.edu/dataset/601/ai4i+2020+predictive+maintenance+dataset) | ?Classification, Regression, | 10000 | 6    | Continuous,Integer                  | classification               | Machine failure,TWF |





## Project structure

```
project/
├─ configs/
├─ data/
├─ docs/
├─ report/
├─ src/
├─ tests/
├─ notebooks/
└─ results/
```

## Install

```
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

### With GPU

If a GPU is available, it is highly recommended to use either the 'cu11' or 'cu12' extra requirement. These versions offer significantly accelerated Product and Lpq Laplace Kernels. With CUDA-11 use:

```
pip install xrfm[cu11]
```

or, with CUDA-12:

```
pip install xrfm[cu12]
```

### General Installation

```
pip install xrfm
```



## Quick Start

```

```



## 🗺️ Roadmap

- [x] upload dataset
- [ ] Data preprocess

- [ ] Write Report introduction

- [ ] Write Report **Methodology**

- [ ] Regression Compare

- [ ] Classification Compare

- [ ] Result

  - [ ]  Present a results table with datasets as rows and (model, metric) pairs as columns
  - [ ] On one dataset, perform an interpretability comparison: extract the AGOP diagonal from each xRFM leaf and
    compute PCA loadings, mutual information scores, and permutation importance on the same data. Where
    do the methods agree and where do they diverge?
  - [ ] On one large dataset (n > 10, 000), subsample the training set at several sizes and plot test performance and
    training time versus n for all models

- [ ] Write Report Result 

- [ ] Write Discussion

- [ ] Bonus:

- **Bonus (+10%).** Implement the AGOP-based splitting criterion from scratch (without using xRFM library internals)

  and verify it selects the same split direction as the library on a small dataset. Include this in an appendix with a brief

  explanation. If you attempt this bonus section, please indicate on your title page by adding ”+bonus” in the project

  title.

- [ ] Write final report