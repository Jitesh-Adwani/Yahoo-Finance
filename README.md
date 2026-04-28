# Yahoo-Finance
# EUR/INR Currency Analysis using Technical Indicators

This project focuses on scraping historical EUR/INR exchange rate data from Yahoo Finance and performing technical analysis to generate trading signals based on widely used indicators.

# 🚀 Project Overview

The goal of this project is to:

1. Scrape historical EUR/INR currency data
2. Perform technical analysis using key indicators
3. Generate BUY / SELL / NEUTRAL decisions for:
     - 1-day timeframe
     - 1-week timeframe
# 📅 Data Source
  - Source: Yahoo Finance
  - Currency Pair: EUR/INR
  - Time Period:
  - Start: January 1, 2023
  - End: September 30, 2024
# 🛠️ Tech Stack
    Python
    Pandas
    NumPy
    Matplotlib / Seaborn (for visualization)
    yfinance / BeautifulSoup (for scraping)
# 📈 Technical Indicators Used
**1. Moving Average (MA)**

  A Moving Average smooths price data to identify trends over a specific period.

Simple Moving Average (SMA):

<img width="575" height="279" alt="image" src="https://github.com/user-attachments/assets/a51a8f79-3322-4208-b0d8-049a18ebcd22" />

	​

	​

Helps identify:
  - Trend direction
  - Support & resistance levels

**2. Bollinger Bands**

Bollinger Bands measure volatility and potential overbought/oversold conditions.

**Components:**
  
  Middle Band = Moving Average
  - Upper Band = MA + (2 × Standard Deviation)
  - Lower Band = MA − (2 × Standard Deviation)
    
 **Interpretation:**
  - Price near upper band → Overbought
  - Price near lower band → Oversold
    
**3. Commodity Channel Index (CCI)**
CCI measures deviation of price from its statistical mean.

Formula:
<img width="355" height="273" alt="image" src="https://github.com/user-attachments/assets/fef10991-e57b-4996-8216-ce483b741d94" />


**Interpretation:**
  - CCI > +100 → Overbought
  - CCI < -100 → Oversold
  - 
# 🔍 Analysis Methodology
**Data Collection**
  Fetch historical EUR/INR prices from Yahoo Finance
  Data Preprocessing
  Clean missing values
  Convert date formats
  Extract OHLC (Open, High, Low, Close)
  Indicator Calculation
  
**Compute:**
  Moving Average (daily & weekly)
  Bollinger Bands
  CCI
  
**Timeframe Analysis**
  - 1-Day Analysis: Based on latest daily indicators
  - 1-Week Analysis: Aggregated weekly trends
# 📊 Trading Signal Logic

Signals are derived by combining all indicators:

**Indicator	Condition	Signal**
- Moving Average	Price > MA	Bullish
- Bollinger Bands	Near lower band	Buy
- Bollinger Bands	Near upper band	Sell
- CCI	> +100	Sell
- CCI	< -100	Buy
🧠 Decision Strategy
📅 As of September 30, 2024:
# **🔹 1-Day Signal**
Combine short-term MA trend, Bollinger position, and CCI value
**Output:**
- ✅ BUY → Bullish momentum + oversold signals
- ❌ SELL → Overbought + bearish reversal
- ⚖️ NEUTRAL → Mixed signals
# **🔹 1-Week Signal**
   - Focus on broader trend stability
   - Reduce noise from daily fluctuations
# ⚠️ Disclaimer

This project is for educational purposes only.
It does not constitute financial advice. Always perform your own research before making trading decisions.
