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