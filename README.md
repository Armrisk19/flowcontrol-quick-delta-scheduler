# FLOWCONTROL Opportunity Capture Scheduler v2.5.0

This public GitHub Actions scheduler refreshes market-only Gateway intelligence every five minutes and verifies the synchronized release contract.

Required repository secrets:
- `OMNI_COGNITIVE_GATEWAY_TOKEN`
- `FLOWCONTROL_GATEWAY_BASE_URL` (optional when using the default FLOWCONTROL Gateway URL)

The five-minute cycle refreshes Quick Delta, the opportunity queue, and the 60-cell Directional Opportunity Mesh. Official and macro source refreshes run hourly to control external usage and latency. The scheduler verifies multi-timeframe coverage, breadth classification, one-direction selection, lifecycle self-tests, release synchronization, and an optional non-blocking live OpenAI acceptance diagnostic. Scheduled core refreshes continue when that optional diagnostic is unavailable.

The scheduler does not place trades. Engine remains the execution authority.
