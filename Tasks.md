# Tasks

## GitHub issues (synced 2026-10-24)

Source: the 22 open issues of QWavey/Ping_Checker. Issue #1 is an umbrella audit. Its 21 bullets are each filed as their own issue (#2 to #38), so they are tracked below under those numbers. Line numbers refer to the current Ping_Checker.py.

- [ ] #2 Full response body downloaded for every request — Ping_Checker.py:85 — FIX — open
- [ ] #3 Dependency not pinned or declared — Ping_Checker.py:2 — SKIP — skipped: improvement, not a defect; the script runs on the current requests release
- [ ] #4 No ceiling or target check on request volume — Ping_Checker.py:66, 122 — HELD — attack behaviour, needs authorization context
- [ ] #5 Size printed but never sent — Ping_Checker.py:71, 89, 94 — FIX — open
- [ ] #7 max_requests help says requests, but it counts loop iterations — Ping_Checker.py:122 — FIX — open
- [ ] #7 max_requests does not cap requests sent (stacking sends 1 to 10 per iteration) — Ping_Checker.py:66, 82 — HELD — attack behaviour, needs authorization context
- [ ] #9 Speed has no effect unless Delay is dynamic (README wording) — README.md:23 — FIX — open
- [ ] #9 Speed-derived delay applied under Delay none and fixed — Ping_Checker.py:73-80 — HELD — attack behaviour, needs authorization context (changes request pacing)
- [ ] #11 Network and URL errors reported as target denials — Ping_Checker.py:89-101 — FIX — open
- [ ] #13 Slow speed branch never changes the delay — Ping_Checker.py:63, 73-74 — HELD — attack behaviour, needs authorization context (changes request pacing)
- [x] #15 Unbounded size growth overflows float — Ping_Checker.py:71 — FIX — fixed in d228135
- [ ] #17 Mode prompt runs before argument checks; max_requests below 1 accepted — Ping_Checker.py:116-126 — FIX — open
- [ ] #19 Elapsed time measured with wall-clock time — Ping_Checker.py:84, 86 — FIX — open
- [ ] #21 Speed ignored unless Delay is dynamic (README wording) — README.md:23 — FIX — open (same change as #9)
- [ ] #21 Slow branch under dynamic delay sleeps the same as fixed — Ping_Checker.py:63, 73-80 — HELD — attack behaviour, needs authorization context (changes request pacing)
- [ ] #23 Size and growth settings only change a printed number — Ping_Checker.py:71, 89, 94; README.md:14, 24-25, 80 — FIX — open
- [ ] #25 Network errors reported as denials — Ping_Checker.py:99-101 — FIX — open (same change as #11)
- [ ] #27 Mode prompt runs before argument parsing — Ping_Checker.py:116-123 — FIX — open (same change as #17)
- [ ] #29 URL and max_requests not validated — Ping_Checker.py:122-126 — FIX — open (the http/https scheme check is in d228135; host and minimum value still to do)
- [ ] #31 Latency timed with wall-clock time — Ping_Checker.py:84, 86 — FIX — open
- [ ] #31 Printed time does not say what it covers — README.md (Notes) — FIX — open
- [ ] #31 Shared requests.Session for the whole run — Ping_Checker.py:85 — HELD — attack behaviour, needs authorization context (connection and cookie reuse change what the target receives)
- [ ] #32 No tests and no dependency manifest — repo root — SKIP — skipped: improvement, not a defect
- [x] #34 README usage command and clone URL wrong — README.md:34, 42 — FIX — fixed in d228135
- [ ] #36 Advanced-mode prompt re-asks silently on bad input — Ping_Checker.py:138-143 — FIX — open
- [ ] #38 Duplicated test-type lookup and unreachable fallback — Ping_Checker.py:26-37, 108-112, 163-165 — SKIP — skipped: refactor, current behaviour is correct
