# Spynixx Launcher Notices

This public repository contains launcher announcements only. It does not contain the private launcher source code.

## Publishing a new notice

1. Edit `update-notice.json`.
2. Give `noticeId` a value that has never been used before.
3. Update the title, date, type, and content.
4. Keep `schemaVersion` set to `1`.
5. Commit and push to the `main` branch.

Supported notice types are `info`, `update`, `warning`, and `maintenance`.

Use `releaseUrl` for the notice's **View Release** button. For security, it must point to `https://github.com/SPYNIXX-BOT/Spynixx-Launcher-Notices/releases/`.

Set `enabled` to `false` to stop showing the notice. An enabled announcement appears when the launcher starts and remains available from the Announcements button in the sidebar.

Do not put passwords, API keys, GitHub tokens, private URLs, or other secrets in this repository.
