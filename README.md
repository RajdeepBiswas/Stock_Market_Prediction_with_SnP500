---
page_type: 
- Complete Solution
languages:
- Python
products:
- Azure Machine Learning | Azure Blob Storage
description: 
- The core purpose of this project is to predict the future price of a given stock and/or sector.
urlFragment: "https://github.com/RajdeepBiswas/Stock_Market_Prediction_with_SnP500"
---

# STOCK MARKET PREDICTION WITH S&P 500 DATA
![stock-exchange](images/stock-exchange.jpg)

## Domain

  We are going to work within the financial economics domain, more specifically with stock price and fundamentals data. Financial economics is the branch of economics characterized by a concentration on monetary activities, in which “money of one type or another is likely to appear on both sides of a trade”. Its concern is thus the interrelation of financial variables, such as prices, interest rates and shares, as opposed to those concerning the real economy (Financial_economics).  
  Stock market prediction is the act of trying to determine the future value of a company stock or other financial instrument traded on an exchange. The successful prediction of a stock's future price could yield significant profit (Stock_market_prediction).  Most stock traders nowadays depend on Intelligent Trading Systems which help them in predicting prices based on various situations and conditions, thereby helping them in making instantaneous investment decisions.  
  This work disagrees with the efficient-market hypothesis which suggests that stock prices reflect all currently available information and any price changes that are not based on newly revealed information thus are inherently unpredictable (Efficient-market_hypothesis).  

**Before we go further a note on stocks and shares:**  
A **share** is an indivisible unit of capital, expressing the ownership relationship between the company and the shareholder. The denominated value of a share is its face value, and the total of the face value of issued shares represent the capital of a company, which may not reflect the market value of those shares (Share_(finance)).  
The income received from the ownership of shares is a **dividend**. When a corporation earns a profit or surplus, it is (optionally) able to pay a proportion of the profit as a dividend to shareholders (Dividend).  
**Stock** (also capital stock) is all the shares into which ownership of a corporation is divided. In American English, the shares are collectively known as "stock". A single share of the stock represents fractional ownership of the corporation in proportion to the total number of shares (Stock).  

**Stock lingos that we need to know:**  
**Share price:** The stock price is the highest amount someone is willing to pay for the stock, or the lowest amount that it can be bought for (Share_price).  
**EPS:** Earnings per share (EPS) is calculated as a company's profit divided by the outstanding shares of its common stock. The resulting number serves as an indicator of a company's profitability (eps).  
**P/E ratio:** The price-to-earnings ratio (P/E ratio) is the ratio for valuing a company that measures its current share price relative to its per-share earnings (EPS). The price-to-earnings ratio is also sometimes known as the price multiple or the earnings multiple (price-earningsratio).  
**Dividend yield:** The dividend yield, expressed as a percentage, is a financial ratio (dividend/price) that shows how much a company pays out in dividends each year relative to its stock price (dividendyield).  
**Market Cap:** Market capitalization refers to the total dollar market value of a company's outstanding shares of stock. Commonly referred to as "market cap," it is calculated by multiplying the total number of a company's outstanding shares by the current market price of one share (marketcapitalization).  
**EBITDA:** EBITDA, or earnings before interest, taxes, depreciation, and amortization, is a measure of a company's overall financial performance and is used as an alternative to net income in some circumstances. EBITDA, however, can be misleading because it strips out the cost of capital investments like property, plant, and equipment (ebitda).  
**P/S ratio:** The price-to-sales (P/S) ratio is a valuation ratio that compares a company’s stock price to its revenues. It is an indicator of the value that financial markets have placed on each dollar of a company’s sales or revenues.  
**P/B ratio:** Companies use the price-to-book ratio (P/B ratio) to compare a firm's market capitalization to its book value. It is calculated by dividing the company's stock price per share by its book value per share (BVPS). An asset's book value is equal to it’s carrying value on the balance sheet, and companies calculate it netting the asset against its accumulated depreciation.  
Stock Prices are very dynamic and susceptible to quick changes because of the underlying nature of the financial domain and in part because of the mix of known parameters (Previous Day’s Closing Price, P/E Ratio etc.) and unknown factors (like Election Results, Rumors etc.)  

## Contents

| File/folder       | Description                                |
|-------------------|--------------------------------------------|
| `notebook`        | Python Notebooks.                          |
| `data`            | S&P 500 stock data.                        |
| `images`          | Sample images used for documentation.      |
| `.gitignore`      | Define what to ignore at commit time.      |
| `CHANGELOG.md`    | List of changes to the sample.             |
| `CONTRIBUTING.md` | Guidelines for contributing to the sample. |
| `README.md`       | This README file.                          |
| `LICENSE`         | The license for the sample.                |

## Data
High-quality financial data is expensive to acquire and is therefore rarely shared for free. My goal is to make the following dataset free of errors and make it available to everyone at no cost.  
For this project, I am extracting the daily trading and fundamentals data for the companies that comprise the S&P 500 (sp-500). The S&P 500 Index, or the Standard & Poor's 500 Index, created in 1957 is widely regarded as the best single gauge of large-cap US equities. It is a market-capitalization-weighted index of the 500 largest publicly traded companies in the U.S and covers approximately 80% of available market capitalization. It is not an exact list of the top 500 U.S. companies by market capitalization because there are other criteria to be included in the index (sp500).  

**Data Sources and Description:**
1.	Daily Stock Prices  
Source: pandas-datareader remote data access  
File Name Format: <Ticker Symbol>_<Start Date>_<End Date>_data.csv  
Example: AAPL_09-01-2016_09-01-2021_data.csv  
2.	Stock Split Action  
Source: pandas-datareader remote data access  
File Name Format: <Ticker Symbol>_<Start Date>_<End Date>_splits.csv  
Example: AAPL_09-02-2016_09-02-2021_splits.csv  
3.	Stock Dividend  
Source: pandas-datareader remote data access  
File Name Format: <Ticker Symbol>_<Start Date>_<End Date>_dividend.csv  
Example: AAPL_09-02-2016_09-02-2021_dividend.csv  
4.	Sector Information  
Source: https://datahub.io/  
File Name: snp500_sector.csv  
5.	Financial Information  
Source: https://datahub.io/  
File Name: snp500_financial.csv  

## Research Questions? Benefits? Why analyze these data?  
The core purpose of this project is to predict the future price of a given stock. This is what a trader does day in and day out. They would predict a stock price would go up or down based on their research and optionally using systems. Based on the analysis they would open a position on that stock and optimize their profit. A highly accurate stock prediction system augmented with in depth technical knowledge can be used to open positions with a higher chance of profits.  

**Research Questions:**  
* Will the stock go up or down in the future (day/week/month/year)?
* Will the sector go up or down in the future (day/week/month/year)?
* Top 10 value stocks in S&P 500?
* Top 10 growth stocks in S&P 500?
* Top 10 income stocks in S&P 500?
* Stretch Goal: A starter portfolio?
* Next Phase of this project can be sentiment analysis on Stock market news.
* Next Phase of this project can consider mid cap or small cap market.
* Next Phase of this project can consider cryptocurrency.

**Why analyze these data?**  
	I think the answer boils down to why invest in stock. There is a lot of literature out there on this but for me below would be the top 3 reasons (why-invest-in-stocks).  
1.	Potentially beat the inflation: The ability to protect your wealth from inflation, as the returns often significantly outpace the rate of inflation.
2.	Liquidity: The ease of buying and selling, which makes stocks a more liquid investment compared to other options like real estate.
3.	Low Startup Cost: The ability to start small. Thanks to $0 commissions and the ability to buy fractional shares with many online brokers, investors can begin purchasing stocks with a little bit of money.

## What Method?  
Before going into the methods, I would like to call out that the research will have at the very least embody the following principles (responsible-ai):  
* Fair - AI must maximize efficiencies without destroying dignity and guard against bias.
* Accountable - AI must have algorithmic accountability.
* Transparent - AI systems must be transparent and understandable.
* Ethical - AI must assist humanity and be designed for intelligent privacy.

The S&P 500 and company datasets are extraordinarily rich in nature and a lot of interesting data science and exploratory  data analytics analysis can be done using it. In this project the following methodology is followed:
1.	Raw data is extracted using API calls using Python notebooks and stored in the bronze layer of the data lake.
2.	Data transformation and cleansing happened using python from Raw to Processed stage and data is stored in the silver layer.
3.	Finally, the processed data is  flattened by joining using standard taxonomy in a serving layer. This is the gold layer of the data lake and will be used in the applications and the visualizations. 
4.	After the data is processed, we started the analysis by calculating trading indicators. These are nothing but mathematical calculations which can help traders identify certain signals and trends within the market. By no means we exhaustive since there are hundreds of trading indicators.
5.	Next, we plotted the classic interactive OHLC chart — a chart with bars Open, High, Low, Close prices, that we are used to seeing on trading platforms.  
6.	After the visualization section we moved on to the Prediction section which consisted of the following steps:  
	Prep the data  
	Train Test Split  
	Baseline Model Creation   
	Regression Model creation  
	Train the model  
	Evaluate the model  
Please note the model was simplistic in nature and more experimentation and sophisticated models are needed to better support this project and avoid overfitting problems.   
7.	This is the most exciting step of the project. And this is all about operationalizing the model and generate the profit via a simple strategy.  
	Strategy: If our model predicts a higher closing value than the opening value we make a trade for a single share on that day—buying at market open and selling just before market close.  
	Assumptions  
	Results of Simulated Investment  
8.	This is the correct time to do fundamental analysis which evaluates a company's past performance as well as the credibility of its accounts. Following steps were performed for the fundamental analysis:  
	Prep the data  
	Top 10 value stocks in S&P 500?  
	Top 10 growth stocks in S&P 500?  
	Top 10 income stocks in S&P 500?  
9.	Create an AutoML timeseries forecast model.   
	Get the performance metrics.  
	Get the model explanation.  
10.	Models are deployed in Azure Container Instance (container-instances) and exposed in REST endpoints which can be used in any programming language. It can also scale out as required without any infrastructure maintenance overhead. Note we can also deploy it in Azure Kubernetes Service (kubernetes-service), we just avoided it since we do not need spend extra money for dedicated containers for this scenario.  
11.	Client scripts written in python to call the REST endpoint with authentication (consume-web-service)and get back the results. This is how we will operationalize the model. In a real-world environment this REST APIs will be embedded in an application or dashboard generating near real time BUY/SELL alerts.

Prediction methodologies fall into three broad categories and often overlap. They are fundamental analysis, technical analysis (charting) and machine learning based methods.  

**Fundamental analysis:**  
Fundamental analysts are concerned with the company that underlies the stock itself. They evaluate a company's past performance as well as the credibility of its accounts. Many performance ratios are created that aid the fundamental analyst with assessing the validity of a stock, such as the P/E ratio, EPS etc. The fundamental metrics often rely on financial statements like balance sheet, income statement etc. Because fundamental analysis relies on reports that are issued based on a slower time frame, typically every quarter this type of analysis is often used to project long-term price movements.  
**Technical analysis:**  
Technical analysts or chartists are not concerned with any of the company's fundamentals. They seek to determine the future price of a stock based solely on the trends of the past price (a form of time series analysis). Numerous patterns are employed such as the head and shoulders or cup and saucer. Alongside the patterns, techniques are used such as the exponential moving average (EMA), oscillators, support and resistance levels or momentum and volume indicators. Candle stick patterns, believed to have been first developed by Japanese rice merchants, are nowadays widely used by technical analysts. Technical analysis is rather used for short-term strategies, than the long-term ones. And therefore, it is far more prevalent in commodities and forex markets where traders focus on short-term price movements.  
**Machine learning:**  
With the advent of the digital computer, stock market prediction has since moved into the technological realm. Support Vector Machines (SVM) and Artificial Neural Networks (ANN) are widely used for prediction of stock prices and its movements. Every algorithm has its way of learning patterns and then predicting. Artificial Neural Network (ANN) is a popular method which also incorporate technical analysis for making predictions in financial markets. My initial research also suggested good performance of XGBRegressor from XGBoost library, Recurrent neural networks with basic, LSTM or GRU cells and interestingly linear regression.  

## Potential Issues?  
The challenge in terms of the prediction is best described by the following long-standing hypothesis:  
**The Efficient Market Hypothesis (EMH):**  
The efficient market hypothesis (EMH), alternatively known as the efficient market theory, is a hypothesis that states that share prices reflect all information and consistent alpha generation is impossible.
According to the EMH, stocks always trade at their fair value on exchanges, making it impossible for investors to purchase undervalued stocks or sell stocks for inflated prices. Therefore, it should be impossible to outperform the overall market through expert stock selection or market timing, and the only way an investor can obtain higher returns is by purchasing riskier investments.  
**The Random Walk Hypothesis:**  
Random walk theory suggests that changes in stock prices have the same distribution and are independent of each other. Therefore, it assumes the past movement or trend of a stock price or market cannot be used to predict its future movement. In short, random walk theory proclaims that stocks take a random and unpredictable path that makes all methods of predicting stock prices futile in the long run.  
Random walk theory believes it is impossible to outperform the market without assuming additional risk. It considers technical analysis undependable because chartists only buy or sell a security after an established trend has developed. Likewise, the theory finds fundamental analysis undependable due to the often-poor quality of information collected and its ability to be misinterpreted.  
This is a remarkably interesting project and many people have pursued this as their PhD thesis.  If I do not strike a balance on the data analysis vs predictions vs the different type of features, I would like to expose, it can quickly go off schedule. Also, I need to draw boundaries on the MSE or other performance indicators. Hyperparameter tuning would be part of the project, but I would also like to try out as many models as possible.  

## Concluding Remarks
**Abstract:**  
	This project would demonstrate the following capabilities:  
* Extraction Loading and Transformation of S&P 500 data and company fundamentals
* Exploratory and Time Series Data Analysis on top of the stock data.
* Stock Screener based on fundamentals.
* Stock Price Prediction using multiple and/or an ensemble of machine learning models.

**What it is not:**  
* Should not be used as a basis for any financial decision.
* We are not trying to produce a new algorithm to beat the market.

### Disclaimer: This research should not be used to make any financial decision and it is purely academic in nature. 

## References  
Dividend. (n.d.). Retrieved from en.wikipedia.org: https://en.wikipedia.org/wiki/Dividend  
dividendyield. (n.d.). Retrieved from www.investopedia.com: https://www.investopedia.com/terms/d/dividendyield.asp  
ebitda. (n.d.). Retrieved from www.investopedia.com: https://www.investopedia.com/terms/e/ebitda.asp  
Efficient-market_hypothesis. (n.d.). Retrieved from en.wikipedia.org: https://en.wikipedia.org/wiki/Efficient-market_hypothesis  
eps. (n.d.). Retrieved from www.investopedia.com: https://www.investopedia.com/terms/e/eps.asp  
Financial_economics. (n.d.). Retrieved from en.wikipedia.org: https://en.wikipedia.org/wiki/Financial_economics  
marketcapitalization. (n.d.). Retrieved from www.investopedia.com: https://www.investopedia.com/terms/m/marketcapitalization.asp  
price-earningsratio. (n.d.). Retrieved from www.investopedia.com: https://www.investopedia.com/terms/p/price-earningsratio.asp  
responsible-ai. (n.d.). Retrieved from www.microsoft.com: https://www.microsoft.com/en-us/ai/responsible-ai  
Share_(finance). (n.d.). Retrieved from en.wikipedia.org: https://en.wikipedia.org/wiki/Share_(finance)  
Share_price. (n.d.). Retrieved from en.wikipedia.org: https://en.wikipedia.org/wiki/Share_price  
sp500. (n.d.). Retrieved from www.investopedia.com: https://www.investopedia.com/terms/s/sp500.asp  
sp-500. (n.d.). Retrieved from www.spglobal.com: https://www.spglobal.com/spdji/en/indices/equity/sp-500/#overview  
Stock. (n.d.). Retrieved from en.wikipedia.org: https://en.wikipedia.org/wiki/Stock  
Stock_market_prediction. (n.d.). Retrieved from en.wikipedia.org: https://en.wikipedia.org/wiki/Stock_market_prediction  
why-invest-in-stocks. (n.d.). Retrieved from www.fool.com: https://www.fool.com/investing/how-to-invest/stocks/why-invest-in-stocks/  

