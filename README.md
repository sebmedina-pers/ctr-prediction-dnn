# CTR Prediction (Criteo DAC)

Local, incremental ML project using the **Criteo Display Advertising Challenge (dac-v1)** dataset to prepare for a **Senior Data Scientist (ad-tech)** interview.

## Scope (incremental)

We will build this step-by-step (EDA → simple baselines → efficient preprocessing for high-cardinality categoricals → embeddings/DNNs → training/eval pipelines → ML-systems considerations).

**Important constraints:** the dataset is very large; avoid loading full files into memory or duplicating them.

## Dataset

The dataset lives in `criteo_advertising_dataset/` and is **ignored by Git**.

Schema (tab-separated):

- Train: `label` + `I1..I13` (integer) + `C1..C26` (categorical, hashed)
- Test: `I1..I13` + `C1..C26` (no label)

Missing values are represented as empty fields.

## Environment

We keep a local virtual environment at `.venv/` (also ignored by Git).

Once you have a working `python3` installed, create and populate the venv:

```bash
python3 -m venv .venv
./.venv/bin/python -m pip install --upgrade pip
./.venv/bin/pip install -r requirements.txt
```

## Repo layout

```text
ctr-prediction-dnn/
├── criteo_advertising_dataset/   # not tracked
├── notebooks/
├── src/
├── tests/
├── README.md
├── .gitignore
└── requirements.txt
```

