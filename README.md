# My Hex Setup

An independent, reproducible setup for
[Hex](https://github.com/anomalyco/hex), a local voice-dictation application.

This repository documents installation and deliberately selected preferences.
It does not contain Hex application data, transcription history, recordings,
credentials, or private workplace material.

## Current Setup

- Platform: Windows 11 x64
- Hex channel: Stable
- Installation method: Official managed Windows installer
- Installed version: 3.4.0
- Status: Installed, signature verified, and first-run setup complete

## Guides

- [Windows installation](docs/windows-installation.md)
- [Current sanitized setup](docs/current-setup.md)
- [Hex overview](docs/overview.md)

## Privacy

Do not copy `%APPDATA%\hex`, `%LOCALAPPDATA%\hex`, or exported meeting folders
into this repository. Those locations may contain transcripts, audio, logs,
local API authorization, personal vocabulary, device details, and local paths.

Only reviewed, sanitized examples belong here. See [`.gitignore`](.gitignore)
for defensive exclusions.

## Upstream Project

Hex is developed by Anomaly and distributed under the
[MIT License](https://github.com/anomalyco/hex/blob/dev/LICENSE). This
repository is independent and is not affiliated with or endorsed by Anomaly.

No Hex source code or binaries are redistributed here.

## License

Original material in this repository is available under the [MIT License](LICENSE).
Hex itself is a separate and distinct upstream project under its own MIT license and
copyright notice.
