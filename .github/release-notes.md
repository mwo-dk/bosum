Bosum is a two-pane file manager in the Norton Commander tradition. The terminal app shows git status in every panel, and the desktop app adds tabs, a sidebar, previews and themes. Both share Everything-style instant search.

## Download

Every file comes from this release's **Assets** list below.

| You have | Desktop app | Terminal app |
|---|---|---|
| Windows 10/11 | `Bosum_…_x64-setup.exe` (or the `.msi`) | `bosum-terminal-…-x86_64-pc-windows-msvc.zip` |
| Mac with Apple Silicon (M1 or newer) | `Bosum_…_aarch64.dmg` | `bosum-terminal-…-aarch64-apple-darwin.tar.gz` |
| Mac with Intel | `Bosum_…_x64.dmg` | `bosum-terminal-…-x86_64-apple-darwin.tar.gz` |
| Linux (Debian, Ubuntu) | `Bosum_…_amd64.deb` | `bosum-terminal-…-x86_64-unknown-linux-musl.tar.gz` |
| Linux (Fedora, openSUSE) | `Bosum-…x86_64.rpm` | same as above |
| Linux (any distro) | `Bosum_…_amd64.AppImage` | same; `aarch64-…` for ARM |

The terminal app is a single file named `bosum` (`bosum.exe` on Windows). Put it anywhere on your `PATH`.

## The apps are not code-signed

Bosum is free, and the builds are not signed with a paid certificate, so your system warns you the first time:

- **Windows:** SmartScreen says "Windows protected your PC". Click **More info**, then **Run anyway**.
- **macOS:** the app "can't be opened" or "is damaged". Drag Bosum to Applications first, then run this once in Terminal:
  `xattr -cr /Applications/Bosum.app`. Do the same for the terminal app's `bosum` file.
- **Linux:** no warning. Make the AppImage executable (`chmod +x`) and run it.

## Build it yourself

You can build from source instead:

```sh
git clone https://github.com/mwo-dk/bosum.git
cd bosum
./install/install.sh          # Linux or macOS
```

On Windows:

```powershell
git clone https://github.com/mwo-dk/bosum.git
cd bosum
powershell -ExecutionPolicy Bypass -File install\install.ps1
```

The script offers to install Rust and Node.js if they are missing, and it asks before it does. See [INSTALL.md](https://github.com/mwo-dk/bosum/blob/master/install/INSTALL.md) for details.

Git glyphs and file icons need a [Nerd Font](https://www.nerdfonts.com).
