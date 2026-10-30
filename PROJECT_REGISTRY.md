# Public project registry

Session: `ANEVUM.OPS.PACKAGE.2026-10-30.002.COMPLETE-GITHUB-RESTRUCTURE`  
Snapshot: October 30, 2026. This registry describes public source status, not deployment readiness. [See the evidence-based completion audit](./AUDIT_2026-10-30.md): repository reorganization is **not complete**. Verify the current project and release documentation before making changes. Private operations and recovery information belong in private records.

| Repository | Project | Public source status |
| --- | --- | --- |
| [anevum](https://github.com/anevum/anevum) | Devon's GitHub profile | Profile and cross-project index. |
| [anevum-web](https://github.com/anevum/anevum-web) | ANEVUM website and integrated platform | Source and history on main; repository separation is in progress. |
| [rhen](https://github.com/anevum/rhen) | ANEVUM market research software | Source and tests on main; Apache-2.0 license. |
| [devonakins.com](https://github.com/anevum/devonakins.com) | Devon's personal website | Source and tests on main; MIT license. |
| [family-adventure-book](https://github.com/anevum/family-adventure-book) | Independent family adventure game | Local-save prototype; Apache-2.0 license. |
| [brandle](https://github.com/anevum/brandle) | Independent word game | Source, tests, Apache-2.0 license and dictionary notice imported in [PR 1](https://github.com/anevum/brandle/pull/1). Deployment handover remains separate. |
| [cristybreathe](https://github.com/anevum/cristybreathe) | Personal workspace software | Source, tests and Apache-2.0 license imported in [PR 1](https://github.com/anevum/cristybreathe/pull/1). Later work needs reconciliation before release. |
| [brandicade](https://github.com/anevum/brandicade) | Independent game collection | README only on main; [static source recovery draft](https://github.com/anevum/brandicade/pull/1) is under verification, with cloud-save source and license notices still to reconcile. |
| [devon-station](https://github.com/anevum/devon-station) | Personal workspace software | README only; public-safe source review pending. |
| [ideaflow](https://github.com/anevum/ideaflow) | Idea capture and meeting software | README only; earlier intake/operations source and a separate meeting-presenter release located, but current public-safe source reconciliation is pending. |
| [severance](https://github.com/anevum/severance) | ANEVUM game development | Godot prototype and separate offline world-state lab imported in [PR 1](https://github.com/anevum/severance/pull/1); the original prototype history remains in [anevum-web](https://github.com/anevum/anevum-web/pull/788). |
| [cristyrusso.com](https://github.com/anevum/cristyrusso.com) | Professional website | README only; source recovery pending. |

Brandle and CristyBreathe imports preserve project-specific lineage while retaining the original history in anevum-web. Their standalone main-branch verification passed at the imported commits. That does not by itself establish production deployment ownership or verify every feature.

Use each project's own documentation for build, test, licensing and contribution details. Treat an empty repository as a destination awaiting verified source, not as a finished application. Review third-party rights before licensing or publishing recovered material. Never commit private data, credentials or operational backups.
