
# AR Aging Dashboard (Power BI)

This project delivers a modern Accounts Receivable (AR) Aging Dashboard in Power BI, designed for finance teams to analyze customer balances, overdue invoices, and aging risk dynamically across any selected snapshot date.

## Data Model

- `Invoices`: Base invoice data (amount, issue date, due date)
- `AR Detail`: Daily exploded balance entries per invoice
- `Daily AR Detail`: Aggregated snapshot for grouped visuals
- `Customer`: Customer metadata
- `Aging Buckets`: Bucket classification table (0-30, 31-60, etc.)
- `Date`: Calendar table with month/day hierarchy

## Report Pages

1. **AR Aging Overview** – KPI cards, aging bar chart
2. **Invoice Breakdown** – Invoice-level detail by bucket
3. **Customer Aging Summary** – Matrix of customers x aging buckets
4. **Invoice Register** – All open invoices with status and days overdue
5. **Customer Statement Snapshot** – One row per customer, full aging spread

## Key Features

- Snapshot filtering via `Date[Month/Day]` hierarchy (single select)
- All AR metrics calculated "as of" selected snapshot date
- Overdue AR dynamically bucketed and color-coded
- Top 10 charts, matrix summaries, and invoice drill-down

## Usage Notes

- Requires valid relationships between `CustomerKey`, `Date`, and `Aging Bucket`
- Visual filters are applied to hide zero-balance customers
- All measures work dynamically based on slicer context

## Author Notes

Built in collaboration with an advanced Power BI user. Improves on static accounting system outputs with full interactivity and flexibility.
