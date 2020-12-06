# siddwm (Siddwm Is Dumb Dumb Window Manager)

## Default Keybindings

**Window Management**

| combo                           | action                 |
| ------------------------------- | ---------------------- |
| `Mouse`                         | focus under cursor     |
| `MOD4` + `Left Mouse`           | move window            |
| `MOD4` + `Right Mouse`          | resize window          |
| `MOD4` + `Shift` + `Right/Left` | inc/dec window width   |
| `MOD4` + `Shift` + `Down/Up`    | inc/dec window height  |
| `MOD4` + `f`                    | maximize toggle        |
| `MOD4` + `c`                    | center window          |
| `MOD4` + `q`                    | close window           |
| `MOD4` + `Shift` + `q`          | kill program           |
| `MOD4` + `1-9`                  | desktop swap           |
| `MOD4` + `Shift` +`1-9`         | send window to desktop |
| `MOD1` + `TAB` (*alt-tab*)      | focus cycle            |

**Programs**

| combo                    | action           | program        |
| ------------------------ | ---------------- | -------------- |
| `MOD4` + `Return`        | terminal         | `kitty`        |
| `MOD4` + `d`             | dmenu            | `rofi`         |
| `MOD4` + `p`             | scrot            | `scrot`        |
| `MOD4` + `w`             | browser          | `firefox`      |
| `XF86_AudioLowerVolume`  | volume down      | `amixer`       |
| `XF86_AudioRaiseVolume`  | volume up        | `amixer`       |
| `XF86_AudioMute`         | volume toggle    | `amixer`       |
| `XF86_MonBrightnessUp`   | brightness up    | `xbacklight`   |
| `XF86_MonBrightnessDown` | brightness down  | `xbacklight`   |
| `MOD4` + `Shift` + `w`   | wallpaper cycler | `wllppr`       |
| `MOD4` + `s`             | status           | `status`       |

## Dependencies
- Xlib

## Installation

1) Copy `config.def.h` to `config.h` and modify it to suit your needs.
2) Run `make` to build `siddwm`.
3) Copy it to your path or run `make install`.
    - `DESTDIR` and `PREFIX` are supported.
4) (Optional) Apply patch with `git apply patches/patch-name`
    - In case of applying multiple patches, it has to be done **manually**.

If you are using GDM, save the following to `/usr/share/xsessions/siddwm.desktop`. It is still recommended to start `siddwm` from `.xinitrc` or through
[your own xinit implementation](https://github.com/dylanaraps/bin/blob/dfd9a9ff4555efb1cc966f8473339f37d13698ba/x).

```
[Desktop Entry]
Name=siddwm
Comment=This session runs siddwm as desktop manager
Exec=siddwm
Type=Application
```
