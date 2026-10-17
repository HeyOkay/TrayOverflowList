# Changelog

## 0.1.8.8

- Remove the DLL pin fallback; retain tray-thread cleanup retries without keeping the mod loaded after disabling it.
- Capture original row properties once, using indexed duplicate checks.
- Replace per-frame tree scans with event-driven updates and bounded layout follow-ups.
- Calculate width from the original native grid measurements without temporary reparenting or synchronous layout updates.
- Revoke collection, row, template, size, scroll, and layout callbacks before restoring native properties.
- Pass the upstream PR validator, full x64/ARM64 builds, and native/XAML integration checks.
- Tested and confirmed working by the user on 2026-10-17.

## 0.1.8.7

- Track flyout controls, rows, and labels weakly; prune expired entries and replace state for recreated flyouts.
- Revoke layout handlers before restoring properties; isolate restore failures, retry cleanup on the tray UI thread, and retain the module only if cleanup cannot finish.
- Reload on settings changes so row height 0 restores native dimensions.
- Use an English fallback label and remove unused image-source queries.
- Recalculate scroll height when reopening the flyout.
- Tested and confirmed working by the user on 2026-10-17.

## 0.1.8.6

- Add configurable, case-insensitive removal of `.Root`, `.App`, and `.Runner` at the end of tray labels.
- Keep the existing Windows name source; preserve internal dots and unknown endings.
- Allow an empty suffix setting to disable name cleanup.
- Keep right edge correction fixed at 1 px and the default row height at 33 px.
- Exclude intermediate diagnostic builds and EXE metadata collection from the release.
- Tested and confirmed working by the user on 2026-10-17.

## 0.1.8.3

- Tested and confirmed working by the user on 2026-10-17.

- Remove the right edge correction setting from the settings UI.
- Fix the correction at 1 px, matching the verified installed value.
- Set the default row height to 33 px, matching the installed setting; keep it configurable.
- Retain the confirmed stable 0.1.8.2 list and width behavior.
- Add English and Russian documentation, license, and attribution for publication.

## 0.1.8.2

- Re-measure the native tray grid when the number of hidden icons changes, so a narrow width captured while startup applications load does not remain fixed.
- Use existing layout events; no width-recalculation timers were added.
- Confirmed stable by the user on Windows 11 build 26300.9457.

## 0.1.8.1

- Fix missing labels on dragged tray icons, a regression introduced between 0.1.7 and 0.1.8.
- Confirmed working by the user.

Only the selected stable release source is included in this repository.
