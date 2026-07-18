# FLOWCONTROL Exact Scoring Scheduler v1.6.2

Every five minutes this public workflow refreshes Quick Delta, refreshes the full opportunity queue when due, refreshes direct official sources when aging, runs the quota-aware macro refresh, and verifies Gateway v9.1.0 / Strategy v25.0.3.

This release aligns scheduler verification with the Gateway health contract:

```text
feed_auth_mode: PUBLIC_NUMERIC_MARKET_DATA_ONLY
```

Repository secrets:

- `FLOWCONTROL_GATEWAY_URL`
- `FLOWCONTROL_GATEWAY_TOKEN`

The token matches `OMNI_COGNITIVE_GATEWAY_TOKEN`.

Run the workflow manually after deployment and enable the real OpenAI acceptance input once. A successful run prints `FLOWCONTROL scheduler verification PASS`.
