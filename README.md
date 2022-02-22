<p align=center>
  <img src="https://git.sr.ht/~shinyzenith/wayshot/blob/main/docs/assets/wayshot.png" alt=wayshot width=60%>
  <p align=center>A native screenshot tool for wlroots based compositors such as sway and river written in Rust. X11 support coming soon. </p>
  
  <p align="center">
  <a href="./LICENSE.md"><img src="https://img.shields.io/github/license/waycrate/wayshot?style=flat-square&logo=appveyor"></a>
  <img src="https://img.shields.io/badge/cargo-v1.0.0-green?style=flat-square&logo=appveyor">
  <img src="https://img.shields.io/github/issues/waycrate/wayshot?style=flat-square&logo=appveyor">
  <img src="https://img.shields.io/github/forks/waycrate/wayshot?style=flat-square&logo=appveyor">
  <img src="https://img.shields.io/github/stars/waycrate/wayshot?style=flat-square&logo=appveyor">
  </p>
</p>

# Usage:

**Note: The project is a WIP.**

Region Selection:

```bash
wayshot -s "$(slurp -f '%x %y %w %h')" > /tmp/image.png
```

Fullscreen:

```bash
wayshot > /tmp/image.png
```

Screenshot and copy to clipboard:

```bash
wayshot | wl-copy
```

Pick a hex color code, using ImageMagick:

```bash
wayshot -s "$(slurp -p -f '%x %y %w %h')" | convert - -format '%[pixel:p{0,0}]' txt:-|egrep "#([A-Fa-f0-9]{6}|[A-Fa-f0-9]{3})" -o
```

Pick a color, using ImageMagick:

```bash
wayshot -s "$(slurp -p -f '%x %y %w %h')" | convert - -format '%[pixel:p{0,0}]' txt:-
```
# Installation

## AUR:
`wayshot-git` has been packaged. `wayshot-bin` will be released soon.

## Compile time dependencies:
-   rustup
-   make

## Compiling:
-   `git clone https://github.com/waycrate/wayshot && cd wayshot`
-   `make setup`
-   `make`
-   `sudo make install`

# Support server:
1. Use the mailing list.
1. I don't endorse the usage of discord but if you really need it, then you can join the following <a href="https://discord.gg/KKZRDYrRYW">server</a> for support.

# Smithay Developers:

Massive thanks to smithay developer <a href="https://github.com/cmeissl">Cmeissl</a> and <a href="https://github.com/vberger">Victor Berger</a>. Without them this project won't be possible as my wayland knowledge is limited.

# Contributors:

<a href="https://github.com/waycrate/wayshot/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=waycrate/wayshot" />
</a>

