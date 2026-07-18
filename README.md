# FLOWCONTROL Public Quick Delta Scheduler v1.3.0

This public GitHub Actions repository refreshes the FLOWCONTROL Gateway Quick Delta every five minutes and verifies the synchronized v8.5.0 / v24.5.0 release.

## Repository secrets

Create these GitHub Actions secrets:

- `FLOWCONTROL_GATEWAY_URL` — the production Vercel base URL, such as `https://example.vercel.app`
- `FLOWCONTROL_GATEWAY_TOKEN` — the same bearer token configured for the Gateway refresh route

## Operation

The workflow:

1. Calls `POST /api/quick-delta-refresh`.
2. Reads `/api/health`, `/api/release-manifest`, `/api/readiness`, and Quick Delta status.
3. Confirms Gateway `8.5.0`, strategy contract `24.5.0`, 20 exact markets, fingerprint `f18daa19f9ed41c06720349b`, and Quick Delta age of 300 seconds or less.
4. Accepts `READY` and core-synchronized `DEGRADED` readiness states so optional intelligence availability remains visible while the five-minute refresh continues.

Run **FLOWCONTROL Five-Minute Quick Delta v1.3.0** manually after deployment. A successful run prints `FLOWCONTROL scheduler verification PASS`.

This repository contains public scheduling logic only. Account data, wallet keys, exchange keys, positions, and orders remain outside this repository.
