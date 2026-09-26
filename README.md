# eckstein-jobs-state

Job **stage** data for the [Eckstein Jobs](https://claude69420.github.io/eckstein-jobs/) app
(Ready to start → Excavation → Base → Prep → Passed inspection → Poured).

- `stages.json` is written **by the app** through the GitHub API. Every stage move is one commit, so the commit
  history of this repo is the audit trail and any stage can be restored from it.
- Shape: `{"version":1,"stages":{"<jobNumber>":{"stage":"<key>","at":"<ISO-8601 UTC>","by":"<device label>"}}}`.
  Jobs with no entry are "Ready to start".
- Kept separate from the app repo on purpose: the app's edit key can only touch this repo, never the app itself.

Full documentation: `APP_MASTER.md` in [Claude69420/eckstein-jobs](https://github.com/Claude69420/eckstein-jobs).
