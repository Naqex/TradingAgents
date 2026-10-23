# Upstream sync — 2026-10-23

Merged upstream `v0.7.0` / `main` at
`e8f5503e9b86d5c2710b0c76b1f686703968c9df` into local `94e11a4`.
The fork retains its custom history; upstream is now an ancestor.

New behavior includes isolated parallel analyst subgraphs, a single join barrier,
bounded tool rounds, run-scoped data config, quick/deep providers and endpoints,
concurrent memory settlement, report settings/HTML and point-in-time fixes.

Local safe provenance and strict atomic publication remain in the new module
layout. Route fingerprints cover both tiers; manifests bind exact portfolio
identity, tool limits and the parallel workflow revision. Research outputs stay
advisory with `execution_capability=false`. `uv.lock` remains authoritative.

Validation in an isolated Windows/Python 3.12 environment: 1397 offline tests and
100 subtests passed, four platform/optional-SDK skips and one integration
deselection. Final portfolio/import changes passed 165 focused tests. Five initial
suite failures also reproduced on pristine upstream and were corrected as Windows
test expectations; no production shell permission was relaxed. Scoped Ruff and
Git whitespace checks passed. Test transport guards block external network.

Run `uv sync --locked --extra dev` before using the updated checkout. The upstream
layout changes imports under `agents`, `memory`, and `dataflows/vendors`; local
demo imports have been adapted, without running its external-data demo.

Old sequential graph checkpoints are deliberately not resumed. Previously settled
memory outcomes retain their old scoring semantics; use fresh run results to
compare the new first-close-after-decision convention.

Optional upstream ChatGPT OAuth is not connected to WMREPLAY and no login occurred.
Its Windows credential ACLs have not been verified; POSIX mode-bit tests do not
establish Windows privacy. Product integration continues to use registered gateway
routes, and must disable CLI update/announcement checks. This sync does not itself
integrate a shared worker, enable provider inference or authorize broker execution.

The workspace architecture review and raw offline receipts live in
`../../planning/research/ai-architecture-review-20261023/`.
