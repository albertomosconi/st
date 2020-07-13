# Custom build of the ST terminal
St is a simple terminal implementation for X. Configuration is done with config.h. Read the comments in the generated config.h to edit it according to your needs. Defaults are stored in config.def.h. Checkout the [suckless](https://st.suckless.org "st suckless.org website") website for the original source code.  

I also took some inspiration from [Luke Smith's build](https://www.github.com/lukesmithxyz/st "luke smith's build")

## Patches
- [Externalpipe](https://st.suckless.org/patches/externalpipe "externalpipe")
Reading and writing st's screen through a pipe.
- [Scrollback](https://st.suckless.org/patches/scrollback "scrollback")
Scroll back through terminal output using alt+j and alt+k.
- [Alpha](https://st.suckless.org/patches/alpha "alpha")
This patch allows users to change the opacity of the background. Note that you need an X composite manager (e.g. compton, xcompmgr) to make this patch effective.
- [Xresources](https://st.suckless.org/patches/xresources "xresources")
This patch adds the ability to configure st via Xresources. At startup, st will read and apply the resources named in the resources[] array in config.h.
- [Ligatures](https://st.suckless.org/patches/ligatures "ligatures")
This patch adds proper drawing of ligatures. The code uses Harfbuzz library to transform original text of a single line to a list of glyphs with ligatures included.

## Installation
Clone this repository in whatever folder you want to keep the source code in, then go in the cloned directory and build the package:

```bash
  git clone https://www.github.com/albertomosconi/st
  cd st
  sudo make clean install
```

## Screenshots
![blue](https://raw.githubusercontent.com/albertomosconi/st/master/screens/blue.png "blue")
![nvim](https://raw.githubusercontent.com/albertomosconi/st/master/screens/nvim.png "blue")
