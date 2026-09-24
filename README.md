# AuNote Beta (GitHub Pages)

This directory is the static deployment copy of AuNote V1.4.2-beta.3 from
`HarryAuu999/field-research-data-tool`, branch `codex/aunote-beta-1.4.2`,
commit `1453466`. It contains only files needed by the PWA. No build step is
required; publish the repository's `main` branch from `/` with GitHub Pages.

The GitHub Pages copy uses IndexedDB `research-notebook-beta-github`. This is
intentional: separate project repositories under `harryauu999.github.io`
share an origin, so the production site's `research-notebook` database would
otherwise be visible to the Beta. The Beta service worker and Manifest are
already scoped to this repository's path, and its icons and title are yellow
and labeled “AuNote Beta”.

Test records stay in the browser or installed PWA. This repository contains
no research records or backups. Installing from the new GitHub Pages address
starts with a separate local dataset. Use the app's full JSON backup and
restore only when a deliberate transfer is needed.

For future updates, copy the runtime files from the Beta source branch,
preserve this deployment's `DB_NAME` in `js/db.js`, increment the version in
`js/app.js`, `sw.js`, and asset query parameters together, and verify the
offline cache before publishing.

