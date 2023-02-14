# Time Series Project: Predicting House Prices
In this project, I work with a dataset from Zillow that has house prices over the course of several 
month-years, starting in 1996. The dataset also provides other information such as: zip code, region, 
county name and city - to name a few. I analyze these series using a time series approach and provide 
recommendations for an hypothetical real estate firm.

The modeling framework is streamlined as follows: time series analysis, basic and rolling statistics, 
seasonal decomposition, unit-root test, SARIMAX modeling and prediction. Lastly, we delve deeper into the 
data, repeating this process with microscopic lenses.

## Business Problem
An hypothetical is looking to diversify its portfolio. Thinking of risk-weighted returns, then the firm 
seeks advisory for spotting the best areas over the course of 12-24 months. The stakeholders of this 
problem, besides the investment firm, are: general public and outside investors, 
municipalities and counties and communities in general.

## Data and Analysis
The dataset used is a time series from Zillow, that has house prices over the course of Apr/96 through 
Apr/18. Besides prices, there are the other categorical variables: RegionID, RegionName, City, State, 
Metro, CountyName and SizeRank.

Splitting and ranking the dataset into the top 10 counties with respect to median prices, we end up with 
the following locations:

<img src='https://github.com/ovilar/phase_4-project/blob/main/img/img00.png' alt='Top Counties - Median 
Price, 1996-2018'>

I rank which counties are the most valuable with respect to their median and mean and assessing how they fare with respect to risk (i.e. standard
deviation). I also provide the evolution of house prices with respect to price, their 12-month window rolling statistics (mean/std. 
deviation) and the log returns. From this initial filtering, we end up with 3 counties as the best risk-weighted returns: Suffolk, NY; Palm 
Beach, FL and Miami-Dade, FL.

## Time Series Workflow 
I start with testing stationarity and performing a seasonal decomposition to assess the best combination of Autoregression Integrated Moving 
Average factors (i.e. p, d, q) and Seasonal Factors (p, d, q, s). Given computational constraints, I limit those to 1 round of runs (even though 
I also provide examples with 2 runs). Then, Autocorrelation and Partial Autocorrelation plots are provided to check the consistency of the 
seasonal decomposition findings. Lastly, I perform Root-Mean Square tests on both training and testing data - which both provide satisfying 
results for our three locations.

## Conclusion
Using a time series approach I provide a SARIMAX model that is able to perform well both with training and testing data. Root-mean squared errors 
are less than 3% of the historical mean prices. Thus, one can infer the model is good to predict with a certain accuracy house prices. The model is 
inversely as good as the time horizon increases, so for shorter-term forecast (up to 24-months) we have more precise price estimates.
<img src='' alt='Forecast of Mean Prices - 60-month window'>

### Takeaways and Recommendations
The best historical risk-weighted return is located in Suffolk, NY, followed by Palm Beach, FL and 
Miami-Dade, FL. So the investor can pursue two distinct strategies:

<ul>
<li>Divide and Conquer - investing in the  best bang for the buck county/location all at once;</li>
<li>Rays of the Sun - choosing one specific location and irradiating the strategy within that county;</li>
<li>Alternative - investing in more established counties.</li>
</ul>

### Further Research
I list below some ideas about further research:
<ul>
<li>Implementing Portfolio Theory as a way of assessing optimizing investment strategies;</li>
<li>Adding exogenous features that might explain house prices (such as socio-economic data, school 
district data, etc.);</li>
<li>Delving deeper to explain the variation within counties to assess under/overpriced real state.</li>
</ul>

## Instructions
This repository provides basic guidelines on how to navigate through this notebook and its material. For 
the sake of space, I do not make the dataset available.

Here you will find:
<ul>
<li><a href='https://github.com/ovilar/phase_4-project/blob/main/presentation.pdf'>Presentation 
file</a>;</li>
<li>Jupyter Notebook;</li>
<li>README.md file;</li>
<li>Image Folder.</li>
</ul>
Feel free to reach out if you have any critique, suggestion or correction.
