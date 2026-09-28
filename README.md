# RPL-Retail — Installer downloads

This repository distributes the Windows installer for **RPL-Retail**, retail
management software by Regards Private Limited.

It contains **no source code**. The application source is private; this repo
holds only the built installer packages so that installed copies of the app
can update themselves without needing any credentials.

## Downloads

Get the latest installer from the [Releases page](../../releases/latest).

Each release contains:

| File | Purpose |
| --- | --- |
| `RPL-Retail-Setup-<version>.exe` | The Windows installer |
| `RPL-Retail-Setup-<version>.exe.sha256` | SHA-256 checksum of the installer |

## Verifying a download

The app verifies this automatically before installing an update. To check a
download by hand, run in PowerShell:

```powershell
Get-FileHash .\RPL-Retail-Setup-<version>.exe -Algorithm SHA256
```

The result should match the hash in the matching `.sha256` file.

## Automatic updates

Installed copies of RPL-Retail check this repository at launch and offer any
newer version. Installing requires Windows administrator approval. To stop a
particular machine updating itself, set `AUTO_UPDATE=0` in that machine's
`.env` file; the Settings screen still allows a manual check.

---

© Regards Private Limited
