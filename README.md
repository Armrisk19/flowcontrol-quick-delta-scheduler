# FLOWCONTROL Autonomous Desk Scheduler v2.0.1

Runs every five minutes and verifies the synchronized production release:

- Gateway 10.0.1
- Strategy 26.0.1
- 20-market universe
- 16 tool declarations
- 24 feed identifiers
- position capacity Quick 7 / Medium 9 / Longer-Term 4 / Global 20
- feed mode PUBLIC_NUMERIC_MARKET_DATA_ONLY

The workflow refreshes Quick Delta, the opportunity queue, official sources, and macro status with four-attempt request handling. It verifies health, release manifest, readiness, probe matrix, source status, and optional OpenAI live acceptance.

Upload:

- `.github/workflows/flowcontrol-autonomous-desk-v2.0.1.yml`
- `EXPECTED_RELEASE.json`
- `README.md`
