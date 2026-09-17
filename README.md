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

Optional `downloadUrl`: Specify a direct release package URL (must start with `https://github.com/SPYNIXX-BOT/Spynixx-Launcher-Notices/releases/download/`). If omitted, the launcher automatically resolves to `Spynixx.Launcher_{latestVersion}.msi` for in-app one-click update.

Set `enabled` to `false` to stop showing the notice. An enabled announcement appears when the launcher starts and remains available from the Announcements button in the sidebar.

Do not put passwords, API keys, GitHub tokens, private URLs, or other secrets in this repository.
