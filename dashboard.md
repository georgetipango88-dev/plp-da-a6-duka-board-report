# Interactive dashboard

## Looker Studio publication status

**The dashboard is not complete or public yet.** A draft report has been created, but its Google Sheets data connector still needs authorization, and public link sharing and screenshots have not been verified. Do not submit the draft URL as a live dashboard.

Google account sign-in is active. The supplied `duka_sales.csv` was uploaded to Google Drive and imported into a Google Sheet:

- [Duka Electronics H1 2026 Sales Data](https://docs.google.com/spreadsheets/d/1p3-XyRAl-BKdG1U5V95uVZ5WOrnR8HCj9986LaHuiPI/edit)
- [Draft Data Studio report](https://datastudio.google.com/reporting/8f8a6e6d-25ed-4e2a-b54f-00bbf8e24cfa/page/gl1CG/edit) (not connected or publicly shared)

**Blocked on Google OAuth:** the connector authorization returns `Error 400: invalid_scope` for `https://www.googleapis.com/auth/datastudio.firstparty`. The connector has not been authorized, so the draft report has no data. This is an OAuth-side failure, not a missing permission setting in the report. Opening the current `lookerstudio.google.com` entry point in the integrated browser redirected to `datastudio.google.com`; the existing report remains blank and disconnected. Repeated authorization attempts in this flow are unlikely to resolve the invalid scope. Google must resolve the authorization error, or the report must be created from a different Google account/environment where the connector authorization succeeds. Do not claim the draft is connected.

Once the connector is authorized and the data is connected, add:

- Scorecards: H1 sales revenue, order count, and average order value.
- Monthly time series: sales revenue by month.
- Breakdown charts: sales revenue by branch and by product/channel.
- Controls: date-range control and a drop-down control for branch or channel.
- Sharing: **Anyone with the link can view**.

After publication, replace this status with the public viewer URL and add at least two genuine report screenshots under `figures/`—one showing scorecards and monthly trend, and one showing breakdowns and both filter controls. Capture screenshots from the published report, not from a static mock-up.

## Dashboard metric definitions

- **Sales revenue:** sum of `quantity * unit_price` (KES); not profit.
- **Orders:** count of `order_id`.
- **Average order value:** sales revenue divided by order count.
- **Date range:** 1 January–29 June 2026, the dates present in the supplied CSV.
