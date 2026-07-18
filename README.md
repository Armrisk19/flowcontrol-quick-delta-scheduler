# FLOWCONTROL Exact Scoring Scheduler v1.6.1

Every five minutes this public workflow refreshes Quick Delta, refreshes the full opportunity queue when due, refreshes direct official sources when aging, runs the quota-aware macro refresh, and verifies Gateway v9.1.0 / Strategy v25.0.3.

Repository secrets:

- `FLOWCONTROL_GATEWAY_URL`
- `FLOWCONTROL_GATEWAY_TOKEN`

The token must match `OMNI_COGNITIVE_GATEWAY_TOKEN`.

Run the workflow manually after deployment and enable the real OpenAI acceptance input once. A successful run prints `FLOWCONTROL scheduler verification PASS`.
