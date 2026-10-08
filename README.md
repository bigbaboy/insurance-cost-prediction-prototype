# Medical Insurance Cost Prediction — Academic Prototype

A Streamlit coursework prototype exploring preprocessing and a regression-based interface for insurance-cost estimation.

**Current status: incomplete runnable package.** The application expects `model/model.pkl`, but that model file is not present in the reviewed repository. It stops before displaying the prediction interface when the file is missing.

## Existing implementation

- Load `insurance.csv`.
- Encode sex, smoking status and region as categorical indicators.
- Standardize age, BMI and number of children for an exploratory data path.
- Show preprocessing output and training/test split dimensions.
- Apply an IQR-based adjustment to the target in the exploratory code.
- Load a serialized regression model and provide a Streamlit input form for predictions when the model is available.

## Repository contents

| File | Purpose |
| --- | --- |
| `app.py` | Data preparation and intended inference interface |
| `insurance.csv` | Source dataset supplied in the repository |
| `requirements.txt` | Python dependencies |

## Setup and current blocker

```bash
git clone https://github.com/bigbaboy/Group2.git
cd Group2
python -m venv .venv
```

Activate the environment, then:

```bash
python -m pip install -r requirements.txt
python -m streamlit run app.py
```

These commands launch the script, but do not resolve the missing model. The application reports the missing artifact and stops.

## Work required for a reproducible demo

- [ ] Recover or implement the training pipeline and document its feature contract.
- [ ] Generate the expected model artifact or change the application to load a unified preprocessing-and-model pipeline.
- [ ] Align training and inference scaling, feature order and constant/intercept handling.
- [ ] Save train/test metrics with the split, seed and dependency versions.
- [ ] Test input validation and missing-file behavior.

The current prediction form constructs raw numerical inputs while the exploratory code scales numerical fields. Compatibility with the missing model cannot be established from the available files. No accuracy, cost-saving outcome or production readiness is claimed.

**Context:** Academic work; collaborator roles and the original training artifact need to be documented. This repository is better presented as work in progress than as a completed deployed product.
