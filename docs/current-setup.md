# Current Sanitized Setup

This page records selected, portable behavior without publishing the raw Hex
settings file. It was last verified on 11 November 2026 with Hex `3.4.0` on
Windows 11 x64.

## Dictation

| Setting | Value |
|---|---|
| Shortcut | Hold `Ctrl` + `Space` |
| Speech model | NVIDIA Parakeet V3 |
| Language | German (`de`) |
| Processing device | Automatic |
| Microphone | System/default selection |
| Double-tap lock | Enabled |
| Paste previous result | `Ctrl` + `Alt` + `V` |
| Cancel | `Escape` |

The downloaded model data occupies approximately 706 MB on this machine. Model
size may change between Hex releases.

## Privacy-Related Choices

| Setting | Value |
|---|---|
| Dictation history retention | One week |
| Keep recording audio | Disabled |
| Meetings | Disabled |
| Meeting summaries | Off |
| Post-processing | Disabled |
| Labs features | Disabled |

Text history remains personal even when audio retention is disabled. It is not
exported to this repository.

## Application Behavior

| Setting | Value |
|---|---|
| Start Hex at login | Enabled |
| Sound effects | Enabled at 50% |
| Avoid Bluetooth microphone | Enabled |
| Capture shortcut | `F9` |

Hex Capture is enabled in the current defaults. Review this feature and its
retention behavior before using it with sensitive applications.

## Verify Without Exporting Settings

Hex exposes individual settings through its CLI. These commands verify the
main choices without copying the complete settings file:

```powershell
hex settings get transcription.model
hex settings get transcription.language
hex settings get history_retention
hex settings get meetings.enabled
```

Expected values for this setup are `parakeet_v3`, `de`, `week`, and `false`.

## Why the Raw File Is Excluded

`%APPDATA%\hex\settings.json` can evolve to include personal vocabulary,
replacement rules, application selectors, local folders, device identifiers,
and integration settings. The repository therefore documents reviewed choices
rather than synchronizing the complete file.
