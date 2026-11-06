# Interactive dashboard

## Looker Studio publication status

**The dashboard is not complete or public yet.** A draft report has been created, but its Google Sheets data connector still needs authorization, and public link sharing and screenshots have not been verified. Do not submit the draft URL as a live dashboard.

Google account sign-in is active. The supplied `duka_sales.csv` was uploaded to Google Drive and imported into a Google Sheet:

- [Duka Electronics H1 2026 Sales Data](https://docs.google.com/spreadsheets/d/1p3-XyRAl-BKdG1U5V95uVZ5WOrnR8HCj9986LaHuiPI/edit)
- [Draft Data Studio report](https://datastudio.google.com/reporting/8f8a6e6d-25ed-4e2a-b54f-00bbf8e24cfa/page/gl1CG/edit) (not connected or publicly shared)

**Blocked on Google OAuth:** the connector authorization returns `Error 400: invalid_scope` for `https://www.googleapis.com/auth/datastudio.firstparty`. The Google error-details dialog confirms this scope is being requested by Data Studio's own OAuth flow (`GeneralOAuthLite`); it is not a scope configured by this assignment or a permission that can be enabled in the report. The connector has not been authorized, so the draft report has no data. Opening the current `lookerstudio.google.com` entry point redirected to `datastudio.google.com`; the existing report remains blank and disconnected. Repeated authorization attempts are unlikely to resolve an invalid scope. Google must resolve the authorization request, or the report must be created from a different Google account/environment where the connector authorization succeeds. Do not claim the draft is connected.

**Next step:** report this to Data Studio support using the connector's **Report an issue** link or the Data Studio feedback/help menu. Include the timestamp, exact scope, `Error 400: invalid_scope`, and the OAuth error-details text. The client ID in that dialog identifies the Data Studio application; do not share passwords, cookies, or OAuth tokens. If testing a different Google account is convenient, use it only as a diagnostic; it will not fix a malformed application scope.

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
