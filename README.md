# My build of st - the simple (suckless) terminal

The [suckless terminal (st)](https://st.suckless.org/) with some additional features that make it literally the best terminal emulator ever:

## Unique features (using dmenu)

- **follow urls** by pressing `alt-l`
- **copy urls** in the same way with `alt-y`
- **copy the output of commands** with `alt-o`

## Bindings for

- **scrollback** with `alt-↑/↓` or `alt-pageup/down` or by scrolling the mouse-wheel
- OR **vim-bindings**: scroll up/down in history with `alt-k` and `alt-j`. Faster with `alt-u`/`alt-d`.
- **zoom/change font size**: same bindings as above, but holding down shift as well. `alt-home` returns to default
- **copy text** with `alt-c`, **paste** is `alt-v` or `shift-insert`

## Pretty stuff

- Compatibility with `Xresources`.
- Default color scheme is set to [dracula](https://draculatheme.com) colors, `Xresources`-colors otherwise.
- Transparency/alpha, which is also adjustable from your `Xresources`.
- Default font is set to [Iosevka SS07](https://github.com/be5invis/iosevka) at 13pt. Don't forget to install the font or override the font in `Xresources`.

## Applied st patches

- [alpha](https://st.suckless.org/patches/alpha/)
- [anysize](https://st.suckless.org/patches/anysize/)
- [clipboard](https://st.suckless.org/patches/clipboard/)
- [dracula](https://st.suckless.org/patches/dracula/)
- [externalpipe](https://st.suckless.org/patches/externalpipe/)
- [font2](https://st.suckless.org/patches/font2/)
- [ISO 14755](https://st.suckless.org/patches/iso14755/)
- [scrollback](https://st.suckless.org/patches/scrollback/)
- [vertcenter](https://st.suckless.org/patches/vertcenter/)
- [xresources](https://st.suckless.org/patches/xresources/)
- updated to latest version 0.8.2

## Installation

```
git clone https://github.com/tristan-zeven/st.git
cd st
sudo make install
```

## How to configure dynamically with Xresources

For many key variables, this build of `st` will look for X settings set in either `~/.Xdefaults` or `~/.Xresources`. You must run `xrdb` on one of these files to load the settings.
For example, you can define your desired fonts, transparency or colors:

```
*.font:	Liberation Mono:pixelsize=12:antialias=true:autohint=true;
*.alpha: 0.9
*.color0: #111
...
```

The `alpha` value (for transparency) goes from `0` (transparent) to `1` (opaque).

### Colors

To be clear about the color settings:

- This build will use dracula colors by default and as a fallback.
- If there are `Xresources` colors defined, those will take priority.

## Contact

- Tristan Zeven <tristan@unshift.nl>
