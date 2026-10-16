# Lana desktop downloads

Private preview builds for team testing and feedback.

[Download the latest preview](https://github.com/frain-dev/lana-releases/releases/tag/v0.1.1)

Desktop **0.1.1** bundles Lana CLI **0.4.2**. Choose the download that matches your operating system and processor:

| Platform | Download | Install |
| --- | --- | --- |
| macOS, Apple Silicon | `Lana-macos-arm64.zip` | Unzip and move **Lana.app** to Applications. |
| macOS, Intel | `Lana-macos-x64.zip` | Unzip and move **Lana.app** to Applications. |
| Windows, x64 | Installer ending in `_x64-setup.exe` | Run the installer, then open Lana from Start. |
| Windows, ARM64 | Installer ending in `_arm64-setup.exe` | Run the installer, then open Lana from Start. |
| Linux, x64 | `amd64` AppImage or Debian package | Make the AppImage executable and open it, or install the `.deb`. |
| Linux, ARM64 | `aarch64` AppImage or `arm64` Debian package | Make the AppImage executable and open it, or install the `.deb`. |

Sign in with your Lana account after launching the app. Close Lana before replacing an existing installation; keep application data to preserve your settings and history.

Both Mac downloads are Developer ID signed, notarized by Apple and stapled for Gatekeeper verification. Windows installers are currently unsigned and may show an unknown-publisher or SmartScreen warning. Windows signing is pending. Linux downloads include SHA-256 checksums; this preview does not provide a signed APT repository.

`SHA256SUMS` lists every installer/archive checksum. Installation, first launch and restart are tested on native CI runners for all six targets. These smoke tests do not cover account sign-in, every app feature, upgrades, or every operating system version. See the release notes for the tested environments.

Repository access is required to view and download these private releases. Share feedback with the Lana team before public distribution.
