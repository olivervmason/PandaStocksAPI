# PandaStocksAPI
A Python mini-project demonstrating the importing of data via API's, and use of Pandas and Matplotlib

*This mini project has been completed to demonstrate my understanding of basic data analytics tools and processes. As such, the 'analysis' is very much exploratory in nature and no real insights were expected to be found as a result, although some interesting patterns did emerge.*

## Part 1

A list of companies to be reviewed was imported from a csv file created based on information found on the London Stock Exchange website.

- Data from the **Yahoo Finance API** was imported using the stock tickers, via the `pandas_datareader` library

- The `datetime` feature was used to retrieve information.

Basic Python programming concepts such as loops, conditional logic (if statements), as well as manipulation of strings and lists are demonstrated

**Filter/clean large datasets**

- Data cleaning and error removal was necessary for companies where the expected stock tickers were not valid.

- The data was returned as two dataframes (one for each date), each showing ~350 stocks along with opening, closing, maximum and minimum price, along with volume.

- The initial **dataframes were sorted** to only show the adjusted closing price on each date, then **transposed** to show the company list as rows rather than column headings

- The resulting **dataframes were merged**, and the columns renamed based on the date

- New columns were created to **calculate the price increase/decrease** in absolute and percentage terms

A final filtered dataframe was created, and merged with the list from the London Stock Exchange to show the company name.

The **final result**, which took a long time to run, was then **exported to csv** format for safekeeping.


## Part 2

Daily price information for the top performing stocks filtered out in part 1 was retrieved from the API. 

This price data was then visually displayed using the `matplotlib` library and a high level analysis performed.


## Part 3 

For the final part of the project, data on international investor sentiment was retrieved from a second API called **Alpha Vantage** was used.

This required the use of an API key, which was stored in a `.gitignore` file, and manipulation of data retrieved in the JSON data format.
