# Probabilistic-Load-Forecasting-with-Quantile-Regression
Exploration of GB, XGB, LGBM and NN's performance in probabilistic load forecasting

* The script is coded in Google Colab, thus there exist commands to retrieve files from and store files to google drive. Modification is required for any personal use.

* In this project, several models are explored for probabilistic load forecasting and performances are compared. For GB and LGBM, there are in-built quantile loss functions from respective libraries. For XGB, a customized loss function is needed to return gradient and hessian of the loss function for training. Similarly for NN, a customized loss function is required but it returns the quantile loss. 

* From the training result, NN has the tendency to overestimate the risk (prediction interval coverage probability (PICP) > prediction interval nominal coverage (PINC); the others show the opposite performance. NN is scalable by changing the number of outputs according to the quantiles and training time are not much affected wheares the others only support for single quantile thus, the training time increases proportionally to number of quantiles (The training time in ascending order: LGBM -> XGB -> GB). 
