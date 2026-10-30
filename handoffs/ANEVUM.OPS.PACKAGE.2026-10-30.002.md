# GitHub restructure — progress handoff

Session: `ANEVUM.OPS.PACKAGE.2026-10-30.002.COMPLETE-GITHUB-RESTRUCTURE`  
Snapshot: October 30, 2026. **The restructure is in progress.** This record is public-safe; private deployment details and recovery evidence belong in private operational records.

## Completed

- [Public project registry](../PROJECT_REGISTRY.md) created and linked from the GitHub profile. The ANEVUM web repository homepage points to the official site.
- Brandle and CristyBreathe standalone source imports were revalidated. Main-branch file comparison found all 20 Brandle files identical to the original source tree and 30 of 31 CristyBreathe files identical; the standalone README differs. Both imported commits passed standalone CI.
- [Brandle PR #2](https://github.com/anevum/brandle/pull/2) adds integration tests for the built Worker and its twelve assets. The PR check and [main check](https://github.com/anevum/brandle/actions/runs/41105145571) passed. [PR #3](https://github.com/anevum/brandle/pull/3) updates standalone instructions. Live Wild Run accepted and scored one guess.
- [Severance PR #1](https://github.com/anevum/severance/pull/1) recovers the Godot prototype and the separate offline world-state lab. The [headless](https://github.com/anevum/severance/actions/runs/41105639854), [browser](https://github.com/anevum/severance/actions/runs/41105639746), and [125-test lab](https://github.com/anevum/severance/actions/runs/41105639884) checks passed on the merge commit. The simulator is not integrated into the game.
- Original Godot history and the existing draft remain in [anevum-web PR #788](https://github.com/anevum/anevum-web/pull/788). The standalone import is a source snapshot, not a subtree-history import. The lab's original archive retains generated outputs and historical fixtures. Two compatibility tests generate new synthetic data from the archived V0.1 engine rather than publishing historical databases.
- A main-branch protection rule was prepared but GitHub account confirmation timed out; it is **not active**.

## Current source and release boundaries

- **Brandle:** standalone verification is in place, but the previous repository still owns its deployment workflow. Verify scoped credentials, a working rollback and exact release behavior before changing that ownership. Do not enable independent deployers simultaneously.
- **CristyBreathe:** the calendar candidate from [anevum-web PR #796](https://github.com/anevum/anevum-web/pull/796) is reconciled in [standalone draft PR #2](https://github.com/anevum/cristybreathe/pull/2). Its 11 application files match the original draft by Git blob ID and [standalone CI passed](https://github.com/anevum/cristybreathe/actions/runs/41106456230). Backup restoration, migration lineage, access and real-user acceptance remain release gates; the draft is not deployed.
- **Brandicade:** [draft PR #1](https://github.com/anevum/brandicade/pull/1) recovers the V1.0.1 static source and adds verification-only CI. All 14 static assets match those embedded in the live Worker by SHA-256. The deployed Worker also includes a cloud-save layer absent from that archive. The generated Worker header identifies GPLv3 while the archive contains an MIT license; investigate provenance and rights before finalizing, and recover server-side source without private configuration.
- **DevonStation:** a private development archive exists and contains operational snapshots. Build and verify a public-safe export rather than publishing the archive wholesale.
- **IdeaFlow:** earlier intake, analyzer and operations source and a separate meeting-presenter release have been located. The intake archive predates the current manual-processing change; do not treat it as the current production source without reconciliation. Preserve manual processing and necessary retention safeguards; exclude recordings, transcripts and private configuration.
- **CristyRusso.com:** a visual design concept exists, but its credentials, service descriptions, contacts and links need verification. It is not an approved production website.
- **Severance:** history remains recoverable in the original repository, but the imported snapshot has not incorporated those commits as ancestors. The two experiments remain independent; neither is a finished game.

## Cleanup and governance still open

The inspection found 848 branches, 280 open pull requests, 62 open issues and 35 workflow files in ANEVUM web, plus 121 Workers, one Pages project and 17 D1 databases. These are point-in-time counts, not a completed classification or deletion list. Of the 280 open PRs inspected by metadata, 267 were drafts and 185 targeted a branch that was also the head of another open PR. One pair shared a head but had different bases and distinct review purposes. These counts do not establish that the changes are duplicates or safe to close. Inspect ancestry and content before closing or deleting anything.

A limited environment-file check found no populated secret-like values in the two historical versions of the tracked ANEVUM web production environment file or the 22 historical versions of RHEN's tracked example environment file. This was a narrow pattern check, not a comprehensive credential or history scan.

Review the ANEVUM web release workflows and production route before removing any code. Keep the retired legacy production deployment disabled. Configure practical branch protection and required checks after identifying the checks that actually run for the intended changes. Review current and historical credentials, licensing and third-party rights; RHEN and Family Adventure Book now include Apache-2.0 licenses after the owner confirmed ownership; respect separately licensed dependencies and notices. No comprehensive secret-history audit, infrastructure cleanup, deployment handover or account-wide governance completion is claimed here.

## Continuation — 2026-10-30

- Verified the 12 accessible repositories and the handoff against live GitHub state. Brandicade, DevonStation, IdeaFlow and CristyRusso.com remain not fully imported. Do not mark them done based on README-only main branches.
- [ANEVUM web PR #797](https://github.com/anevum/anevum-web/pull/797) corrected inaccurate instructions about the retired deployment workflow and was squash-merged as `34b93f1f426f21ac9f8e63d0e0d5bad31b869a99`. Documentation change only; it does not authorize a production deployment.
- PR #797 CI failed **after** application tests and build, when the Wrangler preview response returned `preview.urls: []` and the workflow's `.preview.urls[0]` extraction exited 1. Failure was documented on the PR. Investigate the preview publication/URL contract and keep the check marked failed rather than bypassing privacy or runtime gates.
- Branch protection remains unconfirmed, and no deployment, secret, route, D1, public archive or production access ownership was changed during this continuation.

## Continuation — CI preview scope patch

- Opened [anevum-web PR #798](https://github.com/anevum/anevum-web/pull/798) to exempt root `README.md`-only edits from the otherwise fail-closed legacy Cloudflare preview stage. Mixed README/runtime edits still require preview; two regression tests were added. This is a source-control verification patch, not a production change.
- At handoff, the exact-head ANEVUM Verify and Repository migration verification runs were **queued**, not passed. Do not merge before results are inspected. If the preview step is skipped on the patch, that is by the narrow reviewed maintenance-file allowlist; all other offline safety checks remain.
- Cloudflare documentation confirms preview URL publication depends on explicit configuration and can be disabled. The actual reason the earlier Wrangler preview response returned an empty URL has not yet been established; do not change public preview accessibility without review.

## Continuation — verified PR #798 and repository README correction

- [ANEVUM web PR #798](https://github.com/anevum/anevum-web/pull/798) passed both `ANEVUM Verify` and `Repository migration verification` and was squash-merged on main at `30cc7eba5708901753aa88e9e05b227221646758`. Root README-only edits now bypass the unnecessary Cloudflare preview stage, while mixed/runtime changes still require that stage. This is a CI classification patch, not a production change.
- Replaced title-only main-branch READMEs in `devon-station`, `ideaflow`, `brandicade`, and `cristyrusso.com` with explicit factual project scopes, source provenance and recovery gates. These files do not add application code or transfer deployment ownership.
- Remaining gates: public-safe source recovery for DevonStation/IdeaFlow/CristyRusso.com, server-side recovery and licensing review for Brandicade, independently verified production cutovers, branch protection and historical source/secret audits. No mass branch/PR closures or deployment changes were attempted.

## Verification audit — 2026-10-30

- Published the evidence-based [completion audit](../AUDIT_2026-10-30.md) and linked it from the public project registry.
- Confirmed 12 public repositories; four still have README-only default branches. Existing Cloudflare Workers for Brandicade, DevonStation and IdeaFlow provide recoverable deployment material, but do not establish full publishable standalone source.
- GitHub ruleset-list reads returned empty; branch-protection reads were denied to this integration. No effective branch protection was verified.
- Brandicade and CristyBreathe draft heads had passing CI checks, but licensing, backend parity, private migration and access safeguards remain release gates. Do not merge or deploy based on CI alone.
- **Completion status remains NOT COMPLETE**; no production changes or destructive archive/branch cleanup were performed in this verification pass.

## Small job 001 — Brandle security policy (2026-10-30)

- Inspected exact change in [Brandle PR #4](https://github.com/anevum/brandle/pull/4): adds only `SECURITY.md`, directing private security reports to the existing owner address and prohibiting unsafe production probing.
- PR-head `verify` check passed, then PR was squash-merged at `391f10866438dd4f3541f217094860297bbec0a6`.
- Re-read `SECURITY.md` from main and confirmed successful main-branch `Brandle standalone verification` run `41117000501` against that exact commit.
- No Brandle production deployment, secrets, DNS, D1, or old deployer ownership changed. The Brandle cutover remains a separate gated job.

## Small job 002 — Brandle deployment ownership and rollback inventory (2026-10-30)

**Status: read-only audit completed; deployment cutover NOT authorized or performed.**

- Both `anevum/brandle` and `anevum/anevum-web/games/brandle` have identical Git blob IDs for `build-worker.mjs` (`123bd0c3ef48c6f65c1609a4dced3b2533e1fc4c`) and `wrangler.toml` (`2f8bab43bd69eb97b13c21f94db13eb449980885`). Both target only `brandle-glimmer-grove`, with `workers_dev = true` and compatibility date `2026-10-29`.
- `anevum/anevum-web/.github/workflows/deploy-brandle.yml` is still able to deploy from the monorepo on selected `main` game-source changes and manually via `workflow_dispatch`. A PR cannot deploy through that workflow. The standalone repo's `.github/workflows/ci.yml` only builds and verifies and has no deployment step.
- Cloudflare Worker `brandle-glimmer-grove` has its `workers.dev` subdomain and previews enabled. The settings endpoint reported **zero runtime bindings**; this does not establish the permissions of the GitHub deployment credential. No databases or custom domain routes were found in its standalone Wrangler config.
- Cloudflare's latest deployment ID `86970d97-7975-45e5-a000-0fba9a7379f6` (2026-10-30 01:16:40 UTC) points 100% to version `1c48deb3-6c35-4b9b-9d84-a37d2596ca70`. Three earlier versions remain in Cloudflare's version listing (`ba5fe54e-142d-4faf-b75c-4e95d88f3d69`, `7e854856-1457-4b9b-8bf6-83615f2eaadb`, `2e9071b8-8743-4383-af1d-a457b7ead4d2`). The current deployment source is recorded as Wrangler; these are **potential rollback targets**, not proven reversible releases.
- Standalone CI after security-policy merge passed: [GitHub run 41117000501](https://github.com/anevum/brandle/actions/runs/41117000501), commit `391f10866438dd4f3541f217094860297bbec0a6`. Build reproducibility from a local fresh checkout, exact-byte parity to live deployed code, and a rollback rehearsal were not established in this read-only job.

**Next small job:** Audit existing credential scopes and permitted deployment mechanism without exposing secret values; recover the exact live release artifact, run isolated build/route/browser acceptance checks, and establish a tested rollback procedure. Then perform a single-deployer cutover: disable the old monorepo deploy path before enabling a new scoped standalone deploy path. Recheck real Worker version/URL and both workflows afterward. Avoid changing production for the audit-only step.
