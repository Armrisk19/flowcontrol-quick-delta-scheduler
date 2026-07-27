# FLOWCONTROL Resilient Low-Latency Scheduler v9.1.0

This scheduler refreshes Quick state every five minutes, the opportunity queue every ten minutes, the persistent graph every fifteen minutes, macro state hourly, and official sources every six hours. After each fast lane it writes one packed Engine feed snapshot for all five feeds and twenty identifiers.

Scheduled endpoint failures are warnings, preserve last-known-good state, and keep Engine-native fallback active. A manually dispatched strict verification run fails only on a real version-contract, universe, or critical-readiness mismatch.

The workflow accepts either secret naming pair:

- `FLOWCONTROL_GATEWAY_BASE_URL` or `FLOWCONTROL_GATEWAY_URL`
- `OMNI_COGNITIVE_GATEWAY_TOKEN` or `FLOWCONTROL_GATEWAY_TOKEN`

Disable or delete every older scheduled workflow, especially Persistent Opportunity Graph Scheduler v7.0.0, after v9.1.0 is installed and manually verified.
