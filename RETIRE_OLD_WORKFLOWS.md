# Retire old workflow schedules

The email titled `FLOWCONTROL Persistent Opportunity Graph Scheduler v7.0.0: All jobs have failed` belongs to an older workflow in the private Gateway repository. It is not the v9.1.0 scheduler.

In the private `flowcontrol-omni-x-gateway` repository:

1. Open **Actions**.
2. Select **FLOWCONTROL Persistent Opportunity Graph Scheduler v7.0.0**.
3. Open the `...` menu and choose **Disable workflow**.
4. In **Code**, delete its matching file under `.github/workflows/` when convenient.
5. Disable any other v7 or v8 scheduled refresh workflow after v9.1.0 is green.

Keep only the current v9.1.0 scheduler repository active. Historical failed emails can remain in Gmail; they do not change the deployed code.
