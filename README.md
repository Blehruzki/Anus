<div align="center">

# anus
Another NSP Updater, Super (for [Skyline](https://github.com/skyline-emu/skyline))

**Consider starring 🌟 the project if it helped**

</div align="center">

---

## About

**Anus** is a **Nintendo Switch** ROM patcher made to be compatible with Skyline. The supported platforms currently consist of **Linux**, **Android w/Termux** and **Windows**.

The software is to act as sort-of a band-aid until Skyline supports Updates/DLCs natively.

> **Note:** doesn't support DLCs yet.

Precompiled binaries are available from the [GitHub releases page](https://github.com/nozwock/yanu/releases).

## Features
- [x] NSP updates
- [ ] XCI updates
- [ ] NSZ updates

> **Note:** I might or might not add the features marked as unticked above.

## Installation

### Android w/Termux

1. Download & Install `Termux` from [F-droid](https://f-droid.org/en/packages/com.termux/).
2. Copy-pasta this and press enter:
  ```console
  pkg upgrade -y && pkg in clang make binutils git -y && curl -sLo "$PATH/yanu" https://github.com/nozwock/yanu/releases/latest/download/yanu-aarch64-linux-android && chmod +x "$PATH/yanu" && termux-setup-storage && echo -e "\e[;92mInstalled yanu successfully\nRun it by typing in\n\e[0m\e[;96myanu\e[0m" || echo -e "\e[;91mInstallation failed\e[0m"
  ```

> MiXplorer [XDA Forum](https://forum.xda-developers.com/t/app-2-2-mixplorer-v6-x-released-fully-featured-file-manager.1523691/)</br>
> MiXplorer GDrive [download link](https://drive.google.com/drive/folders/1BfeK39boriHy-9q76eXLLqbCwfV17-Gv)

### Linux

1. Make sure dependencies required to build hactool/hacPack are installed on your system
   ```console
   git gcc make binutils
   ```
2. Download & give executable permission to `yanu` from the console or file manager
   ```console
   chmod +x yanu-x86_64-unknown-linux-musl
   ```

### Windows

- Just [download](https://github.com/nozwock/yanu/releases) & run.

> Some AVs might false positively flag the program tho, deal with it.</br>
> Use these if you're paranoid ig :weary: -
> - https://www.virustotal.com
> - https://www.hybrid-analysis.com 

## Usage (CLI only)

- View CLI help with:
```sh
yanu --help
```

- For updating a ROM using CLI:
```sh
yanu cli --keyfile /path/to/keyfile --base /path/to/base --update /path/to/base
```

- Set new `roms_dir` with (Android only):
```sh
yanu config --roms-dir /new/path/here
```

---

Credits to [hactool](https://github.com/SciresM/hactool) and [hacPack](https://github.com/The-4n/hacPack).</br>
Used [Willfaust's script](https://gist.github.com/willfaust/fb90dec409b8918290012031f09a78ef) for reference.
