# Baseball salary prediction

Predict baseball players’ salaries from seasonal and career performance statistics, in the spirit of a Moneyball-style analysis of the transfer market.

## Data

`cs_05.csv` includes batting and fielding stats (`AtBat`, `Hits`, `HmRun`, `Runs`, `RBI`, `Walks`, career totals, `Years`, `League`, `Division`, `PutOuts`, `Assists`, `Errors`) and `Salary`.

## Method

`Decision_Tree.ipynb` prepares the data (including a Box-Cox transform of the target in the reported comparison) and trains:

- Linear regression
- Ridge regression
- Decision tree
- Random forest
- Stochastic gradient boosting (SGB) regressor

Models are compared on RMSE, MAPE, MAE, and other absolute-error summaries.

## Findings

In the notebook’s Box-Cox comparison table, the SGB regressor had the lowest RMSE (202.4) and MAPE (34.2), ahead of random forest (RMSE 208.4, MAPE 36.2) and a decision tree (RMSE 231.5, MAPE 40.9). Linear and ridge models were weaker on this split. These figures are from the committed notebook outputs.

## How to run

```bash
jupyter notebook Decision_Tree.ipynb
```
