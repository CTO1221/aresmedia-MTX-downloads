# AresMedia-MTX downloads

Public installer downloads. No GitHub login is required.

## Release channels and retained versions

- [Latest stable](https://github.com/CTO1221/aresmedia-MTX-downloads/releases/latest): the recommended stable release.
- [All versions](https://github.com/CTO1221/aresmedia-MTX-downloads/releases): previous stable releases and explicitly marked prereleases.
- Current stable: [v2026.10.08](https://github.com/CTO1221/aresmedia-MTX-downloads/releases/tag/v2026.10.08). Its installer and checksum are retained unchanged.

Every update gets its own version, tag and asset names. New stable releases become
Latest; older releases keep their version-specific download links. Test versions
use a suffix such as `-rc.1`, are marked pre-release and do not replace Latest.

Immutable releases are enabled for future publications. Maintainers must upload
and verify both the installer and checksum in a draft before publishing. Published
assets must not be replaced, existing version tags must not be moved, and older
releases must not be deleted. Corrections are published under a new version.
GitHub applies immutability only to future releases; the existing `v2026.10.08`
release predates the setting and is preserved unchanged under this retention policy.
See [GitHub's immutability documentation](https://docs.github.com/en/code-security/how-tos/secure-your-supply-chain/establish-provenance-and-integrity/prevent-release-changes).

Retained installers do not provide automatic server rollback. Cross-version
replacement is currently refused by the installer; preserve compatible backups
before a separately planned server migration.

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
