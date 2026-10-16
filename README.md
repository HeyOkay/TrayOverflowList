# Windhawk Tray List

A Windhawk mod that displays the Windows 11 hidden tray icons as a vertical list, with icons on the left and application names on the right.

**Stable version: 0.1.8.3** · [Русская инструкция](README.ru.md)

## Features

- Uses the original tray icon controls for clicks, context menus, and dragging.
- Keeps the native flyout background and measures the native panel width.
- Recalculates the width when the number of icons changes, including while startup applications load after a reboot.
- Trims long names with an ellipsis and provides vertical scrolling for long lists.
- Offers a row height setting. The right edge correction is fixed at 1 px.
- Adds no timers for width recalculation; it uses the existing layout events.

## Compatibility

Tested by the user on Windows 11 26H2, build **26300.9457**, x64, with the Windows interface in English. Version 0.1.8.3 has been tested and confirmed working by the user on 2026-10-17.

This mod uses internal Windows tray interfaces. Compatibility with other builds and display languages has not been verified. It cannot be guaranteed after Windows updates.

## Install

1. Install and open [Windhawk](https://windhawk.net/).
2. Choose **Create a new mod** and replace the template with the complete contents of [`tray-overflow-list.wh.cpp`](tray-overflow-list.wh.cpp).
3. Click **Compile** and enable the mod if needed.
4. Open the hidden tray icons flyout.

To update an existing installation, replace its source with the same file and compile. Do not enable two copies of this mod at once.

## Settings

| Setting | Default | Description |
| --- | --- | --- |
| `rowHeight` | `33` | Row height in pixels. `0` keeps the native height. Custom values are applied from `20` upward. |

Close and reopen the flyout after changing settings.

## Troubleshooting

- **The panel remains narrow after reboot:** check that version 0.1.8.3 is enabled and that there is only one active copy. If it persists, report the Windows build and whether reopening the flyout changes the result.
- **Layout or highlight problems:** temporarily disable other mods that alter hidden tray icon geometry and compare the result.
- **Windows update breaks the mod:** disable it in Windhawk. Restart Explorer if the original panel layout does not return.

When reporting a problem, include the mod version, Windows build, display scaling, other tray layout mods, reproduction steps, and a screenshot if useful.

## Source and validation

The repository contains one release source file. Version 0.1.8.3 is based on the user's confirmed stable 0.1.8.2. The release hides the right edge correction setting and fixes it at the installed value of 1 px. The default row height is now 33 px, matching the installed setting; row height remains configurable. Version 0.1.8.3 was subsequently tested and confirmed working by the user on 2026-10-17.

The source passes a syntax check using the locally installed Windhawk compiler. Runtime validation was performed by the user; this is not a claim of automated UI testing or compatibility with all Windows 11 builds.

See [CHANGELOG.md](CHANGELOG.md) for the release history and [NOTICE.md](NOTICE.md) for attribution.

## License

GPL-3.0-only. See [LICENSE](LICENSE). The source includes helpers derived from other GPL-licensed Windhawk tray mods; their existing attribution is retained.
