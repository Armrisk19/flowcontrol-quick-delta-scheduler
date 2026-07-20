# FLOWCONTROL Top-20 Market Mastery Scheduler v2.2.0

Refreshes the live quality-selected top twenty from a twenty-eight-market candidate pool, refreshes opportunity and macro data, creates the exact 120-plan board for the selected universe, and verifies Gateway v10.2.0 / Strategy v26.2.0 contracts.

The first post-deployment manual run should use `force_universe_refresh: true`, `force_board_refresh: true`, and `perform_openai_live_check: false`. Run once more with the live check enabled after the first pass.

The public repository needs repository activity at least once every 60 days so GitHub does not automatically disable scheduled workflows.
