# forecasting-test-harness

Create a workflow for forecasting multiple coherent time series with mutiple candidate models.

## For a single time series

  1. Generate pool of candidate forecasts (on training set). E.g with different orders of ARIMA, different parameters for Holt-Winters.
  1. Evaluate forecast perforamnce (e.g. RMSE) on validation set. Choose some subset of the forecast pool to retain.
  1. Re-train models on train+validation set. Forecast for test set horizon. Combine (e.g. simple average) the forecasts and evaluate the result vs the test set.

## For forecast reconciliation

  1. Reconcile hierarchical time series
