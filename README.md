# Spynixx Launcher Notices

This public repository contains launcher announcements only. It does not contain the private launcher source code.

## Publishing a new notice

1. Edit `update-notice.json`.
2. Give `noticeId` a value that has never been used before.
3. Update the title, date, type, and content.
4. Keep `schemaVersion` set to `1`.
5. Commit and push to the `main` branch.

Supported notice types are `info`, `update`, `warning`, and `maintenance`.

Set `enabled` to `false` to stop showing the notice. When `dismissible` is `true`, a user sees each `noticeId` once after dismissing it. When it is `false`, the notice appears again on their next launcher startup.

Do not put passwords, API keys, GitHub tokens, private URLs, or other secrets in this repository.
