# Microsoft 3-Statement & DCF Valuation Model

A linked three-statement financial model and discounted cash flow (DCF) valuation for **Microsoft Corporation (NASDAQ: MSFT)**, built entirely in Excel using historical FY2023–FY2025 results.

## Overview

This project reconstructs Microsoft's Balance Sheet, Income Statement, and Statement of Cash Flows from public filings and links them together with live formulas. The model then uses those statements to calculate financial ratios and perform a DCF valuation.

The project was built as a practical exercise in financial modeling, with an emphasis on linking the statements together rather than treating them as three disconnected tables.

## What's Inside

| Tab                  | Description                                                                                                                                                                                   |
| -------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Balance Sheet**    | FY2024–FY2025 balance sheet. Cash is linked directly from the Cash Flow tab rather than being re-entered.                                                                                     |
| **Income Statement** | FY2023–FY2025 income statement, from revenue through diluted EPS.                                                                                                                             |
| **Cash Flow**        | FY2023–FY2025 statement of cash flows. Net income is linked directly from the Income Statement, and beginning-of-period cash rolls forward automatically from the prior period's ending cash. |
| **Summary & Ratios** | Gross margin, operating margin, net profit margin, free cash flow, and current ratio — calculated directly from the three statements.                                                         |
| **DCF**              | Discounted cash flow valuation including NOPAT, net working capital, unlevered free cash flow, WACC, terminal value, implied equity value, and implied share price.                           |

## How the Statements Are Linked

The model is designed so that changes flow through the statements rather than relying on duplicate hardcoded figures:

* **Balance Sheet cash** ← references **Cash Flow** ending cash balance
* **Cash Flow net income** ← references **Income Statement** net income
* **Cash Flow beginning-of-period cash** ← references the prior period's ending cash
* **DCF and Summary & Ratios tabs** ← pull inputs directly from the underlying financial statements

This structure helps demonstrate the mechanics of an integrated three-statement financial model.

## DCF Methodology

* **NOPAT** = Operating income × (1 − effective tax rate)
* **Net Working Capital (NWC)** = (Accounts receivable + Inventories + Other current assets) − (Total current liabilities − Short-term debt − Current portion of long-term debt)
* **Unlevered Free Cash Flow (UFCF)** = NOPAT + Depreciation & Amortization + Capital Expenditures − Change in NWC
* **WACC** = weighted cost of equity and after-tax cost of debt based on the capital structure
* **Cost of Equity** = calculated using the CAPM framework
* **Terminal Value** = Gordon Growth (perpetuity growth) method
* **Implied Equity Value** = Enterprise Value − Total Debt + Cash & Short-Term Investments
* **Implied Share Price** = Implied Equity Value ÷ Diluted weighted average shares outstanding

## Financial Analysis

A supporting financial performance analysis is included alongside the Excel model. It evaluates Microsoft's FY2024–FY2025 performance using profitability, cash flow, and liquidity metrics.

The analysis includes:

* Gross margin
* Operating margin
* Net profit margin
* Free cash flow
* Current ratio

The analysis report highlights, among other findings, stable net profitability, improved operating margin, a modest decline in free cash flow associated with increased capital expenditure, and an improvement in the current ratio.

## Data Sources

Historical financial figures are sourced from Microsoft's Form 10-K filings for FY2023–FY2025 through **SEC EDGAR**. Figures are stated in millions of U.S. dollars, except per-share amounts.

## Notes & Limitations

* This is primarily a **historical, tied-out financial model** and does not currently include forward-looking revenue or margin projections.
* The DCF uses cash flow inputs derived from the most recent historical year rather than a multi-year operating forecast.
* The model is intended for **educational and portfolio purposes** and should not be considered investment advice.
* Valuation outputs depend on the assumptions and methodology used in the model and should not be relied upon for actual investment decisions.

## Files

* `Microsoft_3_Statement_Model_FY24_25_FINAL-3.xlsx` — the complete Excel workbook containing the three-statement model, financial ratios, and DCF valuation.
* `Microsoft Financial Performance Analysis & 3-Statement Model (FY2024–FY2025).pdf` — supporting financial performance analysis covering Microsoft's FY2024–FY2025 results.

## Project Purpose

This project demonstrates practical experience with:

**Financial Statement Modeling → Excel → Financial Analysis → DCF Valuation → Corporate Finance**

It was developed as a portfolio project to demonstrate the ability to work with real company financial statements, build linked financial models, analyze financial performance, and apply valuation methodologies.
