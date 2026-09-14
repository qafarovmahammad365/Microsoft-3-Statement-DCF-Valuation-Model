# Microsoft 3-Statement & DCF Valuation Model

A fully linked three-statement financial model and discounted cash flow (DCF) valuation for **Microsoft Corporation (NASDAQ: MSFT)**, built entirely in Excel, based on historical FY2023–FY2025 results.

## Overview

This project reconstructs Microsoft's Balance Sheet, Income Statement, and Statement of Cash Flows from public filings and links them together with live formulas, then uses that output to drive a DCF valuation and a set of summary financial ratios. It's built as a practical exercise in financial modeling: tying real statements together the way a working model should, rather than three disconnected tables that happen to agree.

## What's Inside

| Tab | Description |
|---|---|
| **Balance Sheet** | FY2024–FY2025 balance sheet. Cash is linked live from the Cash Flow tab rather than re-entered. |
| **Income Statement** | FY2023–FY2025 income statement, from revenue down to diluted EPS. |
| **Cash Flow** | FY2023–FY2025 statement of cash flows. Net income is pulled live from the Income Statement, and beginning-of-period cash rolls forward automatically from the prior period's ending cash. |
| **Summary & Ratios** | Gross margin, operating margin, net profit margin, free cash flow, and current ratio — all calculated directly off the three statements. |
| **DCF** | A discounted cash flow valuation: NOPAT, net working capital, unlevered free cash flow, WACC, terminal value, implied equity value, and implied share price. |

## How the Statements Are Linked

Rather than three tabs of static numbers that happen to match, the model is wired so a change flows through:

- **Balance Sheet cash** ← references **Cash Flow** ending cash balance
- **Cash Flow net income** ← references **Income Statement** net income
- **Cash Flow beginning-of-period cash** ← references the prior period's ending cash within the same statement
- **DCF and ratio tabs** ← pull every input directly from the Balance Sheet, Income Statement, and Cash Flow tabs — no hardcoded duplicates

## DCF Methodology

- **NOPAT** = Operating income × (1 − effective tax rate)
- **Net Working Capital (NWC)** = (Accounts receivable + Inventories + Other current assets) − (Total current liabilities − Short-term debt − Current portion of long-term debt)
- **Unlevered Free Cash Flow (UFCF)** = NOPAT + Depreciation & Amortization + Capital Expenditures − Change in NWC
- **WACC** — weighted by an equity/debt capital structure, using a CAPM-based cost of equity and an after-tax cost of debt
- **Terminal Value** — Gordon Growth (perpetuity growth) method applied to the final projected UFCF
- **Implied Equity Value** = Terminal Value − Total Debt + Cash & short-term investments
- **Implied Share Price** = Implied Equity Value ÷ Diluted weighted average shares outstanding

## Data Sources

All historical figures are sourced from Microsoft's Form 10-K filings (FY2023–FY2025), available via [SEC EDGAR](https://www.sec.gov/edgar/search/). Figures are stated in millions of U.S. dollars, except per-share amounts.

## Notes & Limitations

- This is a **historical, tied-out model** — it does not (yet) include forward-looking revenue/margin projections. The DCF derives its cash flow inputs from the most recent historical year rather than a multi-year forecast.
- Built for educational and portfolio purposes. **Not investment advice** — figures, assumptions, and valuation outputs should not be relied on for actual investment decisions.

## File

- `Microsoft_3_Statement_Model_FY24_25_FINAL.xlsx` — the complete workbook (5 tabs, fully linked, zero formula errors)

## License

No license specified — all rights reserved by the author unless otherwise noted.
