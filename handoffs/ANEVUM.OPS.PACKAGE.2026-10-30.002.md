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
- **CristyBreathe:** reconcile [calendar draft PR #796](https://github.com/anevum/anevum-web/pull/796) into the standalone source. Backup restoration, access and real-user acceptance remain release gates; do not apply the draft database migration as part of a source-only import.
- **Brandicade:** a local-save development archive passed seven logic tests, but it does not establish parity with the deployed application. Recover and review the server-side work before import.
- **DevonStation:** a private development archive exists and contains operational snapshots. Build and verify a public-safe export rather than publishing the archive wholesale.
- **IdeaFlow:** identify the source and roles of intake, meeting, processing and operations components. Preserve manual processing and necessary retention safeguards; exclude recordings, transcripts and private configuration.
- **CristyRusso.com:** a visual design concept exists, but its credentials, service descriptions, contacts and links need verification. It is not an approved production website.
- **Severance:** history remains recoverable in the original repository, but the imported snapshot has not incorporated those commits as ancestors. The two experiments remain independent; neither is a finished game.

## Cleanup and governance still open

The inspection found 848 branches, 280 open pull requests, 62 open issues and 35 workflow files in ANEVUM web, plus 121 Workers, one Pages project and 17 D1 databases. These are point-in-time counts, not a completed classification or deletion list. Some draft PRs form chains of dependent work; inspect ancestry before closing or deleting anything.

Review the ANEVUM web release workflows and production route before removing any code. Keep the retired legacy production deployment disabled. Configure practical branch protection and required checks after identifying the checks that actually run for the intended changes. Review current and historical credentials, licensing and third-party rights; RHEN has no root license observed and Family Adventure Book states that it has no open-source license. No comprehensive secret-history audit, infrastructure cleanup, deployment handover or account-wide governance completion is claimed here.
