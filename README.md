# Ambivience

**Everything you saved, coming back around.**

Ambivience gathers your Watch Later videos, bookmarks, Instagram saves, and notes into one calm wall, kept as plain markdown in your Obsidian vault. It runs on your computer and opens in your browser. No account.

[ambivience.com](https://ambivience.com)

This repository holds Ambivience's downloads. The source code isn't published here.

## Download

| System | File |
| --- | --- |
| macOS, Apple Silicon (M1 or later) | [Ambivience-mac-arm64.dmg](https://github.com/LeNPaul/ambivience-releases/releases/latest/download/Ambivience-mac-arm64.dmg) |
| macOS, Intel | [Ambivience-mac-x64.dmg](https://github.com/LeNPaul/ambivience-releases/releases/latest/download/Ambivience-mac-x64.dmg) |
| Windows 10 or 11 (64-bit) | [Ambivience-windows-x64-setup.exe](https://github.com/LeNPaul/ambivience-releases/releases/latest/download/Ambivience-windows-x64-setup.exe) |
| Linux (64-bit) | [Ambivience-linux-x64.tar.gz](https://github.com/LeNPaul/ambivience-releases/releases/latest/download/Ambivience-linux-x64.tar.gz) |

Not sure which Mac you have? Apple menu → **About This Mac**. "Chip: Apple M…" is Apple Silicon; "Processor: Intel" is Intel. Ambivience needs macOS 13 (Ventura) or later.

Older versions and release notes are on the [Releases](https://github.com/LeNPaul/ambivience-releases/releases) page. You'll also need a folder of notes, like an Obsidian vault.

## Install

### macOS

1. Open the `.dmg` and drag Ambivience into Applications.
2. Open Ambivience. Because it isn't signed with a paid Apple developer certificate, macOS blocks it the first time:
   - **macOS 15 or later:** click **Done**, open **System Settings → Privacy & Security**, scroll down to the message about Ambivience, click **Open Anyway**, and confirm with your password.
   - **macOS 13 or 14:** right-click Ambivience in Applications, choose **Open**, then **Open** again.

You do this once per version. Ambivience then opens in your browser, and its icon sits in the menu bar: use it to open Ambivience again or to quit it. There's no Dock icon.

### Windows

1. Run `Ambivience-windows-x64-setup.exe`.
2. If Windows shows "Windows protected your PC", click **More info**, then **Run anyway**.

It installs for your account only (no admin needed), adds Ambivience to the Start menu, and opens it in your browser. To quit, use **Quit Ambivience** in the app's ••• menu. Opening it from the Start menu while it's running takes you back to it.

### Linux

```sh
tar -xzf Ambivience-linux-x64.tar.gz
./ambivience/ambivience
```

It prints its address and opens your browser. To quit, use **Quit Ambivience** in the app's ••• menu, or press Ctrl+C. With zenity or kdialog installed you can pick your vault from a folder dialog; otherwise type its path.

## First run

Ambivience asks where your vault is. It keeps everything in an `Ambivience` folder inside it and leaves the rest of your vault alone. Its settings are saved in `.ambivience` in your home folder.

## Check your download

Each release includes `SHA256SUMS`. To confirm your file is exactly what was published here, compute its checksum and compare it with the matching line:

```sh
# macOS
shasum -a 256 Ambivience-mac-arm64.dmg
# Linux
sha256sum Ambivience-linux-x64.tar.gz
```

```powershell
# Windows (PowerShell)
Get-FileHash .\Ambivience-windows-x64-setup.exe -Algorithm SHA256
```

## Privacy

Your saves stay in your vault. To fill in titles and thumbnails, Ambivience visits the pages you saved, the way your browser would. Nothing else is sent anywhere, and the app only answers on your own computer (`127.0.0.1`).

## Updating

- **macOS:** quit Ambivience from the menu bar, then drag the new version into Applications and replace the old one.
- **Windows:** run the new installer; it quits Ambivience first.
- **Linux:** quit it and unpack the new version in place of the old one.

Your vault and settings stay as they are.

## Uninstalling

- **macOS:** quit Ambivience from the menu bar, then drag it from Applications to the Trash.
- **Windows:** Settings → Apps → Installed apps → Ambivience → Uninstall.
- **Linux:** delete the folder you unpacked.

To remove your settings too, delete `.ambivience` in your home folder. Your vault isn't touched: your items stay as markdown notes in its `Ambivience` folder.

## Feedback

Found a bug or have an idea? [Open an issue](https://github.com/LeNPaul/ambivience-releases/issues).

## License

Free for personal use. All rights reserved. See [LICENSE](LICENSE).
