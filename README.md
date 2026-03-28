---------------------03/28/2026---------------------

## Updated to build with the latest ZMK

This configuration has been updated to work with the current/latest ZMK build system.

### Build notes
- If you’re building via GitHub Actions, make sure your workflow is tracking the current ZMK (and its recommended `west`/module layout).
- If you’re building locally, re-run a clean build when updating ZMK (fresh `west update` + pristine build directory) to avoid stale artifacts.

> Tip: If a build suddenly breaks after pulling newer ZMK, the fix is often to wipe the build directory and re-run the build from scratch.

## Keymap: Miryoku-style layers (QWERTY base)

Layers have been added following the **Miryoku** approach with a **QWERTY** base layer.

- **Base**: QWERTY (Miryoku-inspired)
- **Added layers**: navigation, numbers, symbols, function/media (see keymap files for exact bindings)

If you’re using ZMK Studio, you can also adjust layer bindings at runtime without reflashing (within Studio’s supported capabilities).

## OLED: Battery indicator

The OLED battery indicator is expected to work with this updated configuration.

If the battery indicator does not show:
- Confirm the board/shield you’re building for has battery measurement enabled (battery/ADC fuel-gauge support varies by board).
- Confirm OLED is enabled for the target (and for split builds, that the side you expect to display battery has the relevant display + power/battery config).
- Rebuild from a pristine build directory after toggling any of the above.


---------------------03/05/2025---------------------

Adapted to zmk studio. (https://zmk.studio)

ZMK Studio provides runtime update functionality to ZMK powered devices, allowing users to change their keymap layers without flashing new firmware to their keyboards.

To learn more → https://zmk.dev/docs/features/studio.
