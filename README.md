# FLOWCONTROL Exact Scoring Scheduler v1.6.4

This release uses a new workflow filename and a new visible Actions title so the current scheduler cannot be confused with an older workflow.

Upload these files:

- `.github/workflows/flowcontrol-scoring-ledger-v1.6.4.yml`
- `EXPECTED_RELEASE.json`
- `README.md`

Remove the older workflow file:

- `.github/workflows/flowcontrol-quick-delta.yml`

Run only:

- `FLOWCONTROL Exact Scoring Scheduler v1.6.4`

Expected feed contract:

```text
PUBLIC_NUMERIC_MARKET_DATA_ONLY
```

A successful run prints:

```text
FLOWCONTROL scheduler verification PASS
```
