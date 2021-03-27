# Stock Market Project Overview:
* Obtained the historical stock data from yahoo finance using an open source python API, yfinance 
* Exploratory data analysis (EDA) including descriptive statistics to make sense and study the behavior of the data for the big 6 companies: Amazon, Facebook, Microsoft, Google, Apple and Tesla.
* Discuss different trends that are pronounced when analysing stocks of these companies. 
* Then also look at how the stock prices vary for 51 different companies (which include both the big 6 and smaller companies for contrast), and then leverage traditional probabilistic machine learning methods to forecast stock prices for a company.
* Also look at clustering these companies based on their trading patterns and then forecasting the adjusted closing prices 
* The entire EDA and descriptive analysis for the big 6 companies has been done in R, within R Markdown, and the probabilistic analysis has been done in Python and Jupyter Notebook

## Code and Packages Used 
* *R Version :* 4.0.5 
* *Packages:* tidyverse, plotly, tidyquant, zoo, TTR
* *Python Version :* 3.7
* *Packages:* yfinance, numpy, pandas, plotly, sklearn, KMeans, SpectralClustering, AgglomerativeClustering,GaussianMixture, BayesianGaussianMixture, PCA , Prophet

## EDA 
Below are few highlights of the EDA done on the data sets 

![Capture](https://user-images.githubusercontent.com/56661161/112730513-373cee00-8eef-11eb-93b7-2ee2c3ba6978.JPG)

![teslas](https://user-images.githubusercontent.com/56661161/112730539-5c316100-8eef-11eb-95a4-56a222c00b54.JPG)

* We see that Tesla’s average daily return of 0.997% is atleast 4 times of any other stock (the others are around the same). This may have a lot to do with the high positive returns that Tesla has compared to the others. Tesla is also a very volatile stock, which increases the possibility of making quick positive returns, as will see in the next graph

![vols](https://user-images.githubusercontent.com/56661161/112730576-98fd5800-8eef-11eb-9fab-4b5bb19f01c5.JPG)
* We again see that Tesla is almost twice as volatile as the other stocks (almost the same). There are multiple reasons for it: ranging from product releases, to fluctuations based off Elon Musk’s tweets, which have been known to manipulate Tesla’s stock several times and let to him being charged by the SEC for securities fraud once. This volatility can also be due to many traders short-selling Tesla stock last year as previously mentioned (which could explain the large dips).

## Clustering Companies based on Trading Patterns 
* Here we try to cluster the companies based on their trading pattern, we use the daily return along with the daily volume for the feature vector. 
* The daily return is measured as Return = Closing price - Opening price
* Created a feature vector by combining both daily returns and daily volumes 
* Since the vectors are in higher dimension i.e (total number of days we are analyzing), we perform dimensionality reduction to project into 2D space for visualization. For this purpose, we used PCA.
 ![fffffffffffff](https://user-images.githubusercontent.com/56661161/112730700-36588c00-8ef0-11eb-835f-3f3599d3dcc0.JPG)

* Gaussian Mixture Model Resulting Clusters :
![gmm](https://user-images.githubusercontent.com/56661161/112730728-630ca380-8ef0-11eb-852f-ac6ae4474dd7.JPG)


* K means model resulting clusters 
![kmeans](https://user-images.githubusercontent.com/56661161/112730748-7ddf1800-8ef0-11eb-9211-f2a1018329cf.JPG)


