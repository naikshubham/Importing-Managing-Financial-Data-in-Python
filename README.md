# Importing-Managing-Financial-Data-in-Python
## Data Science Skills for financial data
## Pulling stock price data from various APIs
## calculate returns for various time horizons, analyze stock performance by sector for IPOs, and calculate and summarize correlations


### Reading, inspecting & cleaning data from csv files
- Pandas dataframe columns has its different data types and is stored in dtype
- dtype affects calculation and visualization
- **object** - Text or a mix of text and numeric data
- **int64** - Numeric:Whole numbers
- **float64** - Numeric: Decimals or whole numbers with missing values
- **datetime64** - Date and time information

### Deal with missing values

```python
amex = pd.read_csv('amex-listing.csv', na_values='n/a')
```

- **na_values** converts a given string to **np.nan**, defaults to **None**
- Pass a string 'n/a' values and pandas will replace them value **`np.nan`** (Not a number)

### Properly parse dates

```python
amex = pd.read_csv('amex-listing.csv', na_values='n/a', parse_dates=['Last Update'])
```

### Import data from excel

```python
pd.read_excel(file, sheetname = 0)
```

- Select firstsheet by default with sheetname = 0 or select by name with `sheetname = 'amex`
- Import several sheets with the list such as sheetname = ['amex', 'nasadaq']

### Combine data from multiple worksheets
- Concatenate or "stack" a list of pd.DataFrames
- Syntax : pd.concat([amex, nasdaq, nyse])

### DataReader : Access financial data online

- **`pandas_datareader**`** : provides easy access to various financial internet data sources
- Available sources include : Yahoo! and Google Finance, Federal Reserve, World Bank, OECD, Eurostat, OANDA

### Import Stock prices for Google using Google Finance
- Import the DataReader class from data module
- **`Stock ticker`** is the unique symbol needed to get stock information for a certain company.

### Economic data from Federal Reserve

### Select stock based on criteria
- Use the listing information to select specific stocks
- Criteria : Stock exchange, Sector or Industry, IPO year, Market Capitalization

### Retrive multiple stocks & manage a dataframe with multiple indices
- We will be using listing information to select multiple stocks. eg.largest 3 stocks per sector
- Then use Google Finance to retrieve data for several stocks

#### Multiindex
- Multiindex dataframe has two axis(rows & cols), the index can have multiple levels

### Summarize categorical variables
- So far, we have analyzed quantitative variables
- Categorical variables differ because their values represent different categories
- For numeric values we can apply different transformations(average)
- Columns of dtype "object" are not numerical in nature, they are categorical


## Aggregate data by category
- Split data into groups, then summarize groups
- Examples : Largest company by exchange, Median market capitalization per IPO year, average market capitalization per sector




















