# OptionsPricingGroupProject
Options Pricing Group Project

For this project you will be examining European call option pricing data on the S&P 500. Recall, a European call option gives the holder the right (but not the obligation) to purchase an asset at a given time for a given price. Valuing such an option is tricky because it depends on the future value of the underlying asset.

The Black-Scholes option pricing formula provides an approach for valuing such options. Let K denote the strike price, i.e., the price one must pay to purchase the asset, and (tau) the time until expiration of the option. Suppose that the asset in question is currently trading at S, and has “volitility” (i.e., risk or standard deviation) of σ. Finally, suppose that the annual risk-free interest rate is r.
![image](https://user-images.githubusercontent.com/17756772/233691520-8274494c-12b6-4029-b174-67041b85059d.png)

The 1997 Nobel Prize in Economics was awarded for the Black-Scholes formula because it works remarkably well in practice. However, in this project we are going to attempt to build statistical/ML models to perform the same task. In this project, you should pretend that you don’t know the Black-Scholes formula when building your machine learning models.

You will find two data sets on Blackboard: option_train.csv and option_test_wolabel.csv. The training data set has information on 1,680 separate options. In particular, for each option we have recorded

•	Value (C): Current option value

•	S: Current asset value

•	K: Strike price of option

•	r: Annual interest rate

•	tau: Time to maturity (in years)

•	BS: The Black-Scholes formula was applied to this data (using some ) to get C_pred. and If an option has C_pred – C > 0, i.e., the prediction over estimated the option value, we associate that option by (Over); otherwise, we associate that option with (Under).

The test data set is similar except it has only 1,120 options and is missing the Value and BS variables. You can safely assume that the test data is of good quality, but you should check for missing and erroneous entries in the training data.
The core idea of the project is to use the training data to build statistical/ML models with
1)	Value as the response (i.e., a regression problem) and then

2)	BS as the response (i.e., a classification problem).
 


Page 1
 
DSO 530 Group Project

The other four variables will be used as the predictors. You will explore all of the regression (for Value) and classification (for BS) methods we have discussed in the course on the training data (you may also use methods we have not discussed, but this is not required). Ultimately you will select what you consider to be the most accurate approach and use it to make predictions for C and BS on the 1,120 options in the test data set. You will submit these two sets of predictions. I will compare these predictions in comparison to the actual Value and BS results on the test options (which I have), in terms of out-of-sample R squared and classification error, respectively.
![image](https://user-images.githubusercontent.com/17756772/233691600-905d8c7a-9dd9-4f6c-ad59-ed377652cd9a.png)
