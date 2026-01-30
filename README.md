> [!TIP]
> What's new? [Hedge Fund Risk Model](#project-9-hedge-fund) (1/29), [Private Market](#project-15-private-market-dashboard) (11/23), [Style Drift](#project-14-style-drift-detection) (6/13), [Liquidity Analysis](#project-13-liquidity-analysis) (6/12),
[Equity Dashboard](#project-12-equity-dashboard) (6/7), [ETF](#project-11-exchange-traded-funds) (6/5), [Asset Return Map](#project-10-asset-return-map) (6/4)

# Financial Toolkit in PowerBI

This is an experimental repository created for learning and educational purposes. The core theme in 2025 is to build a series of dashboard screens that provide clear, concise summaries of key information about major asset classes and instruments, all sourced from free data providers. The goal is to simulate the functionality of professional financial platforms and offer an accessible alternative, or a "poor man's Bloomberg terminal", for those who want to explore markets and analytics without costly subscriptions.

## Project 15: Private Market Dashboard

In public markets, performance is usually measured with time-weighted returns. In private markets, however, managers control the timing of capital calls and distributions, so money-weighted returns are more relevant. This [Private Market Dashboard](Private%20Markets.pbix) reports the IRR (a money-weighted measure), alongside key private market metrics such as DPI, RVPI, and TVPI, for each private asset investment made by the Washington State Investment Board between Q1 2009 and Q2 2021. A drill-through filter is also available, illustrating how all performance metrics evolve over time in response to changes in cash flows and valuations.

<img src="images/private_markets.gif" alt="Private Markets" />

## Project 14: Style Drift Detection

Style drift becomes a concern when alpha is diluted as assets under management (AUM) increase. To evaluate how a portfolio's characteristics evolve over time, a snail trail visualization can be used. In the [Style](Style.pbix) Report, two snail trail charts are included to illustrate changes in rolling active return and tracking error. One chart is static, where more recent data points are represented by larger and darker dots. The other is animated. Click the ▶️ button to view the portfolio's progression over time.

<img src="images/style.png" alt="Style Analysis" />

## Project 13: Liquidity Analysis

Although mutual funds can typically be redeemed on a daily basis, not all of their underlying stocks are equally liquid. If the liquidity of the portfolio holdings does not align with the fund’s redemption terms, the fund may struggle to meet redemption requests without incurring significant market impact costs.

In the [Liquidity](Liquidity.pbix) Report, the fund’s liquidity profile is assessed using a burndown chart, which considers the weight of each stock in the portfolio, the trading volume of those stocks, and the fund’s assets under management (AUM). The report uses the holdings of the Fidelity Small Cap America Fund as of March 31, 2025, as an example to illustrate this analysis.

<img src="images/liquidity.png" alt="Liquidity Analysis" />

## Project 12: Equity Dashboard

The [Equity Dashboard](Equity.pbix) report shows the stock return and contribution to the MSCI ACWI Index by individual stock, country, and sector over different time horizons (MTD/QTD/YTD).

<img src="images/equity.png" alt="Equity Dashboard" />

> [!NOTE]  
> Due to the limitations of the free data source, the analysis does not include stocks listed on certain exchanges, including Oslo, Tokyo, Singapore, and Shanghai (A).

## Project 11: Exchange Traded Funds

The [ETF](ETF.pbix) report features an interactive screener that allows users to find ETFs by asset class, market type, and region. It also includes a slicer that lets users toggle the breakdown by fund count or by AUM.

<img src="images/etf.png" alt="ETF Screener" />

In the Holdings worksheet, users can choose from a selection of the most popular ETFs and view their overview, top 10 holdings, and breakdown by country and sector.

<img src="images/holdings.png" alt="ETF Holdings" />

## Project 10: Asset Return Map

The [Asset Class](Asset%20Class.pbix) report presents the performance of various asset classes over time, using selected indexes or ETFs as proxies.

<img src="images/asset_class.png" alt="Asset Return Map" />

In the other worksheet, the asset class returns are displayed in a tabular format, sorted in descending order by return for each calendar year. The conditional formatting can be toggled to highlight either by asset class or by return.

<img src="images/asset_class.gif" alt="Asset Return Map" />

## Project 9: Hedge Fund Strategy Map and Risk Factor Model

The [Hedge Fund](Hedge%20Fund.pbix) report analyzes the performance of hedge fund indices across different regions, investment strategies, and time horizons. A tooltip shows the percentage of constituent funds that have reported their returns.

The second worksheet displays the flagship hedge fund indexes using a Value Added Monthly Index (VAMI) chart, shows the Compound Annual Growth Rate (CAGR) in a bar chart, and presents annual returns in a table. A tooltip shows the sensitivities to the seven hedge fund risk factors described in the [Fung and Hsieh (2004)](https://people.duke.edu/~dah7/HFRFData.htm) paper.

<img src="images/hedge_fund.gif" alt="Hedge Funds" />

## Project 8: Future Contracts

The [Futures](Futures.pbix) report presents the top five futures by trading volume within each category.

<img src="images/futures.png" alt="Futures" />

To access detailed data on individual contracts and their forward curves, right-click and select **Drill Through**.

<img src="images/contracts.png" alt="Contracts" />

## Project 7: Exchange Rates

The [Forex](Forex.pbix) report uses the Bank of Canada's average daily exchange rates to calculate cross rates and percentage changes over time. Use the tabs to navigate between currencies by region (note: CAD and USD are always shown for reference). Hover over any cell to view the direct and indirect exchange rates, as well as their respective changes during the selected period.

<img src="images/forex.png" alt="Exchange Rates" />

## Project 6: Purchasing Power Parity

The [Purchasing Power Parity](Purchasin%20Power%20Parity.pbix) report uses the Purchasing Power Parity (PPP) conversion factor from the World Bank and annual exchange rates from the Bank of Canada to calculate the extent to which a currency is overvalued or undervalued relative to its Purchasing Power Parity (PPP)-implied value against the Canadian dollar.

<img src="images/ppp.png" alt="Purchasing Power Parity" />

## Project 5: Yield Curve and Option-Adjusted Spread

The [Yield Curve](Yield%20Curve.pbix) report uses Power Query to retrieve historical par yield data from the US Treasury and presents changes in the yield curve using a line chart. An additional line chart illustrates the historical movement of yields across different maturities.

<img src="images/yield_curve.png" alt="Yield Curve" />

In the Forward Curve worksheet, Power Query retrieves the latest 1-month SOFR Average Index value, forward rates derived from SOFR futures, and the median interest rate projections published by the Federal Open Market Committee (FOMC).

<img src="images/sofr.png" alt="SOFR Forward Rate" />

In the OAS worksheet, Power Query retrieves historical Option-Adjusted Spread (OAS) data from the Federal Reserve Economic Data (FRED) database and visualizes the selected OAS trends over time.

<img src="images/oas.png" alt="Option-Adjusted Spread" />

In the Policy Rate worksheet, Power Query retrieves historical central bank policy rates from the Bank for International Settlements (BIS) database and visualizes their trends over time for the selected countries.

<img src="images/policy_rate.png" alt="Central Bank Policy Rate" />

## Project 4: Stock Monitor

The [Stock Monitor](Stock%20Monitor.pbix) report uses Power Query to retrieve historical stock prices from Yahoo! Finance and displays them in a line chart. A slicer is included to normalize the starting stock price to $100, enabling a more meaningful comparison across different stocks.

<img src="images/stocks.png" alt="Stock Monitor" />

## Project 3: Equity Market Index

The [Real Time Index](Real%20Time%20Index.pbix) report uses Power Query to retrieve real-time performance data from the [MSCI website](https://www.msci.com/real-time-index-data-search) and displays it in a bar chart. The data is delayed by 20 minutes. The base currency is predetermined and not user-configurable.

<img src="images/index_rt.png" alt="Real Time Market Index" />

## Project 2: Option Strategies

The [Option Strategies](Option%20Strategies.pbix) report presents the values of individual securities and the total payoffs of various option strategies. Theoretical option values are calculated using the Black-Scholes model.

<img src="images/options.png" alt="Option Strategies" />

## Project 1: Mutual Funds / Time Series Analysis

The [Time Series Analysis](Time%20Series%20Analysis.pbix) report contains two pages. The **Metrics** page displays key performance and risk metrics, with interactive slicers to select the fund, benchmark, risk-free rate, time horizon, market condition (up, down, or all), and confidence interval.

<img src="images/ftk_metrics.png" alt="Metrics" />

The **Charts** page visualizes the time series of a selected performance or risk metric, which can be displayed on a cumulative, rolling, trailing, or calendar-year basis.

<img src="images/ftk_charts.png" alt="Charts" />