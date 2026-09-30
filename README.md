# Vaultstrap 🔐

A simple, customizable **Roblox bootstrapper** for Windows.
Free, open source, no ads, no telemetry.

> **Not affiliated with Roblox Corporation.** Vaultstrap is an independent
> project inspired by [Bloxstrap](https://github.com/pizzaboxer/bloxstrap).

![screenshot](screenshot.png)

---

## Features

- ✅ **Automatic Roblox detection** — finds your installed `RobloxPlayerBeta.exe`
- ✅ **One-click launch** — starts the client without freezing the UI
- ✅ **Modern interface** — dark / light mode, built with CustomTkinter
- ✅ **Manifest reader** — parses the official Roblox package manifest (22 packages)
- ✅ **Integrity check** — verifies MD5 hashes of downloaded files
- ✅ **Single `.exe`** — no Python required on the target machine

### Roadmap

- 🚀 Automatic download & extraction of all 22 packages
- 🚀 FastFlags editor (FPS unlock, rendering, ...)
- 🚀 Mods system (replace game files)
- 🚀 Multi-instance launcher
- 🚀 Discord Rich Presence
- 🚀 Auto-updates

---

## Download

➡️ **[Get the latest release](../../releases)** → `Vaultstrap.exe` (~10 MB)

- Windows 10 / 11 (64-bit)
- Python **not** required

> ⚠️ **Windows SmartScreen warning**
> Windows may show *"Windows protected your PC"* when you run the exe.
> Click **More info → Run anyway**. This is normal for unsigned executables.

---

## Building from source

```bash
git clone https://github.com/<your-username>/Vaultstrap.git
cd Vaultstrap

python -m venv .venv
.venv\Scripts\pip install -r requirements.txt

py screen.py
```

### Creating the executable

```bash
.venv\Scripts\python.exe -m PyInstaller --onefile --windowed ^
  --name Vaultstrap ^
  --icon=icone.ico ^
  --add-data "icone.ico;." ^
  --add-data "icons;icons" ^
  screen.py
```

The result is located in `dist\Vaultstrap.exe`.

> Note: on PowerShell / bash use `\` instead of `^` for line continuation.

---

## Project structure

| File | Description |
|---|---|
| `screen.py` | User interface (entry point) |
| `app.py` | Core logic (Roblox detection) |
| `icons/` | UI icons |
| `icone.ico` | Application icon |
| `Vaultstrap.spec` | PyInstaller build config |
| `requirements.txt` | Python dependencies |

---

## Contributing

Issues and pull requests are welcome.

1. Fork the repository
2. Create a feature branch: `git checkout -b my-feature`
3. Commit your changes: `git commit -m "Add my feature"`
4. Open a pull request

## License

Released under the [MIT License](LICENSE).
