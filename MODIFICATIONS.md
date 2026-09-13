# MODIFICATIONS

This repository is a **mirror / archival fork** of
[`wgpsec/ENScan_GO`](https://github.com/wgpsec/ENScan_GO)
(commit `9969d5156c2fec80d5f4724b8d6d6bbb45471933`,
authored 2026-03-28 by `keac <admin@wgpsec.org>`).

## Why this mirror exists

The upstream repository `wgpsec/ENScan_GO` was deleted by its owner
in 2026. Apache License 2.0 §4 ("This License is irrevocable") makes
the deletion irrelevant for redistribution rights; the original
LICENSE remains in this repository verbatim, and the original git
history (182 commits, ending at `9969d51`) is preserved unchanged.

This mirror was created so that downstream consumers — most
notably the [`srcradar`](https://github.com/wgpsec/srcradar)
Docker image — can `git clone` a known-good, verifiable source
instead of relying on the deleted upstream or unvetted
third-party forks (`mssky9527/ENScan_GO`, `zh0u9527/ENScan_GO`)
that appeared after the deletion.

## Files modified by downstream consumers

The `9969d51` HEAD in this repository is byte-for-byte identical to
the upstream at the deletion commit. **No modifications to the
upstream source live on the `main` branch.**

Downstream changes (e.g. qimai / 七麦 module additions made by
srcradar) are kept **out of this repository** and documented in
the consumer's own project. See the consumer's `MODIFICATIONS.txt`
file for the list of files changed and the rationale.

This separation keeps the mirror a faithful archival copy; any
consumer patch lives as a separate layer on top.

## Apache-2.0 §5 compliance as a redistributor

| §5 clause | Requirement | How this repository satisfies it |
|-----------|-------------|----------------------------------|
| §5(a) | "give any other recipients of the Work or Derivative Works a copy of this License" | LICENSE file (11 KB, full Apache-2.0 text) preserved verbatim at the repository root. SHA-256: `c71d239df91726fc519c6eb72d318ec65820627232b2f796219e87dcf35d0ab4` — matches the upstream's LICENSE byte-for-byte. |
| §5(b) | "indicate which files were modified" | This file (`MODIFICATIONS.md`) and the consumer's own `MODIFICATIONS.txt` list every modified file and what changed. The mirror itself contains zero modifications to upstream source. |
| §5(c) | "preserve in source form ... all copyright, patent, trademark, and attribution notices" | Upstream copyright notice (`keac` per LICENSE boilerplate) is preserved verbatim in LICENSE; no notices were stripped from any source file. |
| §5(d) | "if the Work includes a NOTICE file ... include a readable NOTICE" | Upstream did NOT ship a NOTICE file at the mirrored commit; this obligation is N/A. The original author is credited in this file and in each consumer's documentation. |

## Provenance verification

Anyone can verify this mirror's provenance:

```sh
# 1. LICENSE hash must match the upstream record
sha256sum LICENSE
# Expected: c71d239df91726fc519c6eb72d318ec65820627232b2f796219e87dcf35d0ab4

# 2. HEAD must be upstream commit 9969d51
git log -1 --format='%H'
# Expected: 9969d5156c2fec80d5f4724b8d6d6bbb45471933
git log -1 --format='%an <%ae>'
# Expected: keac <admin@wgpsec.org>
```

The first 182 commits in this repository are the original upstream
history with their original authors and dates preserved.

## Mirror vs fork policy

This is an **archival mirror**, not a development fork:

- The `main` branch tracks upstream HEAD exactly; no source changes.
- Tags in this repository mark upstream historical commits only.
- New tags may be added by the mirror maintainer to mark archival
  points, but they do not introduce new code.
- Downstream consumers that need a modified version should maintain
  their own fork and reference it explicitly; they should not push
  patches into this mirror.

## Credits

- Original work: `wgpsec/ENScan_GO`, copyright `keac` and contributors.
- License: Apache License 2.0 (see `LICENSE`).
- Mirror maintained by: `usdagfhjkda` (see git commit history).
