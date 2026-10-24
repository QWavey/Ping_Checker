# Tasks

## GitHub issues (synced 2026-10-24)

Source: the 22 open issues of QWavey/Ping_Checker. Issue #1 is an umbrella audit. Its 21 bullets are each filed as their own issue (#2 to #38), so they are tracked below under those numbers. Line numbers refer to the current Ping_Checker.py.

- [x] #2 Full response body downloaded for every request — Ping_Checker.py:85 — FIX — fixed in 25e705a
- [ ] #3 Dependency not pinned or declared — Ping_Checker.py:2 — SKIP — skipped: improvement, not a defect; the script runs on the current requests release
- [ ] #4 No ceiling or target check on request volume — Ping_Checker.py:66, 122 — HELD — attack behaviour, needs authorization context
- [x] #5 Size printed but never sent — Ping_Checker.py:71, 89, 94 — FIX — fixed in f823668 (value labelled nominal, not sent)
- [x] #7 max_requests help says requests, but it counts loop iterations — Ping_Checker.py:122 — FIX — fixed in 872f85f
- [ ] #7 max_requests does not cap requests sent (stacking sends 1 to 10 per iteration) — Ping_Checker.py:66, 82 — HELD — attack behaviour, needs authorization context
- [x] #9 Speed has no effect unless Delay is dynamic (README wording) — README.md:23 — FIX — fixed in 18d0f5c
- [ ] #9 Speed-derived delay applied under Delay none and fixed — Ping_Checker.py:73-80 — HELD — attack behaviour, needs authorization context (changes request pacing)
- [x] #11 Network and URL errors reported as target denials — Ping_Checker.py:89-101 — FIX — fixed in 71fff32
- [ ] #13 Slow speed branch never changes the delay — Ping_Checker.py:63, 73-74 — HELD — attack behaviour, needs authorization context (changes request pacing)
- [x] #15 Unbounded size growth overflows float — Ping_Checker.py:71 — FIX — fixed in d228135 (cap at 1e300)
- [x] #17 Mode prompt runs before argument checks; max_requests below 1 accepted — Ping_Checker.py:116-126 — FIX — fixed in 77f3df6
- [x] #19 Elapsed time measured with wall-clock time — Ping_Checker.py:84, 86 — FIX — fixed in d8485ad
- [x] #21 Speed ignored unless Delay is dynamic (README wording) — README.md:23 — FIX — fixed in 18d0f5c (same change as #9)
- [ ] #21 Slow branch under dynamic delay sleeps the same as fixed — Ping_Checker.py:63, 73-80 — HELD — attack behaviour, needs authorization context (changes request pacing)
- [x] #23 Size and growth settings only change a printed number — Ping_Checker.py:71, 89, 94; README.md:14, 24-25, 80 — FIX — fixed in f823668 and 967223a
- [x] #25 Network errors reported as denials — Ping_Checker.py:99-101 — FIX — fixed in 71fff32 (same change as #11)
- [x] #27 Mode prompt runs before argument parsing — Ping_Checker.py:116-123 — FIX — fixed in 77f3df6 (same change as #17)
- [x] #29 URL and max_requests not validated — Ping_Checker.py:122-126 — FIX — fixed in d228135 (scheme) and 77f3df6 (host, minimum of 1)
- [x] #31 Latency timed with wall-clock time — Ping_Checker.py:84, 86 — FIX — fixed in d8485ad
- [x] #31 Printed time does not say what it covers — README.md (Notes) — FIX — fixed in 18d0f5c
- [ ] #31 Shared requests.Session for the whole run — Ping_Checker.py:85 — HELD — attack behaviour, needs authorization context (connection and cookie reuse change what the target receives)
- [ ] #32 No tests and no dependency manifest — repo root — SKIP — skipped: improvement, not a defect
- [x] #34 README usage command and clone URL wrong — README.md:34, 42 — FIX — fixed in d228135
- [x] #36 Advanced-mode prompt re-asks silently on bad input — Ping_Checker.py:138-143 — FIX — fixed in a355ba0
- [ ] #38 Duplicated test-type lookup and unreachable fallback — Ping_Checker.py:26-37, 108-112, 163-165 — SKIP — skipped: refactor, current behaviour is correct
