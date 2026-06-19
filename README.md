# Patch34 — Duplicate selected items to next measure

A small REAPER Lua script that duplicates selected media items to the next measure instead of placing the duplicate directly after the item edge.

This is useful for one-shot samples, short sound design events, drums, and any editing situation where `Ctrl+D` should behave musically by measure rather than by item length.

## Behavior

- Duplicates every selected media item one measure forward.
- Keeps the same beat offset inside the following measure.
  - Item on beat 1 → duplicate on beat 1 of the next measure.
  - Item on beat 2 → duplicate on beat 2 of the next measure.
- Preserves item length, takes, fades, envelopes, item properties, and track.
- Respects REAPER's tempo map and time signature changes.
- Selects only the newly created duplicates after running.

## Installation

1. Download:

   `Patch34 - Duplicate selected items to next measure.lua`

2. In REAPER, open:

   `Actions` → `Show action list...`

3. Click:

   `New action...` → `Load ReaScript...`

4. Select the `.lua` file.

5. Find the script in the Action List:

   `Duplicate selected items to next measure`

6. Assign a shortcut, for example `Ctrl+D`.

If REAPER asks whether to remove `Ctrl+D` from the default duplicate action, confirm it if you want this script to replace the default behavior.

## Notes

This script is different from REAPER's default `Item: Duplicate items` action. The default action places the duplicate immediately after the selected item's end. This script places the duplicate one measure later relative to the item's start position.

## Author

Patch34  
https://github.com/patch-34
