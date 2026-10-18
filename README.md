# Lana desktop downloads

Private preview builds for team testing and feedback.

[Lana Desktop 0.1.3 downloads and release notes](https://github.com/frain-dev/lana-releases/releases/tag/v0.1.3)

Desktop **0.1.3** uses **Electron 44.9.0** for its interface and Chromium browser, retains Lana's Rust services, and bundles **Lana CLI 0.4.3**. Choose the download that matches your operating system and processor:

| Platform | Download | Install |
| --- | --- | --- |
| macOS, Apple Silicon | [ZIP](https://github.com/frain-dev/lana-releases/releases/download/v0.1.3/Lana-macos-arm64.zip) | Unzip and move **Lana.app** to Applications. |
| macOS, Intel | [ZIP](https://github.com/frain-dev/lana-releases/releases/download/v0.1.3/Lana-macos-x64.zip) | Unzip and move **Lana.app** to Applications. |
| Windows, x64 | [Installer](https://github.com/frain-dev/lana-releases/releases/download/v0.1.3/Lana-windows-x64-setup.exe) | Run the installer, then open Lana from Start. |
| Windows, ARM64 | [Installer](https://github.com/frain-dev/lana-releases/releases/download/v0.1.3/Lana-windows-arm64-setup.exe) | Run the installer, then open Lana from Start. |
| Linux, x64 | [AppImage](https://github.com/frain-dev/lana-releases/releases/download/v0.1.3/Lana-linux-x64.AppImage) or [Debian package](https://github.com/frain-dev/lana-releases/releases/download/v0.1.3/Lana-linux-x64.deb) | Prefer the `.deb` for a managed installation; see AppImage setup below. |
| Linux, ARM64 | [AppImage](https://github.com/frain-dev/lana-releases/releases/download/v0.1.3/Lana-linux-arm64.AppImage) or [Debian package](https://github.com/frain-dev/lana-releases/releases/download/v0.1.3/Lana-linux-arm64.deb) | Prefer the `.deb` for a managed installation; see AppImage setup below. |

On Ubuntu 24.04 and other AppArmor hosts that restrict unprivileged user namespaces, AppImage requires administrator setup: verify the release checksum, install the root-owned `0755` file at `/opt/Lana.AppImage`, and load the application-specific AppArmor profile for that exact path. Chromium's sandbox remains enabled. FUSE and native runtime libraries are also required. Follow the [matching AppImage setup guide](https://github.com/frain-dev/lana-desktop/blob/ce4b9a67b6be9974b356d111eb7ad40d127c56ae/docs/electron-distribution.md#appimage-on-ubuntu-2404-and-other-restricted-apparmor-hosts); prefer the Debian package for managed installation.

Close Lana before replacing an existing installation and keep its application data. Existing native account credentials and conversation history remain in the regular Lana profile. Sign in with your Lana account if prompted after launching the app.

Chromium has separate website storage. Website sign-ins and cookies from the older WebKit browser, along with browser UI preferences, do not automatically transfer. Import a supported browser profile from the browser's three-dot menu and select your preferences again. Encrypted cookie/password import currently requires macOS Keychain access; support varies by browser and platform. Tabs opened in this version are saved per chat by default; sharing tabs across chats is optional.

This preview adds Customize discovery for skills, connectors and plugins, publisher and brand details, shared install counts, and Most installed sorting. The Customize toolbar stays opaque while scrolling up or down. Browser restoration, background loading, favicons, address suggestions and the working pointer are improved. Terminals load the user's shell startup profile and can start as soon as their folder is approved.

Some connectors require vendor registration, API credentials or consent. Catalog presence does not establish a working connection. Selected Termii and Paystack reads have passed in Lana; Tyms API subscription access, Flutterwave credentials and Eazipay gateway availability remain pending.

Both macOS downloads are Developer ID signed, notarized by Apple and stapled. Gatekeeper and launch/restart of each extracted final ZIP passed. Windows installers are unsigned and may show an unknown-publisher or SmartScreen warning. Both Linux targets passed Debian installation and original AppImage launch/restart with Chromium's sandbox and the documented host policy; no signed APT repository is provided.

Installation, first launch, restart and removal passed on all six native targets in [the release qualification run](https://github.com/frain-dev/lana-desktop/actions/runs/39163389061). `SHA256SUMS` lists the eight distributions and two JSON evidence files. These smoke tests do not establish account sign-in, every app feature, upgrades, or compatibility with every operating system version. The release notes and artifact evidence identify the qualified builds.

[Previous preview: 0.1.2](https://github.com/frain-dev/lana-releases/releases/tag/v0.1.2) remains available unchanged.

Repository access is required to view and download these private releases. Share feedback with the Lana team before public distribution.
