# xi-gtk

a GTK+ front-end for the [Xi editor](https://github.com/google/xi-editor)

**This project is still in development and not yet ready to be used as your main text editor.**

![screenshot](screenshot.png)

## Features

- multiple cursors

## Download

## Development

## Instructions

### Build and Install xi-core

Make sure you have a recent version of [Rust](https://www.rust-lang.org) and Cargo installed (either from your distribution's repositories or with [rustup](https://rustup.rs)) and that `~/.cargo/bin` is in your `PATH` environment variable.

```sh
git clone https://github.com/google/xi-editor.git
cd xi-editor/rust
cargo install
```

### Build and Install xi-gtk

First you need to install the dependencies.

```sh
# Debian/Ubuntu:
sudo apt install build-essential valac meson libgtk-3-dev libjson-glib-dev
# Arch:
sudo pacman -S vala meson
# Fedora:
sudo dnf install meson vala gtk3-devel json-glib-devel
```

Once you have the dependencies installed you can build xi-gtk.

```sh
git clone https://github.com/eyelash/xi-gtk.git
cd xi-gtk
mkdir build
cd build
meson ..
ninja
```

Now you can either launch xi-gtk from the build directory with `./xi-gtk` or install it with `sudo ninja install`.

## Shortcuts

Shortcut                                         | Command
-------------------------------------------------|---------
<kbd>Control</kbd>+<kbd>N</kbd>                  | New File
<kbd>Control</kbd>+<kbd>O</kbd>                  | Open File
<kbd>Control</kbd>+<kbd>S</kbd>                  | Save
<kbd>Control</kbd>+<kbd>Shift</kbd>+<kbd>S</kbd> | Save As
<kbd>Control</kbd>+<kbd>Z</kbd>                  | Undo
<kbd>Control</kbd>+<kbd>Y</kbd>                  | Redo
<kbd>Control</kbd>+<kbd>Q</kbd>                  | Quit

## Roadmap

- [x] mouse input and selections
- [x] saving
- [x] follow the cursor (respect the `scrollto` parameter)
- [x] undo / redo
- [x] copy / paste
- [ ] line numbers
- [ ] find / replace
- [ ] i18n
- [ ] preferences (font family, font size, etc.)
