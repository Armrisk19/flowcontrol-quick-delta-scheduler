# FLOWCONTROL Five-Minute Quick Delta Scheduler v1.2.0

Small public scheduler repository for Gateway v8.4.0. It refreshes public five-minute market-ranking context only. It contains no account, order, position, wallet, subscriber, or private strategy data.

The workflow:

1. refreshes `/api/quick-delta-refresh` every five minutes;
2. retries transient HTTP failures;
3. requires a successful JSON response with all 20 markets;
4. verifies release sync, Quick freshness, and complete Quick universe through `/api/readiness`.

Add GitHub Actions secrets:

- `FLOWCONTROL_GATEWAY_URL`
- `FLOWCONTROL_GATEWAY_TOKEN`

Run the workflow once manually after Gateway v8.4.0 is deployed.
