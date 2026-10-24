# Tasks

## Audit 2026-10-24

- [x] **[MED]** README usage command names a file that does not exist — README.md:42 — the docs say `python Ping_Test.py`, but the script is `Ping_Checker.py`, so the first documented command fails with "No such file or directory". — fixed in d228135
- [ ] **[MED]** Speed has no effect unless Delay is dynamic — Ping_Checker.py:72-79 — `current_delay` is read only in the `dynamic` branch (line 79), so with Delay `none` or `fixed` the Speed option changes nothing. 48 of the 72 test types run identically across the three Speed values. Left open: making Speed change pacing changes the load the tool generates, which the owner should decide.
- [ ] **[MED]** Payload size is never sent — Ping_Checker.py:84 — `requests.get(url)` sends no body, yet the printed `size=...B` (line 93) and the Size and Growth settings (lines 68-70) only change that number, so the output reports a payload the server never receives. Left open: sending a body means changing the request method, which is a design choice for the owner.
- [x] **[LOW]** Invalid URL reported as a denial — Ping_Checker.py:98-100 — `--url example.com` (no scheme) makes `requests` raise MissingSchema, which the handler prints as "Pings denied ... (request failed)", so a typo looks like the server blocking requests. — fixed in d228135
- [x] **[LOW]** Crash on a long run with Size bigger and Growth rapid — Ping_Checker.py:69-70 — `size` is multiplied by 1.2 on every iteration with no cap; after about 3,868 iterations it overflows the float range and the run dies with `OverflowError: cannot convert float infinity to integer`, even though the server never denied a request. — fixed in d228135
- [x] **[LOW]** Install clone URL points at the old owner — README.md:34 — the clone URL is `XQuantumWaveX/Ping_Checker`, but the repo's origin is `QWavey/Ping_Checker`, so the install step may fail if the old owner path is not redirected. — fixed in d228135
