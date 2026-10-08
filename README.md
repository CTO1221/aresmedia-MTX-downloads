# AresMedia-MTX downloads

Public installer downloads. No GitHub login is required.

## Latest stable: v2026.10.08.2

Ubuntu **22.04 LTS / 26.04 LTS**, **amd64**. Includes the Pusher pipeline identity fix and clean production layout.

- [Download installer](https://github.com/CTO1221/aresmedia-MTX-downloads/releases/download/v2026.10.08.2/aresmedia-mtx-2026.10.08.2-ubuntu-amd64.run)
- [SHA-256 checksum](https://github.com/CTO1221/aresmedia-MTX-downloads/releases/download/v2026.10.08.2/aresmedia-mtx-2026.10.08.2-ubuntu-amd64.run.sha256)
- [Release notes](https://github.com/CTO1221/aresmedia-MTX-downloads/releases/tag/v2026.10.08.2)
- [Latest stable](https://github.com/CTO1221/aresmedia-MTX-downloads/releases/latest) · [All versions](https://github.com/CTO1221/aresmedia-MTX-downloads/releases)

## Install in an SSH terminal

```bash
curl -fLO https://github.com/CTO1221/aresmedia-MTX-downloads/releases/download/v2026.10.08.2/aresmedia-mtx-2026.10.08.2-ubuntu-amd64.run
curl -fLO https://github.com/CTO1221/aresmedia-MTX-downloads/releases/download/v2026.10.08.2/aresmedia-mtx-2026.10.08.2-ubuntu-amd64.run.sha256
sha256sum -c aresmedia-mtx-2026.10.08.2-ubuntu-amd64.run.sha256 && sudo bash aresmedia-mtx-2026.10.08.2-ubuntu-amd64.run
```

The interactive wizard asks for domain/IP, RTMP, WHIP/WebRTC, HTTPS and first administrator settings.
MediaMTX is bundled. Internet access is required for Ubuntu/Python dependencies.
Installs into `/opt/aresmedia-mtx`; runtime helpers are in `libexec/`, policies in `config/`.
The package excludes development tools, Git history, Markdown, task lists and recordings.

This installer supports fresh installation and repeating the exact same build.
It refuses cross-version replacement of an existing installation. Retaining an older installer
does not provide automatic server rollback; keep compatible data/configuration backups for migration.

Installer SHA-256: `6ae6584bd234492a1becb5cd41c249c448812d7a351d60b01f8aec7adc93cfe6`.

## Retained releases

| Version | Contents | Download |
| --- | --- | --- |
| [v2026.10.08.2](https://github.com/CTO1221/aresmedia-MTX-downloads/releases/tag/v2026.10.08.2) | Current stable: Pusher fix, clean production layout | [Installer](https://github.com/CTO1221/aresmedia-MTX-downloads/releases/download/v2026.10.08.2/aresmedia-mtx-2026.10.08.2-ubuntu-amd64.run) |
| [v2026.10.08](https://github.com/CTO1221/aresmedia-MTX-downloads/releases/tag/v2026.10.08) | Previous stable, original layout | [Installer](https://github.com/CTO1221/aresmedia-MTX-downloads/releases/download/v2026.10.08/aresmedia-mtx-2026.10.08-ubuntu-amd64.run) |

Each update gets a new version, tag and asset names. Older releases keep their version-specific links.
Test versions use a suffix such as `-rc.1`, are marked pre-release and do not replace Latest stable.

New releases are immutable: upload and verify the installer and checksum in a draft before publishing.
Published assets must not be replaced, version tags must not be moved and older releases must not be deleted.
Corrections require a new version. The original v2026.10.08 predates GitHub's immutability setting and is retained unchanged.
