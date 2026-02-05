# Cradio/Ferris Sweep ZMK Keymap

A 34-key split keyboard layout optimized for macOS with Ukrainian language support.

## Features

- **Home row mods** - Modifiers on home row for comfortable typing
- **Calculator-style numpad** - Numbers arranged like a calculator on the raise layer
- **Paired brackets** - Opening and closing brackets aligned vertically
- **Ukrainian support** - Quick access to х, ї, ж letters via hold-taps and combos
- **macOS integration** - Screenshots, media controls, brightness

## Layers

### Base Layer (QWERTY)

```
╭───────┬───────┬───────┬───────┬───────╮   ╭───────┬───────┬───────┬───────┬───────╮
│   Q   │   W   │   E   │   R   │   T   │   │   Y   │   U   │   I   │   O   │ P/[   │
├───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┤
│ A/SFT │ S/ALT │ D/CTL │ F/GUI │   G   │   │   H   │ J/GUI │ K/CTL │ L/ALT │ '/SFT │
├───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┤
│ Z/FN  │   X   │   C   │   V   │   B   │   │   N   │   M   │   ,   │  ./]  │   /   │
╰───────┴───────┴───────┼───────┼───────┤   ├───────┼───────┼───────┴───────┴───────╯
                        │TAB/LWR│ ENTER │   │ SPACE │BSP/RSE│
                        ╰───────┴───────╯   ╰───────┴───────╯
```

**Home Row Mods:**
- Left hand: A=Shift, S=Alt, D=Ctrl, F=Cmd
- Right hand: J=Cmd, K=Ctrl, L=Alt, '=Shift

**Special Keys:**
- Hold Z → F-keys layer
- Hold P → `[` (Ukrainian х)
- Hold `.` → `]` (Ukrainian ї)

---

### Lower Layer (Symbols) - Hold TAB

```
╭───────┬───────┬───────┬───────┬───────╮   ╭───────┬───────┬───────┬───────┬───────╮
│   `   │   ~   │   !   │   @   │   #   │   │   $   │   %   │   ^   │   &   │   *   │
├───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┤
│   |   │   <   │   {   │   [   │   (   │   │   :   │       │       │       │   ;   │
├───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┤
│   \   │   >   │   }   │   ]   │   )   │   │   -   │   +   │   =   │   _   │   /   │
╰───────┴───────┴───────┼───────┼───────┤   ├───────┼───────┼───────┴───────┴───────╯
                        │  ▼▼▼  │       │   │       │       │
                        ╰───────┴───────╯   ╰───────┴───────╯
```

**Design Notes:**
- Brackets are paired vertically: `{` above `}`, `[` above `]`, `(` above `)`
- Angle brackets `<` `>` next to curly brackets
- Math operators on the right bottom row

---

### Raise Layer (Numbers + Nav) - Hold BACKSPACE

```
╭───────┬───────┬───────┬───────┬───────╮   ╭───────┬───────┬───────┬───────┬───────╮
│   *   │   1   │   2   │   3   │   -   │   │  SS4  │  SS5  │ MUTE  │ VOL-  │ VOL+  │
├───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┤
│   /   │   4   │   5   │   6   │   +   │   │   ←   │   ↓   │   ↑   │   →   │       │
├───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┤
│   .   │   7   │   8   │   9   │   0   │   │ HOME  │ PGDN  │ PGUP  │  END  │       │
╰───────┴───────┴───────┼───────┼───────┤   ├───────┼───────┼───────┴───────┴───────╯
                        │       │  ESC  │   │       │  ▼▼▼  │
                        ╰───────┴───────╯   ╰───────┴───────╯
```

**Left Side - Calculator Numpad:**
- Numbers 1-9, 0 arranged like a calculator
- Operators: `*`, `/`, `-`, `+`, `.`

**Right Side - Navigation & Media:**
- Arrow keys on home row (Vim-style HJKL positions)
- Home/End, Page Up/Down on bottom row
- Screenshots: SS4 = Cmd+Shift+4, SS5 = Cmd+Shift+5
- Volume controls on top row

---

### Tri Layer (System) - Hold BOTH Thumbs

```
╭───────┬───────┬───────┬───────┬───────╮   ╭───────┬───────┬───────┬───────┬───────╮
│ RESET │BOOTLDR│       │       │       │   │       │       │       │BOOTLDR│ RESET │
├───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┤
│  BT0  │  BT1  │  BT2  │  BT3  │  BT4  │   │       │       │       │       │       │
├───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┤
│BT CLR │       │       │       │       │   │       │       │       │       │       │
╰───────┴───────┴───────┼───────┼───────┤   ├───────┼───────┼───────┴───────┴───────╯
                        │  ▼▼▼  │       │   │       │  ▼▼▼  │
                        ╰───────┴───────╯   ╰───────┴───────╯
```

**Bluetooth:**
- BT0-BT4: Select Bluetooth profile
- BT CLR: Clear current profile pairing

**System:**
- RESET: Soft reset the keyboard
- BOOTLDR: Enter bootloader mode (for flashing)

---

### F-Keys Layer - Hold Z

```
╭───────┬───────┬───────┬───────┬───────╮   ╭───────┬───────┬───────┬───────┬───────╮
│  F1   │  F2   │  F3   │  F4   │  F5   │   │  F6   │  F7   │  F8   │  F9   │  F10  │
├───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┤
│ BRI-  │ BRI+  │ PREV  │ PLAY  │ NEXT  │   │       │       │       │  F11  │  F12  │
├───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┤
│  ▼▼▼  │       │       │       │       │   │       │       │       │       │       │
╰───────┴───────┴───────┼───────┼───────┤   ├───────┼───────┼───────┴───────┴───────╯
                        │       │       │   │       │       │
                        ╰───────┴───────╯   ╰───────┴───────╯
```

**macOS Media:**
- Brightness up/down
- Previous/Play-Pause/Next track

---

## Ukrainian Language Support

When using Ukrainian keyboard layout in macOS:

| Action | Output | Ukrainian Letter |
|--------|--------|------------------|
| Hold P | `[` | х |
| Hold `.` | `]` | ї |
| Combo O+P | `[` | х |
| Combo L+' | `;` | ж |

---

## Combos

| Keys | Output | Notes |
|------|--------|-------|
| O + P | `[` | Ukrainian х |
| L + ' | `;` | Ukrainian ж |

---

## Building & Flashing

### Automatic Build
Push to GitHub and download the firmware artifacts from the Actions tab.

### Flashing
1. Double-tap the reset button on the nice!nano (or use BOOTLDR key from tri-layer)
2. A USB drive named `NICENANO` will appear
3. Copy the appropriate `.uf2` file:
   - `cradio_left-nice_nano_v2.uf2` for left half
   - `cradio_right-nice_nano_v2.uf2` for right half
4. The keyboard will automatically reboot

---

## Hardware

- **Keyboard:** Cradio / Ferris Sweep (34 keys)
- **Controllers:** nice!nano v2
- **Firmware:** ZMK v0.3
