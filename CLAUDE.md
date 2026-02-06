# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Is

A ZMK firmware user configuration for a **Cradio/Ferris Sweep** 34-key split keyboard running on **nice!nano v2** controllers. This is NOT the ZMK firmware source — it's a personal keymap/config repo that the ZMK build system consumes.

## Building

There is no local build. Firmware is built automatically via GitHub Actions on push/PR. The workflow (`.github/workflows/build.yml`) delegates to the official ZMK build action (`zmkfirmware/zmk/.github/workflows/build-user-config.yml@v0.3`). Build artifacts (`cradio_left-nice_nano_v2.uf2` and `cradio_right-nice_nano_v2.uf2`) are downloadable from the Actions tab.

To trigger a build: push to the repo or open a PR.

## Key Files

- **`config/cradio.keymap`** — The keymap. This is the primary file you'll edit. Uses ZMK device tree syntax with 5 layers (BASE, LOWER, RAISE, TRI, FKEYS).
- **`config/cradio.conf`** — Kconfig settings (BT power, debounce timing, USB logging toggle).
- **`config/west.yml`** — ZMK dependency manifest (locked to v0.3).
- **`build.yaml`** — GitHub Actions build matrix defining board/shield combos.

## Keymap Architecture

The keymap uses several ZMK features that interact:

- **Home row mods** via `ht` hold-tap behavior (tap-preferred, 220ms): left ASDF = Shift/Alt/Ctrl/Cmd, right JKL' = Cmd/Ctrl/Alt/Shift. Defined with `HRML`/`HRMR` macros.
- **Tri-layer**: LOWER + RAISE held simultaneously activates TRI (system/BT layer) via `conditional_layers`.
- **Hold Z for F-keys layer** via `lt_z` (a separate hold-tap that activates layer 4).
- **Ukrainian letter support**: Two hold-tap behaviors (`ua_ze_kha` on P, `ua_yi` on `.`) and two combos (O+P → `[`, L+' → `;`) provide access to х, ї, ж when using Ukrainian OS layout.
- **macOS macros**: `mac_ss4` (Cmd+Shift+4) and `mac_ss5` (Cmd+Shift+5) for screenshots.

## Editing Conventions

- When modifying the keymap, keep the ASCII diagram comments in sync with the actual bindings. Also update `README.md` to reflect any keymap changes — it contains layer diagrams and feature descriptions that must stay consistent.
- Key positions are 0-indexed (0-33), left-to-right, top-to-bottom. Row 0: positions 0-9, Row 1: 10-19, Row 2: 20-29, Thumbs: 30-33.
- The `&trans` binding means "pass through to the layer below."
