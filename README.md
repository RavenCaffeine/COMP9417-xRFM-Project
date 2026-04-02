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
| [Forest Fires](https://archive.ics.uci.edu/dataset/162/forest%2Bfires?utm_source=chatgpt.com) | Regression                   | 517   | 12   | Integer ,Categorical,Continuous     | regression,mixed             | area                |
| [Metro Interstate Traffic Volume](https://archive.ics.uci.edu/dataset/492/metro+interstate+traffic+volume) | Regression                   | 48204 | 8    | Categorical,Continuous,Integer,Date | classification,mixed,n>10000 | traffic_volume      |
| [Superconductivty](https://archive.ics.uci.edu/dataset/464/superconductivty+data) | Regression                   | 21263 | 81   | Continuous,Integer                  | classification,n>10000,d>50  | critical_temp       |
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

