Yield Curve Construction – US Treasury (FRED Data)

A Treasury & Fixed-Income Analytics Project in Python

Project Overview

This project constructs a continuous US Treasury yield curve using real market data sourced from the Federal Reserve Economic Data (FRED) API.
It retrieves on-the-run yields for multiple maturities (1M to 10Y), cleans the data, and uses monotone piecewise cubic Hermite interpolation (PCHIP) to generate a smooth, arbitrage-free term structure.

The final output is a continuous yield curve, plotted alongside observed market yields.

Business Relevance (Treasury / ALM / Risk)

Yield curve construction is a core task in:

⦁	Treasury Mid-Office

Mark-to-Market valuation

Sensitivity & duration analysis

Risk monitoring

⦁	ALM / IRRBB

NII/EVE simulations

Shock scenario modelling

Repricing gap study

⦁	Market Risk

PV01 / DV01 computation

Curve risk measurement

Stress testing

⦁	Investment & Fixed Income Strategy

Bond pricing

Forward curve analysis

Portfolio analytics


This project forms the foundation for bond valuation, PV01, duration, VaR, IRRBB, and liquidity risk engines.

Key Features of This Notebook

1. Automatic Data Retrieval from FRED

Uses FRED API to pull the latest yields:

1-month

3-month

6-month

1-year

2-year

3-year

5-year

7-year

10-year

2. Tenor Mapping

Tenors expressed in years (fractions for short maturities).

3. Yield Cleaning & Structuring

Fetches time-series

Removes missing values

Extracts the latest available yields

4. Monotone Continuous Interpolation (PCHIP)

PCHIP avoids oscillations

Ensures no negative yields

Produces smooth, realistic curves

5. High-Resolution Yield Curve Plot

200 interpolated tenors

Clear visualisation of observed vs continuous curve

⦁	Methods & Tools Used

Python Libraries

numpy – numerical operations

matplotlib – plotting

fredapi – market data retrieval

scipy.interpolate – PCHIP interpolation

⦁	Interpolation Method

PCHIP (Piecewise Cubic Hermite Interpolating Polynomial)

Shape-preserving

No artificial oscillations

Ideal for yield curves

⦁	Output

Continuous yield curve plot

Blue line: interpolated continuous curve

Red points: observed market yields

⦁	Numerical arrays

Tenors

Observed yields

Interpolated yields

⦁	These can be directly used for:

Bond valuation

Discount factor generation

Forward rate construction

Sensitivity analytics

Risk factor creation

⦁	File Structure

01_yield_curve/
│
├── yield_curve.ipynb          ← main notebook
├── data/                      ← FRED data used through its API(Anyone can generate their fred API from FRED website)
├── README.md                  ← this file
└── images/                    ← curve plots


Author

Santosh Kumar
FRM | CQF | EPAT | MScFE (WQU) | CFA L2 candiadte & CMT Candidate | MCSI
Focused on Treasury, Market Risk, Credit Risk, ICAAP, ALM, ILAAP, Quantitative Finance & Python-based analytics.
