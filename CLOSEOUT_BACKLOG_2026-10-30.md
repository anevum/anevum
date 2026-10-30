# GitHub portfolio reorganization — completion audit and execution backlog

Date: 2026-10-30 (read-only inventory checkpoint).
Session: `ANEVUM.OPS.PACKAGE.2026-10-30.002.COMPLETE-GITHUB-RESTRUCTURE`.

**Verdict: NOT COMPLETE.** The twelve public repositories exist, but source ownership, effective branch controls, release ownership, source/rights provenance and the large historical backlog are not resolved. This is an evidence-grounded inventory, not authorization to alter live resources.

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
