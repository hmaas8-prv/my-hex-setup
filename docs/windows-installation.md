# Install Hex on Windows

This guide installs the stable Hex release for the current Windows user using
the project's official managed installer.

## Requirements

- 64-bit Windows on x64 or ARM64
- PowerShell 5.1 or newer
- Internet access for the application and selected speech model
- Microphone access

## Install

Open PowerShell and run:

```powershell
$env:HEX_INSTALL_CHANNEL = "stable"
irm https://raw.githubusercontent.com/anomalyco/hex/dev/.github/release/install-windows.ps1 | iex
```

Review the
[upstream installer source](https://github.com/anomalyco/hex/blob/dev/.github/release/install-windows.ps1)
before running it. The installer downloads the release manifest over HTTPS and
checks the application size, SHA-256 digest, reported version, and Authenticode
signature.

The managed installation is stored under `%APPDATA%\hex` and adds
`%APPDATA%\hex\bin` to the user `PATH`. Open a new terminal before using the
`hex` command.

## Verify

In a new PowerShell session:

```powershell
$version = Get-Content "$env:APPDATA\hex\current-version" -Raw
$executable = "$env:APPDATA\hex\versions\$version\hex.exe"
hex --version
Get-AuthenticodeSignature $executable
```

Confirm that a version is printed and the signature status is `Valid`.

## Tested Result

This procedure was tested on Windows 11 x64 on 11 November 2026:

- Installed Hex `3.4.0` on the stable channel.
- `hex --version` returned `hex 3.4.0`.
- The executable's Authenticode status was `Valid`.
- The signer was `Anomaly Innovations, Inc`.
- The Start menu shortcut was created.
- `%APPDATA%\hex\bin` was added to the user `PATH`.

## First Launch

1. Start Hex from the Start menu.
2. Complete the onboarding flow.
3. Grant microphone access when Windows requests it.
4. Download a speech model suitable for the intended language.
5. Test dictation in a non-sensitive text field.

Do not dictate private material while initially testing history and audio
retention settings.

## Uninstall

The same upstream script supports `-Uninstall`. Download it first so the
parameter can be passed explicitly:

```powershell
$script = "$env:TEMP\install-hex.ps1"
irm https://raw.githubusercontent.com/anomalyco/hex/dev/.github/release/install-windows.ps1 -OutFile $script
powershell -ExecutionPolicy Bypass -File $script -Uninstall
Remove-Item $script
```

The upstream uninstaller intentionally leaves settings and logs in place.
Review those files separately if a complete data removal is required.
