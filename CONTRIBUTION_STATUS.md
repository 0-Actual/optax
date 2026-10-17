# Optax correction: preserved in this fork; not submitted upstream

Decision recorded from the owner's reported time: **October 17, 2026, 3:45 a.m. Eastern (UTC-04:00)**. This is an owner-reported, minute-precision timestamp.

## Disposition

The owner declined Google's Individual Contributor License Agreement and ended the upstream submission effort because its licensing and commercial-use terms did not fit the owner's preferences. No Google CLA was signed and no upstream pull request was opened. This was the owner's decision, not a rejection by Google or its maintainers.

A fork **was** created: `0-Actual/optax`. The correction and validation remain public here. The absent step is upstream submission, not forking. This status note does not change the repository's existing license or retroactively withdraw permissions already granted under that license.

## Preserved correction and evidence

- Tested code commit: [1c7e94b42f47899bd98021ed03fe4e0088be4a41](https://github.com/0-Actual/optax/commit/1c7e94b42f47899bd98021ed03fe4e0088be4a41).
- Public candidate commit time: October 17, 2026, 02:39:36 Eastern.
- [Hosted validation](https://github.com/0-Actual/optax/actions/runs/39010905993) completed its numerical check at 02:43:32 Eastern.
- Added regression cases on the original baseline: **30 failed, 4 passed**.
- Corrected selected suites: **55 tests and 30 subtests passed**. These are not 85 independent tests or 30 distinct defects.
- The correction replaces arithmetic zero masks with selection, preserving the zero-intermediate-update and accumulator-reset contracts for nonfinite inputs.
- The validation workflow is on a separate branch. Full-suite, GPU/TPU, performance, novelty, maintainer approval and merge are not claimed.

The original source, baseline failures, corrected source and validation history remain available. This documentation-only addition does not alter the tested code.

## Assistant errors and process correction

This work was prepared with OpenAI Codex assistance. The assistant identified the Google CLA requirement during the initial repository review but did not adequately explain its commercial implications before substantial implementation and public fork publication. The separate implications of the existing open-source license were also explained too late. This was a guidance and sequencing failure.

Local dependency setup also consumed avoidable time before the local JAX runtime's CPU-feature incompatibility was identified. Numerical tests ultimately ran successfully on the hosted CPU runner; the local collection failure was not a failed numerical assertion.

For subsequent work, contribution terms, publication licensing, rights representations and resource requirements must be presented before substantial implementation or publication. A request to examine another project is not acceptance of a new agreement.

No private research archive is included in this correction or status note.
