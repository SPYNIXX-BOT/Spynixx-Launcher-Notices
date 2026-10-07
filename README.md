# Spynixx Launcher Notices

This public repository contains launcher announcements only. It does not contain the private launcher source code.

## Publishing a new notice

1. Edit `update-notice.json`.
2. Give `noticeId` a value that has never been used before.
3. Update the title, date, type, and content.
4. Keep `schemaVersion` set to `1`.
5. Commit and push to the `main` branch.

Supported notice types are `info`, `update`, `warning`, and `maintenance`.

Set `latestVersion` for launcher updates. The startup popup is shown only when the installed launcher version is older. Remove `latestVersion` for a general announcement that should pop up for every launcher version.

Use `releaseUrl` for the notice's **View Release** button. For security, it must point to `https://github.com/SPYNIXX-BOT/Spynixx-Launcher-Notices/releases/`.

For an `update` notice, `downloadUrl` and `sha256` are required. `downloadUrl` must be the exact URL of an uploaded `.msi` or `.exe` asset under `https://github.com/SPYNIXX-BOT/Spynixx-Launcher-Notices/releases/download/`. `sha256` must be the lowercase SHA-256 digest of that exact asset. The launcher deliberately does not guess release filenames.

Launcher releases must be published by the launcher's `publish-release.yml` workflow. It validates that the tag and all project versions match, publishes the installer and updater signature, generates `latest.json`, verifies its download URL character-for-character, and updates this notice from the published asset.

Set `enabled` to `false` to stop showing the notice. An enabled announcement appears when the launcher starts and remains available from the Announcements button in the sidebar.

Do not put passwords, API keys, GitHub tokens, private URLs, or other secrets in this repository.
