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
- **Brandicade:** a later V1.0.1 source archive builds and its seven logic tests pass. All 14 static assets match those embedded in the live Worker by SHA-256. The deployed Worker also includes a cloud-save layer absent from that archive. The generated Worker header identifies GPLv3 while the archive contains an MIT license; investigate provenance and rights before publishing or relicensing, and recover the server-side source without private configuration.
- **DevonStation:** a private development archive exists and contains operational snapshots. Build and verify a public-safe export rather than publishing the archive wholesale.
- **IdeaFlow:** earlier intake, analyzer and operations source and a separate meeting-presenter release have been located. The intake archive predates the current manual-processing change; do not treat it as the current production source without reconciliation. Preserve manual processing and necessary retention safeguards; exclude recordings, transcripts and private configuration.
- **CristyRusso.com:** a visual design concept exists, but its credentials, service descriptions, contacts and links need verification. It is not an approved production website.
- **Severance:** history remains recoverable in the original repository, but the imported snapshot has not incorporated those commits as ancestors. The two experiments remain independent; neither is a finished game.

## Cleanup and governance still open

The inspection found 848 branches, 280 open pull requests, 62 open issues and 35 workflow files in ANEVUM web, plus 121 Workers, one Pages project and 17 D1 databases. These are point-in-time counts, not a completed classification or deletion list. Some draft PRs form chains of dependent work; inspect ancestry before closing or deleting anything.

Review the ANEVUM web release workflows and production route before removing any code. Keep the retired legacy production deployment disabled. Configure practical branch protection and required checks after identifying the checks that actually run for the intended changes. Review current and historical credentials, licensing and third-party rights; RHEN has no root license observed and Family Adventure Book states that it has no open-source license. No comprehensive secret-history audit, infrastructure cleanup, deployment handover or account-wide governance completion is claimed here.
