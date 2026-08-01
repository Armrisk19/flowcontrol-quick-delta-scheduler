# FLOWCONTROL Adaptive Learning Scheduler v9.3.0

This scheduler is matched to Gateway v4.5.0 and Omni X v38.8.0.

It performs only jobs that actually exist in the gateway:

- refresh the bounded adaptive profile every hour;
- refresh/check the persistent macro-event ledger every hour;
- verify full gateway health, capabilities, and adaptive feed output;
- run a stricter six-hour release and persistence check;
- preserve last-known-good adaptive state when an advisory refresh fails.

It deliberately removes the old quick-delta, queue, opportunity-graph, packed-feed, readiness, and release-manifest calls because those routes do not exist in the v4.5.0 gateway.

Required GitHub secrets:

- `FLOWCONTROL_GATEWAY_BASE_URL` or `FLOWCONTROL_GATEWAY_URL`
- `OMNI_COGNITIVE_GATEWAY_TOKEN` or `FLOWCONTROL_GATEWAY_TOKEN`

The gateway uses the dedicated bearer token as a private persistence scope when Engine does not provide an agent instance ID. Upstash must remain configured in Vercel for durable learning across deployments.
