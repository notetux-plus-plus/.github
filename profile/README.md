<div align="center">

# Notetux++

**A native Linux port of Notepad++**

[![License: GPL-3.0](https://img.shields.io/badge/license-GPL--3.0-blue?style=flat-square)](https://github.com/notetux-plus-plus/notetux-plus-plus/blob/main/LICENSE)
[![Latest Release](https://img.shields.io/github/v/release/notetux-plus-plus/notetux-plus-plus?style=flat-square&label=release)](https://github.com/notetux-plus-plus/notetux-plus-plus/releases/latest)
[![Build](https://img.shields.io/github/actions/workflow/status/notetux-plus-plus/notetux-plus-plus/build.yml?style=flat-square&label=build)](https://github.com/notetux-plus-plus/notetux-plus-plus/actions)
[![Platform](https://img.shields.io/badge/platform-Linux-blue?style=flat-square&logo=linux&logoColor=white)](https://github.com/notetux-plus-plus/notetux-plus-plus)
[![Language](https://img.shields.io/badge/language-C11-blue?style=flat-square&logo=c&logoColor=white)](https://github.com/notetux-plus-plus/notetux-plus-plus)
[![GTK](https://img.shields.io/badge/UI-GTK3-4a86c8?style=flat-square)](https://gtk.org)
[![Ko-fi](https://img.shields.io/badge/donate-Ko--fi-ff5e5b?style=flat-square&logo=ko-fi&logoColor=white)](https://ko-fi.com/andreacoi)

Notetux++ brings the full Notepad++ experience to Linux — natively, without Wine, without
Electron, without Flatpak. Built in C11 on GTK3 with the same Scintilla editing engine and
Lexilla syntax-highlighting library that power the original.

</div>

---

## What is Notetux++

Notepad++ is the most widely used code editor on Windows. Notetux++ is its Linux counterpart:
same UI structure, same keyboard shortcuts, same plugin model — compiled as a native GTK3
application that integrates cleanly with your desktop, your package manager, and your system
fonts.

**No AppImage. No Flatpak. No Snap.** Native `.deb`, `.rpm`, `.pkg.tar.zst`, and `.apk`
packages for every major distribution.

---

## Features

| Category | What's included |
|----------|----------------|
| **Editor** | Scintilla engine · multi-tab · split view · word wrap · line numbers · folding · bookmarks · column editor · incremental search |
| **Syntax** | 80+ languages via Lexilla · User Defined Languages (NPP UDL format) · auto-complete · function list |
| **UI panels** | Document List · Folder as Workspace · Function List · Document Map · Search Results · Clipboard History · Character Panel · Project Manager |
| **Search** | Find/Replace · Find in Files · regex · mark · multi-select |
| **Coding tools** | Git gutter · spell checker (enchant, runtime loaded) · macro recorder · run commands |
| **Theming** | Full styler XML theme support · Style Configurator · dark/light icon sets |
| **I18n** | NPP localization XML format · system locale auto-detection |
| **Plugins** | Native `.so` plugin system · Plugins Admin with online catalogue |
| **Session** | Auto-save session · auto-backup · monitoring (tail -f) |

---

## Repositories

| Repo | Description | Release |
|------|-------------|---------|
| [notetux-plus-plus](https://github.com/notetux-plus-plus/notetux-plus-plus) | Main application | [![release](https://img.shields.io/github/v/release/notetux-plus-plus/notetux-plus-plus?style=flat-square&label=latest)](https://github.com/notetux-plus-plus/notetux-plus-plus/releases/latest) |
| [nppPluginList](https://github.com/notetux-plus-plus/nppPluginList) | Plugin catalogue | — |
| [hello_world](https://github.com/notetux-plus-plus/hello_world) | HelloPlugin | [![release](https://img.shields.io/github/v/release/notetux-plus-plus/hello_world?style=flat-square&label=latest)](https://github.com/notetux-plus-plus/hello_world/releases/latest) |
| [npp_ftp](https://github.com/notetux-plus-plus/npp_ftp) | NppFTP | [![release](https://img.shields.io/github/v/release/notetux-plus-plus/npp_ftp?style=flat-square&label=latest)](https://github.com/notetux-plus-plus/npp_ftp/releases/latest) |
| [compare](https://github.com/notetux-plus-plus/compare) | Compare | [![release](https://img.shields.io/github/v/release/notetux-plus-plus/compare?style=flat-square&label=latest)](https://github.com/notetux-plus-plus/compare/releases/latest) |
| [json_viewer](https://github.com/notetux-plus-plus/json_viewer) | JSON Viewer | [![release](https://img.shields.io/github/v/release/notetux-plus-plus/json_viewer?style=flat-square&label=latest)](https://github.com/notetux-plus-plus/json_viewer/releases/latest) |

---

## Plugin ecosystem

The plugin system follows the same ABI as Notepad++ (five mandatory C exports), adapted for
Linux `.so` files. Plugins are listed in the
[nppPluginList](https://github.com/notetux-plus-plus/nppPluginList) catalogue and installable
directly from **Plugins → Plugins Admin**.

| Plugin | Description | Status | Release |
|--------|-------------|--------|---------|
| [HelloPlugin](https://github.com/notetux-plus-plus/hello_world) | Minimal reference plugin — starting point for developers | ✅ Released | [![release](https://img.shields.io/github/v/release/notetux-plus-plus/hello_world?style=flat-square&label=)](https://github.com/notetux-plus-plus/hello_world/releases/latest) |
| [NppFTP](https://github.com/notetux-plus-plus/npp_ftp) | Remote file editing over FTP · SFTP · SCP | 🚧 In development | — |
| [Compare](https://github.com/notetux-plus-plus/compare) | Side-by-side visual diff with scroll-lock | 🚧 In development | — |
| [JSON Viewer](https://github.com/notetux-plus-plus/json_viewer) | Interactive JSON tree · format · minify · validate | 🚧 In development | — |

All plugin `.so` files are compiled on Ubuntu 20.04 (glibc 2.31) and run unchanged on any
distro that can run Notetux++.

---

## Roadmap

### Application

| Milestone | Status |
|-----------|--------|
| Core editor (Scintilla + Lexilla + GTK3) | ✅ Done |
| Multi-tab, session, auto-backup | ✅ Done |
| Find/Replace, Find in Files | ✅ Done |
| All UI panels (Document Map, Function List, Workspace…) | ✅ Done |
| Plugin system + Plugins Admin | ✅ Done |
| Spell checker (enchant runtime) | ✅ Done |
| Git gutter, macro recorder, run commands | ✅ Done |
| Clipboard History, Character Panel, Project Manager | ✅ Done |
| Native distro packages (.deb · .rpm · .pkg.tar.zst · .apk) | ✅ Done |
| **Vim mode** (Normal / Insert / Visual) | 🔲 Planned |
| **Embedded terminal panel** | 🔲 Planned |

### Plugins

| Plugin | Milestone | Status |
|--------|-----------|--------|
| HelloPlugin | v1.0 — reference implementation | ✅ Done |
| NppFTP | v0.1 — SFTP browser + transparent save | 🔲 Planned |
| Compare | v0.1 — line diff + scroll-lock | 🔲 Planned |
| JSON Viewer | v0.1 — tree panel + format/minify | 🔲 Planned |

---

## Installation

### Pre-built packages

Download the package for your distro from the
[latest release](https://github.com/notetux-plus-plus/notetux-plus-plus/releases/latest):

```sh
# Debian / Ubuntu / Mint
sudo dpkg -i notetux++_<version>_amd64.deb

# Fedora / RHEL / openSUSE
sudo rpm -i notetux++-<version>.x86_64.rpm

# Arch / Manjaro
sudo pacman -U notetux++-<version>-x86_64.pkg.tar.zst

# Alpine
sudo apk add --allow-untrusted notetux++-<version>.apk
```

### Build from source

```sh
git clone https://github.com/notetux-plus-plus/notetux-plus-plus.git
cd notetux-plus-plus
cmake -B build && cmake --build build
./build/notetux++
```

**Requirements:** CMake 3.20+, GCC (C11/C++17), GTK3 development headers.

---

## Contributing

- **Application bugs and features** → [notetux-plus-plus](https://github.com/notetux-plus-plus/notetux-plus-plus/issues)
- **Plugin catalogue** → [nppPluginList](https://github.com/notetux-plus-plus/nppPluginList)
- **Plugin development** → fork the relevant plugin repo; use [HelloPlugin](https://github.com/notetux-plus-plus/hello_world) as a starting point

All code is C11. Follow the GTK3 patterns established in the main source tree (no `gtk_dialog_run` loops, persistent singleton dialogs, `response` signal + `gtk_widget_hide`).

---

## Support the project

If Notetux++ saves you time, consider buying me a coffee.

[![Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/andreacoi)

---

## License

Notetux++ is released under the [GNU General Public License v3.0](https://github.com/notetux-plus-plus/notetux-plus-plus/blob/main/LICENSE).
Scintilla and Lexilla are vendored under their own licenses (see `scintilla/License.txt` and `lexilla/License.txt`).
