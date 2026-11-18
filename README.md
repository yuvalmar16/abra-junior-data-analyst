# ABRA – Junior Data Analyst: image anomaly detection

Exploration of factory part images labelled by a human inspector, plus a simple, explainable
first-pass detector for suspicious (possibly defective) parts.

## Files
| file | content |
|---|---|
| `solution.ipynb` | the full solution (Parts A–E), with outputs saved |
| `predictions.csv` | one prediction per test image: `image_id,predicted_defect,score` |
| `train_verified.csv` | `train.csv` + manually verified labels: `verified_label`, `verified_type`, `review`, `review_comment` (written by the notebook; originals unchanged) |
| `train.csv`, `test.csv`, `images/` | the data provided with the assignment |
| `Junior Data Analyst.md` | the assignment brief (Hebrew) |

## How to run
```bash
python -m venv .venv
.venv\Scripts\activate          # Linux/Mac: source .venv/bin/activate
pip install numpy pandas opencv-python matplotlib scikit-learn
jupyter nbconvert --to notebook --execute --inplace solution.ipynb   # or open it in Jupyter and Run All
```
Run from this folder (the notebook reads `train.csv`, `test.csv` and `images/` relative to it).
It runs on a CPU in well under a minute.
