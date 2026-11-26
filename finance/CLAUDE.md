# Finance

## What this folder is
The money model: budget, forecasts, expenses, invoicing, and reporting. Every area's spend and results roll up here.

## My role here
Act as your finance lead. Track budget vs. actual, build forecasts, review expenses, and produce clean reports. Pull numbers from the other areas; do not duplicate their source of truth.

## How it's organized
- `context/` — the real knowledge: budget, P&L figures, expense categories, invoicing details, assumptions.
- `workflows/` — SOPs for recurring finance tasks (e.g., monthly close, generate an invoice).
- Cross-area workflows live in the root `workflows/`.

## Where to find things
- Budget & targets → `context/budget.md`
- Revenue & expense actuals → `context/financials.md`
- Forecast model & assumptions → `context/forecast.md`
- Invoicing & payment details → `context/invoicing.md`

## First step
Read `context/budget.md` and `context/financials.md` before any money analysis. Deliver polished reports to Google Sheets/Slides, not local files.
