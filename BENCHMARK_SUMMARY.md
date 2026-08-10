# OMEGA Benchmark V1 Summary

## Conclusion

**No general comparative-advantage or real-sky superiority claim is supported
by this locked benchmark.**

The benchmark tested a narrow 40–300 day, 3–5-event use case. Most positive
examples were deterministic injections; only two untouched-test positives were
real catalog systems.

## Untouched test results

| Method | Targets | Exact recall | Harmonic-inclusive recall | False-alarm rate | Operational failures | Median runtime |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| OMEGA | 600 | 0.030 | 0.030 | 0.040 | 0 | 4.24 s |
| Astropy BLS | 600 | 0.000 | 0.000 | 0.070 | 0 | 158.07 s |
| Transit Least Squares | 120 | 0.050 | 0.083 | 0.032 | 67 | 604.99 s |

## Paired differences

- OMEGA minus BLS exact recall: `+0.030`; paired 95% interval
  `[0.013, 0.050]` across 300 positive targets.
- OMEGA minus BLS false-alarm rate: `-0.030` across 300 mutually
  successful controls.
- OMEGA minus TLS exact recall: `-0.017`; paired 95% interval
  `[-0.083, 0.050]` across the 60-positive TLS subset.

## Interpretation

OMEGA was faster than the configured comparison paths and completed its
assigned targets reliably. Those are engineering results, not proof that it is
a better astronomical detector. Exact recovery remained low, the positive
cohort was injection-dominated, and neither OMEGA nor BLS exactly recovered
either of the two real-catalog positives.

The evidence supports a narrower human-workflow experiment: measure whether a
transparent queue helps reviewers work faster without suppressing events they
consider important.

## Frozen anchors

- Scientific source: `6fd148df2093589461ff1dcb7f2a2d128ce43fc4b90cb11c65bc538a05e7b4bc`
- Candidate pool: `0ef9e72088b4d84fb5e62c36d6768b4cedfc9ac5290ba6d981e6370e78e7f895`
- Target list: `c537982e138772aabbdfa205773b96eb275fa1bd6877d7bddaebac665372ba6f`
- Injection recipes: `4b1c16daf816119535da27fa2f13c30ddf56a2aa57dbde061b0a8ef3a350a24f`
- Normalized inputs: `5c51cf78184c679389a46daf90fef2c5b6ce45cb95eb38fad2b678a894e0a570`
- Thresholds: `311061f8d4f2b8900e10f9299c2e92de478199c9f9a96242072bcc7fc0cf52a1`

The complete machine-readable record is retained privately with the original
artifacts.
