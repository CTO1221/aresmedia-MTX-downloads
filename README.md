# AresMedia-MTX downloads

Public installer downloads. No GitHub login is required.

## Ubuntu 22.04 / 26.04 LTS, amd64

- [Installer: 2026.10.08](https://github.com/CTO1221/aresmedia-MTX-downloads/releases/download/v2026.10.08/aresmedia-mtx-2026.10.08-ubuntu-amd64.run)
- [SHA-256 checksum](https://github.com/CTO1221/aresmedia-MTX-downloads/releases/download/v2026.10.08/aresmedia-mtx-2026.10.08-ubuntu-amd64.run.sha256)
- [Release notes](https://github.com/CTO1221/aresmedia-MTX-downloads/releases/tag/v2026.10.08)

Download and install in an SSH terminal:

```bash
curl -fLO https://github.com/CTO1221/aresmedia-MTX-downloads/releases/download/v2026.10.08/aresmedia-mtx-2026.10.08-ubuntu-amd64.run
curl -fLO https://github.com/CTO1221/aresmedia-MTX-downloads/releases/download/v2026.10.08/aresmedia-mtx-2026.10.08-ubuntu-amd64.run.sha256
sha256sum -c aresmedia-mtx-2026.10.08-ubuntu-amd64.run.sha256 && sudo bash aresmedia-mtx-2026.10.08-ubuntu-amd64.run
```

Internet access is required for Ubuntu/Python dependencies. The installer asks
for domain/IP, RTMP access, WHIP/WebRTC, HTTPS and first administrator settings.
It installs to `/opt/aresmedia-mtx`. Existing installations and cross-version
upgrades are not overwritten by this package.

This is the requested original **2026.10.08** build, with runtime helpers under
`tools/`. The later **2026.10.08.1** clean-layout build is a different artifact.

Installer SHA-256: `1c46e6744e332b05414ff7ac0146a73a5359b60b77fe594131563f418255c960`.
