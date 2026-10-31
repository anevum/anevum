# GitHub portfolio closeout audit — full accessible account

Audit time: October 30, 2026 (America/New_York); some GitHub/Cloudflare records are dated October 31 UTC.
Session: `ANEVUM.OPS.PACKAGE.2026-10-30.002.COMPLETE-GITHUB-RESTRUCTURE`, Small Job 040.

**Verdict: NOT COMPLETE.** This is a read-only evidence inventory plus a closeout plan. It does not certify full Git history, actual signed-in acceptance, permissions not exposed by the installed GitHub connector, credential scope, or every runtime dependency. All twelve repositories visible in the authenticated GitHub connection belong to `anevum` and are public. No other repositories were listed by that installation.

## Reverified current totals

| Metric | Result | Basis |
| --- | ---: | --- |
| Accessible repositories | 12 | All-repository and owner-filtered GitHub listing |
| Open PRs | 315 | Global and 12 repo-specific GitHub search counts |
| Draft / non-draft open PRs | 299 / 16 | Paginated open PR collections |
| Open issues | 79 | Global and per-repo search collections |
| Branches | 1,466 | Complete page-by-page GitHub branches collections (100/page) |
| Protected default branches | 0 / 12 | Each `main` branch API |
| Active GitHub rulesets | 0 / 12 | Each repo rulesets collection |
| Main branches containing only a README | 4 | Root directory listings |
| Repositories with no topics | 12 / 12 | Each repo metadata |
| Repositories with no description | 9 / 12 | Each repo metadata |
| GitHub Releases observed | 0 / 12 | GitHub releases collections; tags not audited |
| GitHub workflow files on `main` | 46 | Seven repositories: 35 + 3 + 4 + 1 + 1 + 1 + 1 |
| Connected Cloudflare Worker scripts | 121 | Cloudflare account scripts listing |
| ANEVUM zone Worker routes | 45 | Cloudflare zone route list |
| Enabled custom Worker domains | 13 | Cloudflare Worker domains |

The baseline counts in `CLOSEOUT_BACKLOG_2026-10-30.md` remain a historical snapshot. This audit supersedes those counts for today's state, not earlier observations.

## Current repository coverage

| Repo | Branches | Open PRs | Issues | Current `main` and closeout requirement |
| --- | ---: | ---: | ---: | --- |
| [anevum](https://github.com/anevum/anevum) | 28 | 0 | 0 | Profile, registry and handoffs; retain authoritative index and reconcile public positioning. |
| [anevum-web](https://github.com/anevum/anevum-web) | 851 | 281 | 62 | Main source/CI exist; 35 workflows; Brandle/CristyBreathe still under `games/` and `apps/`; overlapping production routes, old and new product scopes, extensive PR/branch history. |
| [rhen](https://github.com/anevum/rhen) | 538 | 25 | 12 | Main source, Apache-2.0, tests and 3 successful checks; independently verify actual Railway service, source SHA and risk/backup boundaries. |
| [family-adventure-book](https://github.com/anevum/family-adventure-book) | 14 | 4 | 3 | Source and existing Cloudflare Worker; draft security PR #14 and gate/ruleset PR #15 remain held. GitHub `source-smoke` green; a historical Cloudflare check attached to main SHA failed a **preview branch** for missing Wrangler `previews` config—not evidence the live Worker is down. |
| [devonakins.com](https://github.com/anevum/devonakins.com) | 10 | 1 | 0 | Main source, MIT, green CI, live Cloudflare custom domains; visual PR #4 open, release provenance/rollback and updated content positioning still need review. |
| [brandle](https://github.com/anevum/brandle) | 11 | 0 | 1 | Main source, Apache-2.0 and green CI; independently deployed game still has a legacy `anevum-web` production writer. Complete owner handover with rollback, preserving browser-origin saves. |
| [cristybreathe](https://github.com/anevum/cristybreathe) | 4 | 1 | 0 | Main source and green CI; calendar draft #2 and monorepo counterpart #796 held pending private Access/D1 backup, permission and migration verification. |
| [brandicade](https://github.com/anevum/brandicade) | 2 | 1 | 1 | README only on main. Draft #1 contains static source and verified direct links; live Access/D1 save backend absent, MIT/GPLv3 provenance conflict; no safe deployment candidate. [Issue #2](https://github.com/anevum/brandicade/issues/2). |
| [devon-station](https://github.com/anevum/devon-station) | 2 | 1 | 0 | README only on main; draft #1 imports partial server components and synthetic tests, not complete UI/assets/runtime. Source archive's `UNLICENSED` notice and private-data exclusions require review. |
| [ideaflow](https://github.com/anevum/ideaflow) | 2 | 1 | 0 | README only on main; draft #1 contains verified analyzer fragment/tests, not the current intake, meeting and operations service sources. Keep explicit manual analysis policy and necessary automated privacy/retention controls. |
| [severance](https://github.com/anevum/severance) | 3 | 0 | 0 | Two separately licensed, green-CI experiments: Godot prototype and Python world-state lab; original history remains in ANEVUM Web, neither component is a complete multiplayer game. Root licensing/packaging clarity is pending, but future game completion is outside portfolio closeout. |
| [cristyrusso.com](https://github.com/anevum/cristyrusso.com) | 1 | 0 | 0 | README-only *intentional future website*. Keep planned status; publishing approved content, domain transfer and design implementation are separate work, not a reason to invent placeholder source. |

## Important findings that were not resolved by earlier documentation

### 1. The "restored app" problem is real

Brandicade, DevonStation and IdeaFlow have running Cloudflare Workers but their new standalone default branches do **not** contain recoverable, complete authoritative sources. A passed test on a partial draft does not change this. The Brandicade Worker contains public HTML cards for Brandle on home and Games, but they first show a modal before opening the separate Brandle game. Draft #1 changes them to direct links, but is NOT deployed. The live code includes Access, `/api/session`, `/api/save`, `/api/backups` and legacy D1 save-history handling omitted from the static archive. Never merge or deploy it over the live Worker without exact server parity, license review, backup and rollback.

### 2. Multiple domains and release writers matter

The `brandicade` Worker is exposed through `brandicade.devonakins.com` and `brandicade.anevum.com` custom domains, plus its Worker subdomain. Anonymous access to each received Cloudflare Access sign-in. Because browser `localStorage` is origin-scoped, switching between those addresses can create separate local-only progress even if they serve the same Worker; no actual user save loss was demonstrated. Choose a canonical user-facing origin only after backup, redirect and Access review.

`anevum-web/.github/workflows/deploy-brandle.yml` still deploys on selected `main` source pushes and manual dispatch; the independent `brandle` repository's CI is intentionally verification-only. The held [ANEVUM Web PR #799](https://github.com/anevum/anevum-web/pull/799) must retire the old writer as part of a guarded single-owner handoff, not before.

Cloudflare has 121 scripts and 45 ANEVUM-zone routes with many overlapping patterns (including `anevum.com/*` plus exact routes). Neither 121-40 nor any naming convention measures safe-to-delete scripts. Identify current route ownership, sensitive/private endpoints, dependencies, other-zone and `workers.dev` traffic before change.

### 3. Governance is not in effect

All twelve `main` refs report `protected: false`; all twelve ruleset listings are empty. GitHub reports administrator permission for the account, but the installed GitHub application lacks its separate Administration API permission and cannot activate rulesets (403 observed during prior work). [Family Adventure Book draft PR #15](https://github.com/anevum/family-adventure-book/pull/15) holds an **importable initial** main ruleset and 37 passing synthetic release/rule tests; these are *not enforced* by GitHub or the current Cloudflare production build. Avoid requiring a workflow before it exists on `main`.

No repository has Dependabot configuration, CODEOWNERS, or issue templates under the inspected `.github` roots. These can be added selectively after base controls, but a solo maintainer should not be trapped by unavailable reviewer requirements.

### 4. CI and release provenance are incomplete

`anevum-web` has 35 workflow files, including archived V5/V131 tools, manual D1 migrations, comment-triggered staging writers, the active legacy Brandle writer and CI that performs preview builds. The retired `deploy-production.yml` deliberately fails closed, but older workflows and the Cloudflare route graph still require owner-by-owner verification before retirement. Some PRs have failed checks even when their general `verify` check passed: e.g. [PR #763](https://github.com/anevum/anevum-web/pull/763) had a preview timeout and packaging assertion failure on its observed head. [PR #793](https://github.com/anevum/anevum-web/pull/793) also has failed checks. These are **PR-check failures, not proof that the current live application is broken**.

No GitHub Releases were listed in any repo. Production versions live in Cloudflare/Railway and source documentation; tags were not audited. Establish per-app source SHA, one production writer, pinned tools, workflow/checks, build artifact identity, environment scope, encrypted backups, actual restoration and rollback evidence. Inspect real CI/Cloudflare build identity before declaring an app released.

### 5. Rights, safety and continuity

Historical targeted credential scans are useful but not an exhaustive review of all Git refs, binaries, deleted files, third-party assets or private records. Full rights and secrets checks remain essential for open-source publication, especially RHEN/ANEVUM Web, DevonStation and the MIT/GPLv3 Brandicade conflict. Never print tokens or patient/client content or commit private saved data to a public repository.

The public `anevum-web` README still presents RHEN as a flagship studio product and earlier studio positioning, while the current operating direction prioritizes ANEVUM as a family creative studio separate from Cristy's businesses. `devonakins.com` README still describes mathematical "instruments" the owner wants removed from the personal site; visual/content work is pending review in [PR #4](https://github.com/anevum/devonakins.com/pull/4). Fix public descriptions based on actual accepted code and approved positioning, not by claiming unreleased changes are already live.

All 12 repositories lack GitHub topics; nine have no description, and ten have no homepage configured (not every repository needs a homepage). The 79 open issues have no issue labels in the retrieved results; meaningful workflow classification has not been applied. This affects portfolio navigation and the ability to distinguish locked decisions, active work, backlog and obsolete records.

## Completion gates: required, independent evidence

- **C1 / Authoritative source:** Every running app has one owning repo containing independently buildable public-safe code with full backend entrypoints, deterministic instructions, license/notice rights and retained original source lineage; planned repos explicitly say "planned".
- **C2 / Security and governance:** All active code repos have applicable enforced branch rules, required project checks, no accidental bypass/force pushes, credentials/PII/PHI history audit and independent privacy boundaries; do not equate test plans with enforcement.
- **C3 / Data recovery:** Every stateful deployment has reviewed DB migrations, retention and access policy, encrypted backup plus actual restore rehearsal, and no unsafe account-ID or storage-origin change.
- **C4 / Production release:** Each live Worker/Railway service has exactly one documented release owner, code commit, artifact/version, deployment environment, toolchain, source-to-live mapping, smoke test, negative-path guard and proved rollback. Only then retire duplicate writers.
- **C5 / Historical backlog:** Classify all **315** open PRs (**299** draft / **16** non-draft), **1,466** branches and **79** open issues by active, locked, backlog, superseded, archive or duplicate with evidence. Do not bulk close, merge or delete anything based on age or title alone. Review non-draft PRs and security-sensitive changes first.
- **C6 / Public portfolio:** Accurate README/project status, links, description, topics, homepage where relevant, notices, root distribution boundaries, changelog/release manifest, source and owner references; final cross-repo CI and real-device acceptance for affected live apps.

**Completion definition:** C1-C6 pass for the *infrastructure and source organization* scope. It does not require implementing the unfinished SEVERANCE world, every ANEVUM feature, all CristyBreathe improvements or an unapproved redesign for Cristy. Historical work may be formally archived rather than implemented. The repository and Notion tracker must clearly indicate what is locked, active, backlog or obsolete.

## Small-job implementation order

| Order | Independently verifiable next work | Stop condition / acceptance |
| ---: | --- | --- |
| 1 | Restore public-safe Brandicade server layer and identity/save history | Exact Access/D1 route compatibility, rights review, no player rows exported |
| 2 | Verify Brandicade backup and safe Brandle direct release | Actual authorized device behavior, origin preservation, tested rollback |
| 3 | Restore full DevonStation UI, modules and source lineage | Fresh checkout and tests; private snapshots excluded; license rights resolved |
| 4 | Restore four current IdeaFlow services | Manual analysis, retention and storage protections, no private recordings in Git |
| 5 | Verify CristyBreathe Access, D1 backup/restore and calendar candidates | Two-account permissions and staged migrations before any release |
| 6 | Reconcile ANEVUM apex 45 routes / 121 scripts and current service ownership | No route/data interruption; record live routing and true owners |
| 7 | Reconcile RHEN Railway deployment, broker authority and rollback | No trading/order changes; prove current runtime SHA and safe boundary |
| 8 | Activate administrator-enforced `main` rulesets/required CI | GitHub readback proves effective protection on active repos |
| 9 | Complete repository-wide secrets/history/asset/license review | Remediation and exceptions documented, no private materials exposed |
| 10 | Secure Brandle single-deployer handoff and remaining Worker build paths | Exactly one writer; no loss of local progress |
| 11 | Audit/retire 35 ANEVUM Web workflows and fix failing preview/package checks | Verify every deletion/disable has no live dependent route |
| 12 | Triage 16 non-draft PRs, then 299 draft PRs and all branches/issues in batches | Preserve unique unmerged commits; tag decision/evidence |
| 13 | Finish accurate GitHub profile, repo metadata, security docs and release manifests | URLs and scope facts correct; no false "complete/deployed" claims |
| 14 | Final full source CI, access/device, release/rollback and Notion reconciliation | Every C1-C6 gate marked proven with current evidence |

This is sequencing, **not** an estimate of 14 trivial tasks or a guarantee that 14 commits will close all blockers. Each row may require several small, verified jobs and explicit owner decisions.

## What was verified vs. not verified in this audit

**Verified:** All 12 accessible public repos, roots/metadata/default branches, issue and PR counts, all branch pages, workflow directory inventory, actual main check-run summaries, representative high-risk PR check runs/logs, GitHub ruleset collections, GitHub Releases listings, selected READMEs/previous audits, Cloudflare script/domain/route collections and critical Worker deployment metadata.

**Not verified:** Every file/blob/history revision, every workflow run ever, old branch unique diffs/merge ancestry, actual GitHub environment settings/secret scopes and collaborator access, RHEN's live Railway service, signed-in Brandi/Cristy/device acceptance, Cloudflare D1 data integrity/backups, DNS outside observed zones, exact runtime service dependency graph, private artifacts, actual production rollback, or hidden/uninstalled repositories. These must remain explicit checklist items, not inferred successes.

Do not close this audit until the evidence for C1-C6 is linked and checked.
