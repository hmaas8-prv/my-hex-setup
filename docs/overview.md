---
title: "Hex Overview"
description: "Independent overview of Hex based on its public project materials."
source_repository: "https://github.com/anomalyco/hex"
source_website: "https://anoma.ly/hex"
topic: "Local AI voice dictation"
product: "Hex"
related_products:
  - "OpenCode"
tags:
  - hex
  - voice-dictation
  - speech-to-text
  - local-ai
  - open-source
  - macos
  - windows
  - linux
language: "English"
content_type: "independent-overview"
---

# Hex - Local Voice Dictation

Hex is an open-source desktop application for local voice dictation. Hold a
configured key, speak, and release it to paste the transcription into the
active application.

This overview is independently maintained from public upstream sources. It is
not an official Hex publication and is not affiliated with Anomaly.

## Key Characteristics

- Speech transcription runs on the user's computer.
- After the application and speech model are downloaded, dictation can operate
  without sending recordings to a remote transcription service.
- Hex supports macOS, Windows, and Linux.
- Different local speech models can be selected for language, accuracy, and
  performance requirements.
- The project is distributed under the MIT License.

## Basic Workflow

1. Place the cursor in an application or text field.
2. Hold the configured dictation shortcut.
3. Speak.
4. Release the shortcut.
5. Hex transcribes the recording locally and pastes the result.

## Installation

Use the downloads and instructions published by the Hex project:

- Website: [anoma.ly/hex](https://anoma.ly/hex)
- Repository: [github.com/anomalyco/hex](https://github.com/anomalyco/hex)
- Documentation: [Hex docs](https://github.com/anomalyco/hex/tree/dev/docs)

The public repository lists installers for macOS, Windows, and Linux. Platform
requirements and available installation methods can change, so they should be
checked upstream rather than duplicated here.

## Personal Setup

A shareable setup should contain only deliberately authored and reviewed files,
such as:

- Documentation explaining the selected model and shortcuts.
- Sanitized examples of portable preferences.
- Reviewed personal commands from `~/.config/hex/`.
- Installation or validation scripts that do not contain credentials or
  machine-specific data.

Do not publish a complete Hex application-data directory. Depending on enabled
features, it can contain transcription history, audio, meeting records, logs,
local paths, device details, process information, or authorization material.

## Licensing

Hex source code is licensed under the MIT License. Redistributing Hex source or
substantial portions of it requires preserving the upstream copyright and
permission notice. A separate repository containing original setup notes and
configuration should use its own license and should clearly identify any
upstream material it includes.

Public availability is not the same as public-domain status. Content without an
explicit reuse license should not be copied into this repository merely because
it can be viewed online.

## Public References

- [Hex website](https://anoma.ly/hex)
- [Hex repository](https://github.com/anomalyco/hex)
- [Hex MIT License](https://github.com/anomalyco/hex/blob/dev/LICENSE)
- [Hex documentation](https://github.com/anomalyco/hex/tree/dev/docs)
- [OpenCode](https://opencode.ai)

## Source Note

This document was independently written from the public references above. It
does not rely on or reproduce private repositories, internal presentations, or
employer-specific materials. Product behavior and requirements should be
verified against the current upstream documentation before use.
