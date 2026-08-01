# FLOWCONTROL Action Signal Scheduler v9.3.1

This scheduler keeps the deterministic action signal fresh without pretending to control Engine orders.

- Every 5 minutes: refresh the 15m + 1h action signal for the 20-market universe.
- Every hour at :07: refresh bounded adaptive learning from verified closed trades.
- Every six hours at :37: refresh macro/event memory and verify the coordinated release.
- Manual strict run: refresh all components and fail on a version, storage, route, or signal mismatch.

Required GitHub Actions secrets:

- `FLOWCONTROL_GATEWAY_BASE_URL` (optional when using the included production default)
- `OMNI_COGNITIVE_GATEWAY_TOKEN`

The scheduler refreshes gateway intelligence. It does not invoke private Engine reviews, sign orders, or submit trades.

Install the workflow at:

`.github/workflows/FLOWCONTROL_Scheduler_v9.3.1_WORKFLOW.yml`

Disable the v9.3.0 workflow before enabling this version.
