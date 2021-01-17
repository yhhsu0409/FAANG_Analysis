# FAANG_Analysis
It would be important to dive into FAANG since they stand as the top 5 technology companies in America. In this report, statistical analysis will be used to evaluate FAANG. The analysis will begin with evaluating on different risks of FAANG. Next, Capital Asset Pricing Model (CAPM) and Fama-French Model will be used to estimate the excess return that FAANG could bring compare to the market. Finally, time series analysis will be used to forecast the FAANG.

## Data
* Recieve FAANG historical stock price by using **yfinance** package
* Time span: 2012-05-18 to 2020-10-09 

## Risks
* Standard Deviation (STD), Downside Deviation, Value at Risk (VaR), Expected Shortfall (ES), Maximum Drawdown (MDD) will be discussed
* FAANG_trend.ipynb
<img src="https://github.com/yhhsu0409/FAANG_Analysis/blob/master/Figures/FAANG_Risks/FAANG_Risks_Conclusion.png" width="800" height="500">

## Capital Asset Pricing Model (CAPM)

Risks can be categorized as systematic, and unsystematic risk. Systematic risk is the one that can affect the entire market, which is beyond the control of an individual and can’t be diversified. For example, macroeconomic risks such as inflation, political crisis, and natural disasters are consider as unsystematic risks. On the other hand, systematic risk is the risk that can be prevented, or can be diversified through asset allocation. For example, risks that only affect individual firm or sector, such as failure of product development, and the drop of real estates during recession, respectively.
Since systematic risk can’t be diversified, it is required for a risk premium. Therefore, there should be a relation between the risk premium and the return of the market. CAPM is the model that build under this relation.
* FAANG CAPM.ipynb
<img src="https://github.com/yhhsu0409/FAANG_Analysis/blob/master/Figures/CAPM/FAANG_CAPM.png" width="800" height="500">

## Fama-French Three Factor Model

Even though CAPM gives an nice relation between risk premium and expected return of an asset, but risk-premium by itself can’t explain the expected return completely. In 1993, Fama and French adds market equity and book-to-market-equity ratio (B/M) as additional two factors for the explanation of expected return. The reason for market equity as a factor can refer to the research of Banz’s in 1981, where he found out that a firm with smaller market equity will have better performance than the market, and the reason for book-to-market-equity ratio as a factor can refer to the research of Stattman, where he found out that firm with higher B/M ratio tends to have higher peroformance than the market.

* FAANG Fama French.ipynb

## Stock Price Forecast

In previous sections, expected return of a stock have been discussed by using CAPM and Fama-French model. However, the models can only give the investors a point estimate, which is not quite enough. In this section, the stock price of FAANG will be forecasted through ARIMA model, so that the investors could have a general idea on how the stock will progress with time.

* FAANG ARIMA.ipynb

e.g. Facebook Forecast
<img src="https://github.com/yhhsu0409/FAANG_Analysis/blob/master/Figures/Forecasts/FB_forecast.png" width="800" height="500">


## GARCH
After evaluating the forecasts, it shows that the residuals aren’t white noise; therefore, there’s still something missing in the model.

One possible reason is the ARCH effect, where the volatility are not constant over time (homoskedasticity); instead, it’s changing over time (heteroskedasticity). Volatility is important since it may be a representation of risk. Investors will want to trade stocks while the volatility of an asset is low. Therefore, the analysis on volatility is also an important part. Here, GARCH model will be used to evaluate the volatility of the daily return.

e.g. Amazon GARCH
<img src="https://github.com/yhhsu0409/FAANG_Analysis/blob/master/Figures/GARCH/AMZN_GARCH.png" width="800" height="500">

## Final Report

* Final Report can be found in the **Final FAANG Report.pdf**
* In addition, a detailed version of the report can be found in **FAANG_Report__Detail_and_Code_Included_Version_.pdf**<br>
  The difference is that the detailed version dives into the math and code of the project.







