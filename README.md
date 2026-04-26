# ACC102-assignments
This will be used for the acc102 assignments
# Tesla Stock Price Analysis (2020-2023)

## 1. Problem & User
**Problem**: People who interets in investing and analysing need to quickly understand Tesla's (TSLA) stock price trends from 2020 to 2023 to evaluate its market performance.

**Target Users**: Retail investors, quantitative analysis beginners, finance students.

## 2. Data
- **Source**: CRSP (via Wharton Research Data Services, WRDS)
- **Access Date**: 2026-04-26
- **Key Fields**:
  - `htsymbol`: Ticker symbol (TSLA)
  - `date`: Trading date
  - `prc`: Closing price (in cents — divide by 100 for dollars)
  - `ret`: Daily return
  - `permno`: CRSP permanent company identifier

## 3. Methods
1. Connect to WRDS database using the `wrds` Python library
2. Query data from `crsp.msf` (monthly stock file) and `crsp.msfhdr` (header info) using SQL
3. Load results into a Pandas DataFrame
4. Sort data by date
5. Plot closing price over time using Matplotlib

## 4. Key Findings
- TSLA stock showed significant upward trend from 2020 to 2023
- Price increased from ~$30 in early 2020 to over $200 by end of 2023 (after converting from cents)
- Multiple noticeable fluctuations reflect market reactions to company performance and macro conditions
- Rapid growth phase observed around 2021

## 5. How to run
```bash
# Install dependencies
pip install pandas matplotlib wrds

# Run the script (assuming filename: tesla_analysis.py)
python tesla_analysis.py


## 6. Product / Demo

**Code & Analysis**: See `tesla_analysis.ipynb` for the full implementation.

**Key Visualization** – TSLA Closing Price (2020–2023):

![TSLA Price Chart](figures/tsla_price.png)

## 7. Limitations & next steps

**Limitations**:
- Data only through 2023, not covering 2024–2025
- No comparison with other EV peers

**Next Steps**:
- Add moving averages and volume analysis
- Compare with S&P 500 index
