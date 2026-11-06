# Interactive dashboard

## Looker Studio publication status

**The public Looker Studio report has not yet been published.** Google sign-in and report-sharing permissions are required to create and publish it; this workspace currently has no authenticated Google account. No report URL or Looker Studio screenshots are claimed here. Do not submit a placeholder URL as a live dashboard.

When signed in, create the dashboard from the included `duka_sales.csv` using the Looker Studio file upload connector (or import the CSV to Google Sheets first). Use `order_date` as the date dimension, `revenue = quantity * unit_price` as the sales-revenue metric, and `order_id` as the order count. Add the following:

- Scorecards: H1 sales revenue, order count, and average order value.
- Monthly time series: sales revenue by month.
- Breakdown charts: sales revenue by branch and by product/channel.
- Controls: date-range control and a drop-down control for branch or channel.
- Share settings: **Anyone with the link can view**.

After publication, replace the status above with the public Looker Studio URL and add at least two genuine report screenshots under `figures/`—one showing scorecards and monthly trend, and one showing breakdowns and both filter controls. Capture screenshots from the published report, not from a static mock-up.

## Dashboard metric definitions

- **Sales revenue:** sum of `quantity * unit_price` (KES); not profit.
- **Orders:** count of `order_id`.
- **Average order value:** sales revenue divided by order count.
- **Date range:** 1 January–29 June 2026, the dates present in the supplied CSV.
