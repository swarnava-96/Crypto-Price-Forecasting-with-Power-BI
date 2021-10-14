# Crypto-Price-Forecasting-with-Power-BI

### Goal: To create an interactive dashboard using MS Power BI Desktop as a POC to forecast crypto prices. 

### About the data set: 
The data set is downloaded from Kaggle[[link](https://www.kaggle.com/sudalairajkumar/cryptocurrencypricehistory)]. 
The dataset has one csv file for each currency. Price history is available on a daily basis from April 28, 2013. 
This dataset has the historical price information of some of the top crypto currencies by market capitalization.

1. Date : date of observation
2. Open : Opening price on the given day
3. High : Highest price on the given day
4. Low : Lowest price on the given day
5. Close : Closing price on the given day
6. Volume : Volume of transactions on the given day
7. Market Cap : Market capitalization in USD

Some of the questions which could be inferred from this dataset are:

1. How did the historical prices / market capitalizations of various currencies change over time?
2. Predicting the future price of the currencies
3. Which currencies are more volatile and which ones are more stable?
4. How does the price fluctuations of currencies correlate with each other?
5. Seasonal trend in the price fluctuations

### Project Description:
1. I have used the seven most popular crypto currencies data from the above set. The crypto currencies that I have used in this
project are: BinanceCoin, Bitcoin, Dogecoin, Ethereum, NEM, Stellar and XRP. The folder "Datafile" contains all the datasets
including the combined csv file.
2.  The first step was to combine all the seven csv files into one combined csv file as per the requirement of Power BI.
Since, I use Excel 2007, so I don't have the Power Query tab inside my Data ribbon. So, I have used Pandas to combine all the csv's
from my folder. File, "Data Preprocessing.ipynb" contains the Python codes. I have also performed some basic Exploratory Data 
Analysis using Python in order to understand the data well.
3. The second step is to load the combined dataset into Power BI Desktop.
4. After loading the data into Power BI Desktop, the first step is to change the values of the features "High", "Low", "Open",
"Close" and "Marketcap" into currency.
5. Slicer was made showing the names of the seven crypto currencies.
6. A custom column(Year) was added for extracting the year from the date column using the formula:

```Date.Year([Date])```

8.  Line chart was plotted showing Market Capital with time. From this chart we can clearly see the rise in Bitcoin during the period
2020-21. 
9. Forecasting of Market Capital for crypto currency was done for the next 365 days.
10. Cards were made showing features like High, Low, Average, Volume and Market Capitalization.
11. Average was calculated by creating a custom column and using the formula:

```([High]+[Low])/2```

12. In the second page of the report two line charts were plotted showing High vs Low by date and Open vs Close by date.


### Demo:
![image](https://user-images.githubusercontent.com/75041273/137232253-91fe92b7-def5-4421-b925-7df652ff1a26.png)
![image](https://user-images.githubusercontent.com/75041273/137232359-3da8904c-0b4a-4c43-b90b-52d96e25ddf0.png)

### Installation:

The following steps will guide you to install Power BI Desktop and run the project at your local machine:

1. Download and install Power Bi Desktop from [here](https://www.microsoft.com/en-in/p/power-bi-desktop/9ntxr16hnw1t#activetab=pivot:overviewtab).
2. Clone this github repository or download as zip.
3. Once Everything is done, open the .pbix file. 

If you already have Power BI Desktop, then you can skip the first step.
