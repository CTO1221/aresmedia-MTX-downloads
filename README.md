# AresMedia-MTX downloads

Public installer downloads; no GitHub login is required.

## Latest stable: v2026.10.08.3

Ubuntu **22.04 LTS / 26.04 LTS**, **amd64**. Includes transactional updates, the Pusher fix and clean production layout.

- [Download installer](https://github.com/CTO1221/aresmedia-MTX-downloads/releases/download/v2026.10.08.3/aresmedia-mtx-2026.10.08.3-ubuntu-amd64.run)
- [SHA-256 checksum](https://github.com/CTO1221/aresmedia-MTX-downloads/releases/download/v2026.10.08.3/aresmedia-mtx-2026.10.08.3-ubuntu-amd64.run.sha256)
- [Release notes and validation scope](https://github.com/CTO1221/aresmedia-MTX-downloads/releases/tag/v2026.10.08.3)
- [Latest stable](https://github.com/CTO1221/aresmedia-MTX-downloads/releases/latest) · [All versions](https://github.com/CTO1221/aresmedia-MTX-downloads/releases)

## Update an existing installation

Run in an SSH terminal:

```bash
curl -fLO https://github.com/CTO1221/aresmedia-MTX-downloads/releases/download/v2026.10.08.3/aresmedia-mtx-2026.10.08.3-ubuntu-amd64.run && curl -fLO https://github.com/CTO1221/aresmedia-MTX-downloads/releases/download/v2026.10.08.3/aresmedia-mtx-2026.10.08.3-ubuntu-amd64.run.sha256 && sha256sum -c aresmedia-mtx-2026.10.08.3-ubuntu-amd64.run.sha256 && sudo bash aresmedia-mtx-2026.10.08.3-ubuntu-amd64.run --update
```

Updates briefly stop media services; publishers and viewers must reconnect. Application files,
`.env`, local SQLite state and changed service configuration are backed up under
`/opt/.aresmedia-update-backups/`. Administrator accounts, settings, TLS and recordings are retained.
Recordings remain in place and are not duplicated in the backup.

The updater migrates old `tools/packaging` layouts to `libexec/config`, checks backend/worker health,
and automatically restores the previous code/database/configuration on failure. If recovery is
interrupted, rerun `--update` to finish recovery, then run it again to retry. Repeating the same
installed version verifies it without restarting services. Keep the printed backup path.

Automatic updates require a healthy managed install-pack installation, local SQLite state inside
`data/`, and unchanged Python dependencies/bundled runtime. Git/DEB installations, external databases,
custom systemd overrides, dependency changes and downgrades require a separate migration.
Unknown local code modifications are refused; the reviewed lab-c Pusher hotfix is recognized by checksum.

## Fresh installation

Download and verify the files above, then run without the update flag:

```bash
sudo bash aresmedia-mtx-2026.10.08.3-ubuntu-amd64.run
```

The wizard asks for domain/IP, RTMP, WHIP/WebRTC, HTTPS and first administrator settings.
MediaMTX is bundled; Internet is needed for Ubuntu/Python dependencies. Installation directory:
`/opt/aresmedia-mtx`. The package excludes Git history, development tools, Markdown and task lists.

Installer SHA-256: `073c2157a18e6705616286e68b9730fd253dc92bf4042d154c195438980b1327`.

## Retained releases

| Version | Contents |
| --- | --- |
| [v2026.10.08.3](https://github.com/CTO1221/aresmedia-MTX-downloads/releases/tag/v2026.10.08.3) | Current stable: transactional updater and Pusher fix |
| [v2026.10.08.2](https://github.com/CTO1221/aresmedia-MTX-downloads/releases/tag/v2026.10.08.2) | Pusher fix, clean production layout; fresh installer |
| [v2026.10.08](https://github.com/CTO1221/aresmedia-MTX-downloads/releases/tag/v2026.10.08) | Original installer |

Every update gets a new version/tag and permanent asset names. Earlier releases remain downloadable.
New releases are immutable: upload and verify all assets in a draft before publication. Corrections
require a new version. Prereleases such as `-rc.1` do not replace Latest stable. The original
v2026.10.08 predates immutability and is retained unchanged. Never delete old releases or move their tags.
