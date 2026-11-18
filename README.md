# IPO Grey Market Premium (GMP) & Listing Outcome Analysis

## Project overview
An exploratory analysis of IPO grey market premium (GMP) and listing outcomes. The project examines whether pre-listing indicators are associated with subsequent listing performance while highlighting the timing of information availability.

## Business questions
- How are observed GMP values distributed across IPOs?
- How do GMP-based implied prices compare with actual listing prices?
- How does the relationship vary across IPOs and market periods?
- Can pre-listing information provide a useful, properly validated signal?

## Existing files
- `GMP.ipynb` — original analysis notebook.
- `gmp.csv` — IPO/GMP dataset.

## Critical modelling control: prevent target leakage
A prediction made before listing may use only information available at that prediction timestamp. Actual listing price, listing gain, post-listing profit and any fields calculated from those outcomes must never be used as predictors for a pre-listing forecast. They may be used as outcomes for evaluation.

## Improvement plan
1. Document each column, its definition and the timestamp when it becomes available.
2. Validate price, GMP and percentage calculations.
3. Define the prediction target and prediction cut-off time.
4. Use chronological validation where the sample size permits; avoid random leakage across time.
5. Compare against a simple baseline and report MAE/RMSE or classification metrics suited to the target.
6. Explain sample-size limitations and the influence of market sentiment.

## Tools
Python, pandas, NumPy, scikit-learn and visualisation libraries used in the notebook.

## Disclaimer
GMP is an informal, unofficial indicator and is not a regulated or guaranteed measure of listing performance. This project is educational and is not investment advice.
