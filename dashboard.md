# Interactive dashboard

## Public report

[Open the Duka Electronics H1 2026 Board Dashboard](https://datastudio.google.com/u/0/reporting/8f8a6e6d-25ed-4e2a-b54f-00bbf8e24cfa/page/gl1CG)

The report is published and shared as **Unlisted**. The share dialog confirmed that anyone on the Internet with the link can view it; it is not publicly indexed.

The report uses the [Duka Electronics H1 2026 Sales Data](https://docs.google.com/spreadsheets/d/1p3-XyRAl-BKdG1U5V95uVZ5WOrnR8HCj9986LaHuiPI/edit) Google Sheet.

### Pages and controls

- **Executive Overview** - revenue, record-count, and average-order-value scorecards; a date-range control; a branch drop-down; and the revenue time series.
- **Branch and Product Breakdown** - revenue by branch and revenue by product. The charts are sorted from highest to lowest and can be opened full-screen for easier reading.
- The overview controls filter the report by date range and branch.

### Genuine published-report screenshots

These are captures of the published report, cropped to the report or chart area:

- [Executive Overview](figures/dashboard-overview.png) - scorecards, daily trend, and controls.
- [Revenue by branch](figures/dashboard-branch-breakdown.png).
- [Revenue by product](figures/dashboard-product-breakdown.png).

## Metric definitions

- **Sales revenue:** sum of `quantity * unit_price`, in KES; this is revenue, not profit.
- **Orders:** count of `order_id` (1,000 in the supplied data). The overview's scorecard is currently labelled "Record Count."
- **Average order value:** sales revenue divided by order count (KES).
- **Date range:** 1 January to 29 June 2026, the dates present in the supplied CSV.

## Remaining dashboard gap

The published time series currently groups revenue by **day** (`order_date`), not by month. The assignment requires a monthly trend, so this dashboard item still needs to be changed to monthly granularity before the dashboard can be considered fully compliant. The report link and screenshots above reflect the current live state.
