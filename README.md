# Mushroom Classification (Edible vs Poisonous)

## Project Overview
This project predicts whether a mushroom is edible or poisonous from its physical
features (cap shape, odor, gill size, habitat, etc.). It compares two beginner-friendly
models: a Decision Tree and K-Nearest Neighbors (KNN). This is useful because eating
the wrong wild mushroom can be dangerous, so an accurate classifier shows how ML can
support safety decisions.

## Dataset
UCI Mushroom dataset: https://archive.ics.uci.edu/dataset/73/mushroom
- 8,124 mushrooms, 22 features, 1 target (edible / poisonous)
- Missing values are marked with `?` (only in `stalk-root`, 2,480 rows) and were
  treated as their own "unknown" category.

## Setup Instructions
1. Clone this repo: `git clone https://github.com/chirantana2007-del/mushroom-classification.git`
2. Install the libraries: `pip install pandas numpy matplotlib scikit-learn jupyter`
3. Open `mushroom_classification.ipynb` in Jupyter Notebook or Google Colab
4. Run all cells (the dataset is loaded directly from the UCI link, so no download is needed)

## Results
| Model | Accuracy |
|---|---|
| Decision Tree | 1.0000 (100%) |
| KNN (k=5) | 0.9982 (99.82%) |

Confusion matrix on the 1,625-sample test set:
- Decision Tree: 0 mistakes
- KNN: 3 mistakes (edible predicted as poisonous). Neither model predicted a
  poisonous mushroom as edible.

## Conclusion
The Decision Tree performed better (0 errors vs 3 for KNN). Both models reached
near-perfect accuracy because the mushroom features are very informative. I learned
to encode categorical data, to check for hidden missing values (`?`), and that the
confusion matrix matters more than accuracy alone when one type of error is more
dangerous than the other.
