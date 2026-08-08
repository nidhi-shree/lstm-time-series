# LSTM Time Series Forecasting

This project builds an LSTM model to forecast atmospheric CO2 levels using
weekly data from the Mauna Loa Observatory (1958-2001).

## What's in this folder

- `lstm_time_series.ipynb` - the main notebook, already run with all outputs
  (plots, metrics, model summary) saved inside it. Just open and read, no
  need to re-run anything unless you want to.
- `build_nb.py` - the script used to generate the notebook cells. You don't
  need this to view the results, it's just here for reference.

## About the data

The dataset comes straight from `statsmodels` (`sm.datasets.co2`), so there's
no file to download or link to keep track of. It loads directly in the
notebook. 

## What the notebook covers

1. Loading and cleaning the data (a few missing weeks get filled in)
2. Scaling the values and turning the series into sequences
3. Building a 4-layer LSTM model with dropout after each layer
4. Training it and tracking the loss
5. Checking how good the predictions are (RMSE, MAE, MSE)
6. Plotting the loss curve and actual vs predicted values
7. Trying out a few different hyperparameters to see what works better
8. A short write-up at the end explaining the model choices

## How to run it

If you want to re-run it yourself:

```
pip install tensorflow-cpu scikit-learn statsmodels pandas matplotlib
jupyter notebook lstm_time_series.ipynb
```

Training takes a few minutes on a normal CPU.

That's about it. The notebook has comments and short text cells along the
way explaining what each part is doing, so it should be easy to follow even
if you're just skimming through.
