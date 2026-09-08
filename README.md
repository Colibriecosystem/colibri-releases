# Colibri release feed

Public distribution feed for **Colibri** — the auto-updater, the in-app version
picker and the force-update policy read this repository anonymously. Only
compiled artefacts live here (`Colibri-win.msi`, the Velopack `.nupkg` update
packages, `RELEASES`, `releases.win.json`, `assets.win.json`,
`colibri-schema.json`); the application source stays private.

Downloads: **[Releases](https://github.com/Colibriecosystem/colibri-releases/releases)**.

## History

Transferred on **2026-09-08** from `arthur-avetikyan/nexora-releases` and renamed
to `colibri-releases`. The repository id is unchanged, so GitHub permanently
redirects every old URL — web pages, the REST API and release asset links — which
is what lets builds published before the move keep updating with no user action.

## Standing rules

These protect installs that predate the move. Breaking any of them silently
brands the auto-updater for those users.

1. **Never create a repository or fork named `arthur-avetikyan/nexora-releases`**
   (treat `Colibriecosystem/nexora-releases` the same). GitHub deletes the
   redirect permanently the moment a repository exists at the old location.
2. **Never delete or rename the `arthur-avetikyan` GitHub account** — the
   redirect lives on that namespace.
3. **Never rename this repository's default branch** (`main`). The force-update
   policy URL is a compile-time constant that hardcodes `main`.
4. **Never delete a published release.** Older clients may still resolve it, and
   the version picker lists the full history.

Releases are published by `scripts/publish-release.ps1` in the private source
repository; `update-policy.json` at this repository's root is written by
`scripts/set-update-policy.ps1`.
