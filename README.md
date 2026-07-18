# FLOWCONTROL Exact Scoring Scheduler v1.6.3

This release hardens Gateway communication against temporary Vercel or upstream HTTP 502 responses.

Each required Gateway request now:

- names the endpoint in the Actions log;
- attempts the request up to four times;
- waits progressively between attempts;
- prints the HTTP status and response body on retry;
- fails only after all attempts are exhausted.

The macro refresh request is advisory. A temporary refresh failure is deferred while the scheduler validates the cached macro status. Required health, release, readiness, probe, Quick Delta, opportunity queue, official-source, and macro-status checks remain strict.

Expected release contract:

- Gateway `9.1.0`
- Strategy `25.0.3`
- feed mode `PUBLIC_NUMERIC_MARKET_DATA_ONLY`
- 20 markets
- 16 tool declarations
- 24 feed identifiers
