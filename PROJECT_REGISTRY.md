# Public project registry

Session: `ANEVUM.OPS.PACKAGE.2026-10-30.002.COMPLETE-GITHUB-RESTRUCTURE`  
Snapshot: October 30, 2026. This registry describes public source status, not deployment readiness. [See the evidence-based completion audit](./AUDIT_2026-10-30.md): repository reorganization is **not complete**. Verify the current project and release documentation before making changes. Private operations and recovery information belong in private records.

Operational focus follows **currently used personal/business applications and family creative work**, not completion of historical experiments. See [current-portfolio-first scope](./CLOSEOUT_BACKLOG_2026-10-30.md#scope-reset-current-portfolio-first-closeout-october-30-2026-local-small-job-044). Retirement candidates remain deployed/preserved until a separately verified decommission.

| Repository | Project | Public source status |
| --- | --- | --- |
| [anevum](https://github.com/anevum/anevum) | Devon's GitHub profile | Profile and cross-project index. |
| [anevum-web](https://github.com/anevum/anevum-web) | ANEVUM website and integrated platform | Source and history on main; repository separation is in progress. |
| [rhen](https://github.com/anevum/rhen) | Experimental market research software | **Parked for feature development**. Source/tests and Apache-2.0 license remain on main; verify Railway/broker runtime and dependent services before any retirement. |
| [devonakins.com](https://github.com/anevum/devonakins.com) | Devon's personal website | Source and tests on main; MIT license. |
| [family-adventure-book](https://github.com/anevum/family-adventure-book) | Independent family adventure game | **Parked / retirement candidate**. Source and a Worker deployment still exist. No new development or deployment work; verify family data and routing before decommissioning; preserve Git history. |
| [brandle](https://github.com/anevum/brandle) | Independent word game | Source/tests and live standalone game verified; production release still belongs to the legacy ANEVUM Web deployer pending gated cutover. Brandicade's direct launcher is staged, not a shared-progress integration. |
| [cristybreathe](https://github.com/anevum/cristybreathe) | Personal workspace software | Source, tests and Apache-2.0 license imported in [PR 1](https://github.com/anevum/cristybreathe/pull/1). Later work needs reconciliation before release. |
| [brandicade](https://github.com/anevum/brandicade) | Private family game collection | **README only on main.** [Draft recovery PR #1](https://github.com/anevum/brandicade/pull/1) now has passing CI and one-tap Brandle launchers to its original site; changes are not live. The running Access/D1 save backend, identity/schema compatibility, full in-arcade integration, license provenance and rollback remain unresolved in [issue #2](https://github.com/anevum/brandicade/issues/2). |
| [devon-station](https://github.com/anevum/devon-station) | Personal workspace software | README only; public-safe source review pending. |
| [ideaflow](https://github.com/anevum/ideaflow) | Idea capture and meeting software | README only; earlier intake/operations source and a separate meeting-presenter release located, but current public-safe source reconciliation is pending. |
| [severance](https://github.com/anevum/severance) | ANEVUM family creative prototype | **Parked creative source**. Godot prototype and offline world-state experiments are preserved; no active game release obligation. Original lineage remains in [anevum-web](https://github.com/anevum/anevum-web/pull/788). |
| [cristyrusso.com](https://github.com/anevum/cristyrusso.com) | Planned professional website | **Planned; README only**. Separate design/content approvals are required before implementation. No placeholder application or assumed existing source. |

Brandle and CristyBreathe imports preserve project-specific lineage while retaining the original history in anevum-web. Their standalone main-branch verification passed at the imported commits. That does not by itself establish production deployment ownership or verify every feature.

Use each project's own documentation for build, test, licensing and contribution details. Treat an empty repository as a destination awaiting verified source, not as a finished application. Review third-party rights before licensing or publishing recovered material. Never commit private data, credentials or operational backups.
