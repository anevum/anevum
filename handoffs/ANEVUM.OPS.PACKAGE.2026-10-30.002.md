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

## Small job 003 — Brandle deployed-asset parity (2026-10-30)

**Read-only integrity verification completed; cutover still pending.** Downloaded the current Cloudflare `brandle-glimmer-grove` Worker module through the authorized API, decoded its generated `BASE64` asset table, and computed Git blob SHA-1 digests using the exact `blob <byte-size>\0<bytes>` Git-object hashing method. Compared those hashes with GitHub contents metadata on the standalone `anevum/brandle` main branch and the original `anevum/anevum-web/games/brandle` main branch.

- **12/12 assets exactly matched** the standalone repository and **12/12 exactly matched** the original monorepo (index, CSS, app, logic, word dictionary, manifest, SVG/PNG graphics, and service worker). There were no mismatches. This is exact *asset-byte* parity, not a guarantee that GitHub's build emits byte-identical whole Worker JavaScript after Wrangler bundling.
- The current Cloudflare deployment remains `86970d97-7975-45e5-a000-0fba9a7379f6` with current version `1c48deb3-6c35-4b9b-9d84-a37d2596ca70`. Three earlier versions were enumerated in job 002. Version presence does **not** prove a tested rollback.
- The standalone main-branch build and tests passed on GitHub run `41117000501`; local git clone could not run because the working container could not resolve github.com. No new local build, live-browser playthrough, GitHub secret-permission check, rollback rehearsal, or deployment cutover was performed.
- **Remaining release gates:** verify scoped deployment credentials and rollback procedure; stage the independent deployer while the monorepo path still owns releases, then retire the old deployer *before* enabling the new one; execute exact-head CI and post-release routes/playback; verify recovery to the known version if needed. Do not modify ANEVUM apex routing or other services.

## Small job 004 — staged Brandle release workflow (2026-10-30)

- Opened [Brandle PR #5](https://github.com/anevum/brandle/pull/5) (`6e88b446b3ec55e51eb673ebc091a4e2acedb80a`). It adds `.github/staged-releases/brandle-production.yml` **outside the active Actions workflow directory** and `docs/DEPLOYMENT_HANDOVER.md`. This is an inactive manual-only release template, not a new deployer.
- The template includes exact-SHA main-ancestry checks, standalone source build/tests, a Worker-name boundary check, environment and owner-switch gates, and a basic post-release HTTP smoke. These checks do **not** prove effective GitHub environment protection or credential scopes; source checks are not sufficient for full release approval.
- At first check, PR #5 exact-head `verify` was **queued**. Review CI before merge. No production, Cloudflare, GitHub secrets, route, D1 or old monorepo deployment ownership changed.
- Cutover still requires scoped credential verification, protected environment confirmation, actual rollback rehearsal, and a second reviewed change that disables legacy deployment before activating the standalone workflow. See the PR handover document.

## Small job 005 — merge inactive Brandle release template (2026-10-30)

- [Brandle PR #5](https://github.com/anevum/brandle/pull/5) exact-head `verify` check passed on `6e88b446b3ec55e51eb673ebc091a4e2acedb80a`. Squash merged to standalone main as `0a08d7038b1ed79d998078a09b4423ffb5b09694`.
- Verified `.github/staged-releases/brandle-production.yml` and `docs/DEPLOYMENT_HANDOVER.md` are present on `main`. The template is outside `.github/workflows` and cannot be dispatched as a workflow; release ownership has not transferred.
- GitHub branch metadata explicitly says `main.protected=false`. The connected integration's generic GitHub fetch cannot read `/environments` (unsupported URL); environment rules and credential scoping remain unverified. Do **not** activate the template or assume environment approvals are enforced.
- The post-merge standalone CI run [`41123827902`](https://github.com/anevum/brandle/actions/runs/41123827902) **passed** at exact merge commit `0a08d7038b1ed79d998078a09b4423ffb5b09694`. Production and legacy deploy workflow unchanged.

## Small job 006 — Brandle CI release-ownership guard (2026-10-30)

- GitHub confirmed `anevum/brandle` main is **unprotected** and its repository ruleset list is empty; the connected GitHub tool cannot inspect or configure environment secrets/approval rules. Administrative controls are not verified.
- Opened [Brandle PR #6](https://github.com/anevum/brandle/pull/6) (`4038b68b886e9be854fdc538ce61e9c7cf6c4e0c`) with `release-guard.test.mjs` and CI integration. It asserts that the only active standalone Actions workflow remains CI, release credentials/deployment commands are absent from CI, and the inactive staged release remains manual-only and requires owner flags, exact-SHA ancestry, and an environment.
- PR #6 exact-head `verify` passed in [run 41124488220](https://github.com/anevum/brandle/actions/runs/41124488220), and was squash merged as `bb1c790daf4d691eaaad3648b21c987fdbae2190`. The guard file was verified present on `main`. Post-merge [run 41124539352](https://github.com/anevum/brandle/actions/runs/41124539352) **passed** on exact merge commit `bb1c790daf4d691eaaad3648b21c987fdbae2190`. No production Worker, domain, legacy workflow, token or deployment settings changed. Do not activate a deployer until branch and environment protections plus rollback are verified.

## Small job 007 — Brandle administrator safeguards (2026-10-30)

- Verified personal public `anevum/brandle` repository has `admin=true`, `main` at `bb1c790daf4d691eaaad3648b21c987fdbae2190` with `protected=false`, no listed rulesets, and only active `ci.yml`. Required check candidate is GitHub Actions `verify` (passed on that commit).
- Created [Brandle issue #7](https://github.com/anevum/brandle/issues/7), an explicit administrative configuration checklist for protected `main`, required checks, protected `brandle-production` environment, scoped Cloudflare credentials, secret presence checks, and safely sequenced single-deployer cutover. For a solo maintainer, required reviewer count should remain zero until a genuine independent reviewer is available.
- GitHub connector has code/content privileges but no branch-rule/environment administration action; no protection or secret change was made. **Do not treat the issue as implementation of those settings.** No live Worker, routing, old deployer, or standalone release activation changed.
- Next job: once admin checks have verifiable evidence, independently review the rollback rehearsal and only then prepare the legacy deployer retirement PR, retaining a non-deploying verification path.

## Small job 008 — Brandle rollback procedure preparation (2026-10-30)

- Opened [Brandle PR #8](https://github.com/anevum/brandle/pull/8) with `docs/ROLLBACK_VERIFICATION.md`, a non-destructive checklist for current-version confirmation, 12-asset hashes, safe HTTP/gameplay smoke, release credential review and an explicitly separate authorized rollback rehearsal.
- A proposed read-only network verification script was blocked by safety checks and **was not committed or tested**. No fresh Cloudflare parity check or rollback rehearsal was performed. Documentation is the only change.
- PR #8 head is `fed02b043571eaa8100ad801ca6062063b2717cb`; CI was queued when first checked. Merge only on passing exact-head verification. The old deployment owner and live Worker remain untouched.

- Job 008 follow-up: PR #8 exact-head `verify` passed; merged documentation-only commit `4bb985fda3f888d80f22cb49f95b7ebbdaebf29d` and verified `docs/ROLLBACK_VERIFICATION.md` on `main`. Post-merge CI was queued at the verification point; do not claim its success without checking. No live rollback occurred.

## Small job 009 — Brandle historical release integrity baseline (2026-10-30)

- Verified PR #8 post-merge GitHub Actions `verify` passed on exact commit `4bb985fda3f888d80f22cb49f95b7ebbdaebf29d` ([run 41125915054](https://github.com/anevum/brandle/actions/runs/41125915054)). `main` still unprotected and rulesets still empty.
- Opened [Brandle PR #9](https://github.com/anevum/brandle/pull/9) at `1187781a5bb3fd97132abe8fc0effd4dcf335362` to preserve 12 SHA-256 values from the *previously* observed live Worker, add a no-network local asset comparison command, add parity/drift/missing-file tests, and wire those tests into CI.
- This is an immutable historical baseline. CI must pass before merge. A fresh Cloudflare inspection call was blocked, so do not claim current live parity, credential inspection, rollback rehearsal or production cutover.
- Exact-head CI passed ([run 41126346886](https://github.com/anevum/brandle/actions/runs/41126346886)); PR #9 squash-merged as `f6743b8aff5cfe21f59db0f0c0a21dd352111fb9`. The historical baseline file was verified on `main`. Post-merge [run 41126407339](https://github.com/anevum/brandle/actions/runs/41126407339) **passed** on merge commit `f6743b8aff5cfe21f59db0f0c0a21dd352111fb9`. No production settings or Worker deployments were changed.

## Small job 010 — draft legacy Brandle deploy retirement (2026-10-30)

- Created **draft, unmerged** [ANEVUM Web PR #799](https://github.com/anevum/anevum-web/pull/799), head `abb59ebe5a4b1ea3851d5ea168e614ff95c3f800`. Proposed change to `.github/workflows/deploy-brandle.yml` keeps the push, pull-request and manual triggers strictly for source syntax, tests and generated Worker build, and removes the live Wrangler deployment step and Cloudflare credential references. Original source and history remain untouched.
- Exact-head `verify` and `verify-only` checks were queued at first observation. This branch does **not** modify `main`; the existing live monorepo deployer still owns Brandle. Keep PR #799 unmerged until Brandle issue #7 (actual administrative protections), scoped environment secrets and a rehearsed rollback are verified, with a sequenced cutover to a single independent deployer.

## Small job 011 — Brandle single-deployer cutover runbook (2026-10-30)

- [ANEVUM Web draft PR #799](https://github.com/anevum/anevum-web/pull/799) exact-head `ANEVUM Verify` and Brandle `verify-only` checks **both passed** at `abb59ebe5a4b1ea3851d5ea168e614ff95c3f800`. Verified its sole change replaces the existing Brandle deployment command/credential access with read-only build checks. The PR **remains draft and unmerged**; monorepo production ownership is unchanged.
- Created and merged [Brandle PR #10](https://github.com/anevum/brandle/pull/10) to publish `docs/SINGLE_DEPLOYER_CUTOVER.md` on standalone `main` at `14afd7e50c447e4ec8d50e51e001ceb37e3d9d11`. PR head `verify` passed; file re-read from main. Post-merge [run 41127558462](https://github.com/anevum/brandle/actions/runs/41127558462) **passed** on merge commit `14afd7e50c447e4ec8d50e51e001ceb37e3d9d11`.
- Runbook defines hard gates: effective branch protection, protected environment, limited credentials, fresh asset parity, independently verified rollback, no competing deployment writers; then legacy deployer retirement, standalone manual workflow activation, first release acceptance and rollback conditions. No live Worker changes or production cutover occurred.
- Outstanding administrator actions remain in [Brandle issue #7](https://github.com/anevum/brandle/issues/7). Do not merge draft PR #799 before satisfying them.

## Small job 012 — Brandicade static recovery build test (2026-10-30)

- Inspected [Brandicade draft PR #1](https://github.com/anevum/brandicade/pull/1): recovered static V1.0.1 game source and tests, but **not** the live cloud-save/Cloudflare Access layer. `LICENSE` says MIT while `build_worker.py` emits a GPLv3 notice. Neither legal provenance nor production parity was established; preserve existing notices.
- On the **existing draft branch only**, added `tests/test_static_build.py` and wired it into `.github/workflows/verify.yml` at head `21b2a19918158ffae87b63a9285b4e496590a0d9`. Offline assertions cover repeat-build determinism, all 14 static routes, absence of deployment credentials/commands, and explicit unresolved license/backend documentation.
- CI status not yet reported for that exact head at checkpoint. **Do not merge PR #1** until tests pass and source/rights/privacy boundaries are reviewed; no production Worker, auth, cloud saves, or default branch was modified.

- Job 012 correction: the first test-file creation did not persist; verified the file on the draft branch after retry. Final PR head is `4fd1313e56dc3ab3ea306e0885fb26e7eaae50b1`, test-file blob `d45a6902f59290b93a8ea41627329d5d80160bfb`. Final file tests deterministic builds and explicit MIT/GPL and cloud-save warnings; it does **not** yet validate the 14-asset route inventory. GitHub reported no check runs for the final head when checked; CI is **unverified**. Keep PR #1 draft and unmerged.

## Small job 013 — Brandicade recovery draft conflict resolution (2026-10-30)

- Latest draft PR #1 head `4fd1313e...` had **no check runs**, and GitHub reported `mergeable_state=dirty`. The previously passing CI applied to the older `27f78cb6...` source, not the added static build tests.
- Confirmed the only conflict stemmed from a newer `main` README which documented missing live cloud-save/Access source and the MIT/GPL notice contradiction. Added equivalent accurate project/ownership boundaries to the draft README and created an explicit two-parent merge commit `0f6dabe74aa203d41c8da4190a689b7cb38429de` incorporating `main` ancestry, then advanced the draft branch with expected-SHA lease. GitHub now reports PR #1 `mergeable=true`, still draft.
- Latest PR head CI [run 41131154047](https://github.com/anevum/brandicade/actions/runs/41131154047) **passed** on merge head `0f6dabe74aa203d41c8da4190a689b7cb38429de`. **Do not merge** without independent server-source, access, and licensing review. No `main`, Worker, live saves, Access or production deployment changed.

## Small job 014 — Brandicade live backend provenance inventory (2026-10-30)

- Cloudflare confirmed Worker `brandicade` with D1 binding `SAVES`, last observed deployment `53bdf783-a472-486f-b06d-53551696018a` (version `09c8dcb9-3db4-47c4-b7be-b9a218a7ba1e`), and three retained versions. Read-only inspection found Access JWT header handling, D1 save operations and API routes `/api/session`, `/api/save`, `/api/backups` in live worker content. Do not mistake these structural signals for a tested authorization boundary.
- No independent editable backend source history was located in the inspected GitHub branch inventory/default-branch code search. Public-source recovery remains incomplete, and MIT/GPL notice discrepancy persists.
- Added `docs/LIVE_BACKEND_RECOVERY.md` to **draft Brandicade PR #1** at `8028a71b70de4969106bc0b788db45f530a886b6` documenting architecture signals and privacy, license, Access, D1, migration, backup and release gates. Re-read the file from the draft branch. No sensitive production code or database rows published, and no deployment occurred. Re-check CI for this new head before merge; PR stays draft.

## Small job 015 — isolated Brandicade Access JWT verifier (2026-10-30)

- Added `server/access-jwt.mjs` to the **existing draft Brandicade PR #1**, as a new standalone RS256 JWT verifier; no code is imported by the production Worker. Strict checks include configured issuer and audience, key ID, cryptographic signature, subject and issued/expiry/time claims. This is a newly reconstructed testable security component, **not verified original deployed backend source**.
- Added synthetic-key tests `tests/access-jwt.test.mjs` and wired into existing `verify` CI. Initial new-test run `41132808368` failed because the fixture mistakenly JSON-encoded a signature instead of raw bytes. Corrected raw-signature fixture encoding at `9418f383f91d518950d66f730c0a4963fc110a8c`; CI run `41132933900` then exposed a second fixture bug (mutating a non-significant last base64url character). Fixed byte-significant signature mutation at `42941af8ec310def51a05fc238d8b621468831ee`. The complete draft PR exact-head CI [run 41133013218](https://github.com/anevum/brandicade/actions/runs/41133013218) **passed**.
- Remaining: verify against Cloudflare's authentic JWKS and Access claim contract, ensure subject isolation and D1 storage logic, independently review license provenance, and only then consider a release candidate. **No production access policy, secrets, D1 records, Worker code or deployment changed.** Draft PR #1 remains unmerged.

## Small job 016 — Brandicade isolated save boundary (2026-10-30)

- Implemented `server/save-boundary.mjs` **only in existing Brandicade draft PR #1**. Its injected `authenticate(token)` returns a verified subject, never accepts ownership from a client save; validates schema/identity fields and 512,000-byte payload limits via the existing save sanitizer; uses revision-based compare-and-swap to reject stale updates; returns detached read snapshots. The included in-memory repository is explicitly a synthetic **test adapter only**, not production D1 persistence.
- Added `tests/save-boundary.test.mjs` covering separate Alice/Bob saves, unauthorized access, forged identity fields, stale revision conflicts, malformed/oversize saves and detached reads; integrated it into CI. PR head `89434e1f7da725e20f87d556d8712b78f32647f3` passed [GitHub Actions run 41133336174](https://github.com/anevum/brandicade/actions/runs/41133336174).
- No D1 migration, API routes, live authentication integration, production database, tokens, Worker or deployment changed. Database adapter must enforce per-subject atomic compare-and-swap, Access JWKS must be verified independently, and license discrepancy remains. Keep the PR draft and unmerged.

## Small job 017 — isolated Brandicade D1 adapter and synthetic SQLite verification (2026-10-30)

- Added `server/d1-save-adapter.mjs` to existing **draft** Brandicade PR #1, implementing owner-keyed parameterized reads and atomic INSERT-on-conflict / conditional UPDATE with `RETURNING revision`, preserving optimistic concurrency. Added an explicitly non-production candidate schema in `server/schema/proposed-saves-v1.sql`.
- Added `tests/d1-save-adapter.test.mjs` with a mock D1 statement interface for separate accounts, stale revisions and invalid inputs, plus `tests/test_proposed_d1_schema.py` exercising the candidate schema and conflict SQL against an in-memory SQLite database. CI now runs both Node and Python tests.
- Exact PR head `3794f50f92f4ff7cddf34dbba58b13d7c20cd526` passed [GitHub Actions run 41134033413](https://github.com/anevum/brandicade/actions/runs/41134033413). This confirms tests of the **synthetic mock and candidate SQLite schema**, not a real Cloudflare D1 runtime or production migration.
- No authentication route wiring, existing live D1 query, database migration, secret, Cloudflare Worker or deployment change occurred. License discrepancy and original database lineage remain unresolved. Keep Brandicade PR #1 draft and unmerged.
