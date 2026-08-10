# OMEGA Development Record

This is the public process record for OMEGA. It documents important failures,
corrections, and locked evidence rather than presenting the final software as a
straight-line success. Henry Barrientos directed the project, operated the
workflow, reviewed failures, and assembled the evidence. Public TESS data,
published catalogs, open-source scientific packages, and AI-assisted coding are
credited inputs; they were not invented by the developer.

## Evidence retained

The locked benchmark retains the pre-screen candidate pool, final target list,
deterministic injection recipes, scientific source manifest, normalized-input
manifest, threshold manifest, per-method result records, final reports, and
independent completion audits. SHA-256 hashes connect those artifacts and make
later changes detectable.

## Important failures and corrections

1. An early detector window diluted 1--3 hour signals and recovered no injected
   events. Injection recovery exposed the issue, leading to matched 1, 3, 8,
   and 16 hour searches.
2. TIC 307109526 was rejected after gradient, centroid, and neighboring-source
   evidence showed that its event was not cleanly source-localized.
3. A compelling single target and an initial candidate campaign could not
   establish broad performance. A locked comparative benchmark was created to
   test that stronger claim.
4. Full-resolution and 20-minute TLS trials on TIC 31065777 reached the
   600-second ceiling. They remain operational timeouts, not scientific misses.
5. Only 239 of 349 initially eligible hosts could accept exactly 3--5 sampled
   long-period injections. The candidate pool was expanded instead of weakening
   the frozen recipe rule.
6. The phrase "quiet control" was replaced by "screened no-event control";
   absence of a detected event does not prove a star is intrinsically quiet.
7. Real-artifact claims that could not be verified were replaced with explicitly
   synthetic deterministic artifact controls.
8. An integration test found competing structure in older eclipsing-binary
   candidates. Detector-neutral TIC hosts were added and older candidates were
   isolated as a stress subgroup.
9. Targets previously selected by OMEGA as having no significant event were
   removed from the scored negative cohort to avoid circular evaluation.
10. A fixed 2,000-period BLS grid was too coarse for multi-year baselines. A
    baseline-aware grid capped at 500,000 periods replaced it before locking.
11. An end-to-end dry run exposed two optional truth fields treated as required.
    The runner was corrected before validation or test results existed.
12. A coordinate audit found close or duplicate candidates. Final selection
    admitted at most one object from each close pair and required zero
    cross-split pairs.
13. Only 2 of 18 unflagged catalog systems met the exact event-sampling rule.
    The other 498 positives were labeled deterministic injections, narrowing
    the allowed claim to controlled recovery rather than real-sky yield.
14. A checkpoint auditor initially searched for abbreviated provenance keys and
    falsely reported mismatches. The audit, not the results, was corrected;
    subsequent checks found no mismatches or duplicate identities.
15. The completion auditor initially treated the intentionally absent local
    light-curve cache as an integrity failure. It was changed to separate
    compact-manifest verification from optional server-side input-byte hashing.
16. Exact package versions differed between the server and local computer. The
    server's real Python, platform, hardware policy, and package environment
    were captured without restarting or altering the run.
17. The first auditor trusted manifests to declare expected hashes and counts.
    It was strengthened with five independently frozen anchors and absolute
    cohort requirements.
18. Matching threshold files did not prove how thresholds were calculated. The
    auditor was extended to recompute every threshold from negative validation
    controls and verify the control-identity hash.
19. Result auditing was expanded from labels and aggregate hashes to truth
    fields, source filename, input SHA, byte size, row count, analysis view,
    method version, and search range.
20. The final report's own claim-gate Boolean was not accepted at face value.
    The auditor independently reconstructs the decision and required reasons.
21. The locked sequential run was much slower than target counts suggested.
    Concurrency was not changed after source and resource-policy lock because
    that would invalidate the paired runtime comparison.
22. TLS validation made the required calibration-success count mathematically
    unreachable. The evaluator continued without changing the limit or
    discarding results, and calibration was marked insufficient.
23. TLS also produced a zero-size-array execution error on valid retained
    inputs. Affected rows were preserved as operational failures rather than
    rerun after inspection.
24. Thresholds were frozen using successful negative validation controls before
    any untouched test result existed. TLS retained an observed-control
    threshold while remaining explicitly insufficiently calibrated.
25. OMEGA and BLS completed all 1,200 test records without operational failure.
    OMEGA's narrow exact-period advantage was driven by deterministic injections;
    neither method exactly recovered either of the two real catalog positives.
26. TLS completed its 120-row test subset with 53 successes, 61 bounded
    timeouts, and six retained failures. Its low operational success and
    insufficient calibration prevent a reliable overall comparison.
27. The final claim gate failed as designed. Both independent completion audits
    passed 22 of 22 checks over 2,180 records, while the scientific conclusion
    remained: **no comparative-advantage claim is supported by this locked
    benchmark.**

## Frozen Version 1 anchors

The final cohort contained 1,000 targets: 500 positive and 500 negative trials,
split into 200 development, 200 validation, and 600 untouched test targets.

- scientific source: `6fd148df2093589461ff1dcb7f2a2d128ce43fc4b90cb11c65bc538a05e7b4bc`
- target list: `c537982e138772aabbdfa205773b96eb275fa1bd6877d7bddaebac665372ba6f`
- candidate pool: `0ef9e72088b4d84fb5e62c36d6768b4cedfc9ac5290ba6d981e6370e78e7f895`
- deterministic recipes: `4b1c16daf816119535da27fa2f13c30ddf56a2aa57dbde061b0a8ef3a350a24f`
- normalized inputs: `5c51cf78184c679389a46daf90fef2c5b6ce45cb95eb38fad2b678a894e0a570`

The final run produced 2,180 compact method records: 2,081 successful
executions, 92 bounded timeouts, and seven retained execution failures. On the
test positives, OMEGA matched about 69.7% of injected truth-window event centers
but recovered exact periods for only 9 of 300 targets overall: 9 of 298
injected and 0 of 2 real-catalog targets. The benchmark therefore supports
testing a human event-triage workflow, not claiming an all-purpose discovery
system or general superiority.

## How to describe the work

A precise description is:

> I developed and operated a reproducible TESS dimming-search project, then
> designed a locked 1,000-target benchmark after learning that a compelling
> case study and a candidate campaign did not establish broad performance. I
> preserved catalog snapshots, deterministic injections, operational failures,
> source and data hashes, and an untouched test split so the final claim would
> be decided by evidence rather than the outcome I hoped to see.

Do not imply that Astropy, Lightkurve, TLS, public catalogs, public TESS data,
or AI assistance were personally invented. Honest attribution strengthens the
work.
