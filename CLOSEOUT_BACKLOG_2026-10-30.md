# GitHub portfolio reorganization — completion audit and execution backlog

Date: 2026-10-30 (read-only inventory checkpoint).
Session: `ANEVUM.OPS.PACKAGE.2026-10-30.002.COMPLETE-GITHUB-RESTRUCTURE`.

**Verdict: NOT COMPLETE.** The twelve public repositories exist, but source ownership, effective branch controls, release ownership, source/rights provenance and the large historical backlog are not resolved. This is an evidence-grounded inventory, not authorization to alter live resources.

## Scope reset: current-portfolio-first closeout (October 30, 2026 local; Small Job 044)

**Decision:** The current personal/business and family-creative portfolio, not historical branch count, defines operational closeout. This section **supersedes the old requirement to manually classify all 315 open PRs and 1,466 branches before declaring the current operating portfolio organized**. The full inventory remains useful historical evidence; old Git history is not erased and must not be bulk-deleted. The old C1-C6 audit is a record of its original, broader scope, not a command to complete every obsolete prototype.

Only maintain a project if it (a) supports current authorized business/operations, (b) serves a real personal/family need, or (c) is intentionally preserved creative/IP source. Otherwise freeze development and assess reversible retirement.

| Repository | Disposition | Narrow operating obligation |
| --- | --- | --- |
| [anevum](https://github.com/anevum/anevum) | **ACTIVE** | Public profile, project index and source-of-truth registry |
| [anevum-web](https://github.com/anevum/anevum-web) | **ACTIVE / RESTRICT** | Maintain real website/routes and required releases; stop broad speculative platform work |
| [cristybreathe](https://github.com/anevum/cristybreathe) | **ACTIVE** | Current private business workspace; preserve Access and data boundaries |
| [ideaflow](https://github.com/anevum/ideaflow) | **ACTIVE / MAINTENANCE** | Current manual processing and automatic retention safeguards; recover deployable source only as needed |
| [devon-station](https://github.com/anevum/devon-station) | **ACTIVE / MAINTENANCE** | Current personal operating workspace; recover verified runtime source |
| [devonakins.com](https://github.com/anevum/devonakins.com) | **ACTIVE** | Accurate professional portfolio |
| [brandle](https://github.com/anevum/brandle) | **ACTIVE / FAMILY** | Retain independent original-origin game and player progress |
| [brandicade](https://github.com/anevum/brandicade) | **ACTIVE / FAMILY** | Preserve actual live Access/save system; no unsafe draft cutover |
| [cristyrusso.com](https://github.com/anevum/cristyrusso.com) | **PLANNED** | Separate approved website work; README-only is acceptable; no invented implementation |
| [rhen](https://github.com/anevum/rhen) | **PARKED / VERIFY LIVE OWNER** | No new research development; verify Railway/broker dependency before retirement |
| [severance](https://github.com/anevum/severance) | **PARKED / CREATIVE** | Preserve real experiments as optional family creative source; no forced game release |
| [family-adventure-book](https://github.com/anevum/family-adventure-book) | **RETIREMENT CANDIDATE** | No further feature/release-gate work; Worker and history preserved pending safe decommission |

### Completion gates for the current operating portfolio

1. **Current apps only:** Every actively used app has an identified owning repository, recoverable public-safe source (or documented legitimate private-source exception), reproducible verification, and honest public source/deployment status. A planned site does **not** require an invented implementation.
2. **Live safety:** Each production service has a documented real release owner, actual data/Access boundary, tested backup/restore where stateful, one safe deployer, and verified rollback. Avoid disruptive source cutovers to satisfy cosmetic repository goals.
3. **Governance:** Enforce applicable GitHub branch protections and checks on active code; review historical secrets/rights exposures relevant to published source. Do not count locally passing tests or draft rule configurations as live enforcement.
4. **Retirement safely completed:** For an obsolete deployed service, confirm real usage, connected routes/domains/Workers, storage and browser-local data, live release triggers and rollback. Freeze first; then disable/decommission only with clear owner acceptance. Archive source/history rather than delete first.
5. **Accurate portfolio:** Update registry, status/owner links and the existing private Notion tracker; distinguish ACTIVE, PLANNED, PARKED and RETIREMENT CANDIDATE. No new duplicate tracking system.

**Not required for this operational closeout:** Building unused prototypes, achieving a polished release for every lab, finishing RHEN or SEVERANCE, deploying the future Cristy website early, reviewing every old draft PR/branch, or deleting all unreferenced Workers. Historical backlog triage remains optional, prioritized by security/release impact and unique source value.

### Immediate retirement boundary (no resource deletion authorized by this note)

- `family-adventure-book` is a retirement candidate, not an actively funded release workstream. The existing Worker and four draft PR branches exist; do **not** merge draft release-gate/security work merely to retire it. Verify household use, local/browser progress preservation and any live URL before taking it offline.
- Cloudflare currently has an enabled custom domain `lab.anevum.com` for `anevum-private-lab`, with additional lab route mappings. A name containing `lab`, `family`, `staging` or `test` does **not** establish inactivity. In particular `family-idea-*` belongs to current IdeaFlow; preserve it.
- `rhen` is parked for feature work, not certified safe to delete or stop. Its broker/Railway runtime relationship remains unresolved.
- Continue Brandle/Brandicade, personal and Cristy operational source recovery only to the point needed for stable ownership, recoverability and actual use.

### Next narrow sequence

1. Freeze new feature and release-gate expansion for parked/retirement candidates; preserve existing deployments during mapping.
2. Verify live user-facing production routes and active owner/source for the **ACTIVE** rows; prioritize existing business and personal systems.
3. Fix active-code branch rules, access, backup and release-owner gaps.
4. Review obsolete family-adventure and mapped lab resources in one explicit retirement batch; preserve original source and rollback before service removal.
5. Verify exact production smoke/data recovery, public portfolio claims and the existing Notion dispositions. Close operational infrastructure scope; archive historical work separately.

**Owner decision still needed before irreversible deletion:** Which working domains, saved family progress and historical creative artifacts may be permanently removed. This section records a reprioritization, not a decommission approval. Public documentation deliberately excludes internal financial, clinical and family plans.

---

## Verified account totals

| Metric | Observed |
|---|---:|
| Public GitHub repositories | 12 |
| Open GitHub PRs | 311 |
| Open GitHub issues | 77 |
| All repository branches combined | 1,435 |
| Main branches marked `protected` | 0 / 12 |
| Repository rulesets returned by GitHub | 0 / 12 |
| Repositories with no topics | 12 / 12 |
| Repositories lacking description | 9 / 12 |
| README-only default branches | 4 / 12 |
| ANEVUM Web open PRs | 281 (268 draft, 13 non-draft) |
| ANEVUM Web open issues | 62 |
| ANEVUM Web branches / workflow files | 851 / 35 |
| RHEN open PRs / issues / branches | 25 / 12 / 538 |
| Cloudflare Worker scripts | 121 |
| Worker routes on ANEVUM zone / enabled custom Worker domains | 45 / 13 |

Among Cloudflare scripts, 40 distinct names are referenced by these routes/domains and 81 have no reference in those *particular maps*. The 81 are **not proved unused**; they can still serve `workers.dev` or routes in other zones. No scripts, routes, domains or applications were deleted.

## Repository-by-repository completion status

| Repository | Verified main / outstanding | Priority |
|---|---|---|
| [`anevum`](https://github.com/anevum/anevum) | Public profile, registry and handoffs; refresh status and completion evidence after each package | P2 |
| [`anevum-web`](https://github.com/anevum/anevum-web) | Integrated source and passing latest main verification; 281 open PRs, 851 branches, 35 workflows; still contains `apps/cristybreathe` and `games/brandle`, production route ownership is distributed | P0 |
| [`rhen`](https://github.com/anevum/rhen) | Standalone source, tests, license and passing main CI; 25 open PRs and 538 branches; documented Railway runtime ownership needs verification | P1 |
| [`devonakins.com`](https://github.com/anevum/devonakins.com) | Standalone website source and green main CI, Cloudflare custom-domain Worker; visual PR #4 is open; deployment provenance and rollback not certified | P1 |
| [`family-adventure-book`](https://github.com/anevum/family-adventure-book) | Prototype source and green CI; two draft PRs; Cloudflare Worker deployment exists although README still says no deployment | P2 |
| [`brandle`](https://github.com/anevum/brandle) | Complete static source, CI green and historic live-asset parity; original ANEVUM Web deployer still active; standalone deploy template inactive; administrative gate in issue #7 | P1 |
| [`cristybreathe`](https://github.com/anevum/cristybreathe) | Standalone code/tests and main CI green; calendar PR #2 draft; D1 backup/restore, Access/authorization and release-owner handover need verification | P0 |
| [`severance`](https://github.com/anevum/severance) | Godot prototype and independent Python world-state lab, passing CI; both subprojects licensed, root has no consolidated license; original branch history in ANEVUM Web PR #788 | P2 |
| [`brandicade`](https://github.com/anevum/brandicade) | Main is README-only; draft PR #1 contains recovered static source, new synthetic Access/D1 tests with passing CI; actual live backend, fixed-player identity, backup history and conflicting MIT/GPLv3 notices block merge/cutover | P0 |
| [`devon-station`](https://github.com/anevum/devon-station) | Main README-only; live Worker with Access, D1 and notifications; source archive has private snapshots and requires public-safe reconstruction and tests | P0 |
| [`ideaflow`](https://github.com/anevum/ideaflow) | Main README-only; four live intake/meeting/analyzer/operations Workers with D1/R2/queue dependencies; current-source reconciliation and private-data safeguards needed | P0 |
| [`cristyrusso.com`](https://github.com/anevum/cristyrusso.com) | Planned website/repository, README-only; actual public content, professional claims, rights and domain move need Cristy's approval; do not publish placeholder | P2 |

Do **not** conflate application-feature completion with GitHub organization. A correctly scoped *planned* site or *prototype* may remain unpublished and still be organized. Existing live services, however, need a corresponding recoverable public-safe source or explicitly documented private-source exception.

## Hard completion gates

**G1 — Correct owning repository and source lineage.** Every live app must have one authoritative development repository, reproducible build, deployment version history and documented attribution. Preserve original monorepo commits; do not flatten or delete historical code to create a cosmetic clean tree.

**G2 — Sensitive source and rights review.** Run a full working-tree *and Git-history* secret/PHI/PII/license scan. Verify third-party images, fonts, assets, code and notices. The root `.env.production` on ANEVUM Web currently contains a single feature-flag assignment, not an exposed token in the inspected snapshot; this is not a history-wide clean bill. Resolve Brandicade's MIT/GPLv3 notice conflict without suppressing attribution.

**G3 — Enforced governance.** Add and verify protected `main` rules with required green project CI, PR-only protected changes, no force push/deletion, and reasonable solo-maintainer review policy. GitHub currently reports 0 protected mains and 0 rulesets; the connected GitHub App cannot administer these settings. Configure through approved administrator workflow and verify actual enforcement.

**G4 — Release provenance and recovery.** For every deployed app record: source SHA, workflow/owner, Worker or Railway service, custom route, data bindings, secure credentials, backup/restore proof, rollback rehearsal, minimal device/browser smoke. Never switch deployment owner until there is no competing writer.

**G5 — Historical intake and triage.** Classify 311 PRs and 1,435 branches by active work, unique unmerged changes, superseded, production owner or archive. Do not bulk merge/close/delete on age or duplicate title alone. Especially preserve ANEVUM Web Creator Studio and SEVERANCE branch history and RHEN research audit trails.

**G6 — Portfolio quality and final acceptance.** Correct README claims, project status, root license/NOTICE where appropriate, security disclosure, build/test instructions, project description/topics/homepage, production status, archive links, source ownership registry and release verification. Confirm all internal links, all current CI checks, privacy boundaries and deployment ownership.

## Prioritized small-job queues

### P0 — unblock source and security first

1. Verify and configure protected branches and environment protections; [Brandle admin issue #7](https://github.com/anevum/brandle/issues/7) is a concrete example of this GitHub administrator-only gate.
2. Run secrets/history and rights scan across source-bearing repos and migration branches, triage leaks privately; never publish secrets or actual private client data.
3. Recover and sanitize authoritative DevonStation code from original archive plus live Worker; establish tests, D1 lineage, Access and backup/rollback before importing to public main.
4. Recover and reconcile IdeaFlow's four current Worker sources and past archives; preserve manual-on-request analysis policy and separate automatic retention/privacy protections.
5. Finish Brandicade source provenance, reconcile backend Access verification and existing live `saves` / `save_history` schemas and fixed legacy player mapping; do not deploy or merge [draft PR #1](https://github.com/anevum/brandicade/pull/1) until verified.
6. Inspect CristyBreathe production Access and D1 backup/restore before releasing [calendar PR #2](https://github.com/anevum/cristybreathe/pull/2), and separately validate its original ANEVUM Web [PR #796](https://github.com/anevum/anevum-web/pull/796).
7. Establish actual ANEVUM apex source and route owner map across overlapping Worker routes; preserve Command/member access and rollback before changing any live release mechanism.

### P1 — controlled release ownership and CI

8. Complete Brandle scoped token/environment/rollback rehearsal, then retire old deployer via held [ANEVUM Web draft PR #799](https://github.com/anevum/anevum-web/pull/799) **before** enabling standalone manual release; test first release and confirm one writer.
9. Reconcile CristyBreathe, Brandicade, DevonStation and IdeaFlow standalone release owners **individually** after source gates pass; D1/R2 data and authentication must remain private.
10. Verify DevonAkins.com Worker release lineage/rollback and review [website PR #4](https://github.com/anevum/devonakins.com/pull/4) against current site and tests; do not automatically merge visual work.
11. Verify family-adventure-book Worker origin, intended demo/route and rollback; fix README's unsupported claim that nothing has deployed. No private family content.
12. Map actual RHEN operational host: connected Railway shows five projects, two empty RHEN-named projects and other lab services. This does **not** prove RHEN is offline; reconcile against the operational deployment and GitHub source before any service change.
13. Fix ANEVUM Web application-preview verification, which has failed when Wrangler emits `preview.urls: []`. A previous docs-only CI scope fix did not resolve real application-preview failures. Avoid opening private routes to solve CI superficially.
14. Audit 35 ANEVUM Web workflows for current necessity, secrets, production write permissions, branch triggers and fail-closed retirement; disable only after release-owner proof.

### P2 — archive/portfolio closeout

15. Classify 281 ANEVUM Web PRs (268 drafts) and 851 branches in stable, independently reviewable batches, preserving unique unmerged work. Review the 13 non-draft PRs separately.
16. Classify 25 RHEN PRs (23 drafts) and 538 branches, retaining research lineage and safe broker boundaries. Review any GitHub branch protection and secrets before archival.
17. Triage the remaining five non-Web/non-RHEN PRs and 77 open issues across all repos; leave genuine active work open with owners and accurate status.
18. Reconcile ANEVUM Web product boundaries by locating isolated Brandle/CristyBreathe implementations and making legacy paths non-deploying after standalone cutover. Keep historical Git commits.
19. Update public portfolio descriptions (missing 9 of 12), topics (missing all 12), homepage links where relevant; bring README positioning into line with ANEVUM's family creative studio and separate Cristy/business projects.
20. Confirm source/release/CI/link/license/security status of every repo, update the public project registry and handoffs with verified commit IDs and close out only passed gates.

## Not included in this reorganization completion definition

- Finishing SEVERANCE's game design or building an entire multiplayer game.
- Implementing every feature requested for DevonStation, IdeaFlow, or CristyBreathe beyond the source/release/backup boundaries.
- Publishing an unapproved replacement for cristyrusso.com or migrating its domain.
- Turning on broker order execution, payments, or any production data migration.
- Deleting old Workers, Railway projects, backups, branches or source history without classification and safe recovery.

## Current stop conditions

- **Never** treat a passing unit test as proof a source snapshot matches all running backend logic.
- **Never** commit live saves, private workspace data, clinical records, JWTs, API tokens, customer information or unsanitized Worker bundles to a public repository.
- **Never** authorize a production cutover from a document, an inactive workflow template, or an old version existing in Cloudflare; require actual release owner, current version, rollback and acceptance evidence.
- **Do not** merge the Brandicade recovery draft while the original backend/license/schema are unresolved.
- **Do not** merge Brandle monorepo retirement PR #799 before protected environment, scoped secrets, rollback, and a safe handover are verified.

**Next recommended job:** stop expanding Brandicade prototype code for the moment. Prioritize a public-safe source recovery of DevonStation or IdeaFlow, and separately complete GitHub administrator governance. Track each as one small, verified checkpoint instead of creating further planning-only PRs.


## Small job 039 — refreshed recovery readiness (October 30, 2026 local / October 31 UTC)

This checkpoint **does not change the October 30 baseline counts above**; those remain the initial inventory. A fresh public GitHub search returned **315 open PRs and 79 open issues** (one new Brandicade integration issue was created in this job). All **12** public repositories were rechecked; every current `main` reports **`protected: false`**. Four `main` branches still contain a README only: **Brandicade, DevonStation, IdeaFlow and cristyrusso.com**. The historical 1,435-branch count has not been recalculated in this checkpoint.

**Brandicade/Brandle discrepancy and action:** Read-only inspection of the currently deployed Brandicade Worker found two Brandle cards in its embedded HTML, but the old click path first shows a modal and then links to the independently deployed game. [Brandle](https://brandle-glimmer-grove.devonakins.workers.dev/) loaded in an anonymous browser with its 6x5 word grid and keyboard; the Brandicade app is protected by Cloudflare Access, so Brandi's post-authenticated user experience has **not** been tested. The current independent Brandle Worker serves `X-Frame-Options: DENY`, ruling out an iframe shortcut.

[Brandicade draft recovery PR #1](https://github.com/anevum/brandicade/pull/1) now contains two direct, accessible one-tap Brandle links to the **original** Brandle origin, four new tests, a CI job update, and [Brandle restoration notes](https://github.com/anevum/brandicade/blob/recovery/static-v101-20261030/docs/BRANDLE_RESTORATION.md). Exact-head GitHub verification passed at `650a64fd66086a88a5fbc7fb382153b50f2e2f68` after a test-only name-shadow correction; no application or security backend was deployed. [Brandicade issue #2](https://github.com/anevum/brandicade/issues/2) now owns first-class game integration, consentful origin/save migration, full live server-source restoration, licensing and device acceptance.

**Hard Brandicade hold:** The draft static source is still incomplete. Its bundled build does not include the running Worker's `/api/session`, `/api/save`, `/api/backups`, Cloudflare Access and D1 `saves`/`save_history` behavior. The proposed save adapter uses a different schema/identity strategy and cannot replace the legacy `brandi` record without an approved migration and verified rollback. MIT/GPLv3 provenance is unresolved. Do **not** merge the draft into production or claim the new link is live. Existing player data was not accessed or changed.

**Other P0 source gaps remain:** [DevonStation draft PR #1](https://github.com/anevum/devon-station/pull/1) is a partial backend recovery, not a complete UI/runtime; [IdeaFlow draft PR #1](https://github.com/anevum/ideaflow/pull/1) is the inspected analyzer only, not all four services. Cristy's new website repository remains intentionally not yet implemented/published. Verify existing apps and recover public-safe source without private records before any release-owner migration.

**Next safe execution order:** 1) Recover/preserve live backend and backups for Brandicade and the independently deployed personal/business workspaces, 2) finish permissions/right-to-publish scans, 3) apply GitHub administrator branch controls, 4) prove a single deployment owner and rollback for each app, 5) run authenticated device acceptance for the Brandicade launcher and other affected live apps, 6) classify historical PRs/branches carefully, 7) close registry and metadata hygiene gaps. Keep each job separately verifiable; no bulk closure, deletion, private-record exports, silent origin changes or production replacement.

Notion's existing **Devon Station — Project Portfolio** received separate Brandicade (blocked) and Brandle (active) records with their correct repository, hosting and source-of-truth links.
