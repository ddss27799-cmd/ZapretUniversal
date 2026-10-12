# Zapret for Discord & YouTube (v1.10.3)
Требуется питон

A configuration package based on `winws` (Zapret) designed to bypass deep packet inspection (DPI) and restore access to Discord and YouTube on Windows.

---

## ⚠️ Important Prerequisites (Before You Start)

1. **Administrator Rights:** You must run all batch files (`.bat`) as an **Administrator**. Otherwise, `WinDivert` will fail to start.
2. **Antivirus Exceptions:** Windows Defender or third-party antivirus software may flag `WinDivert.dll` or `WinDivert64.sys` as false positives. You may need to add the folder to your antivirus exclusions.
3. **No Conflicts:** Ensure no other DPI bypass tools (like GoodbyeDPI or custom proxies) are running at the same time.

---

## 📁 File Structure & Purpose

*   `  Zapret.bat` — Launches the default console-based bypass method.
*   `  GUI.bat` — The main shortcut to launch the Graphical User Interface (located in the root folder for quick access).
*   `zapret_gui.py` — The core Python script responsible for managing the GUI window and settings.
*   `bin/` — Contains core binaries (`winws.exe`), driver files (`WinDivert`), and cryptographic TLS/QUIC templates.
*   `lists/` — Text files containing lists of blocked domains and filters (e.g., `list-general.txt`, `list-google.txt`).
*   `Strategy 1.bat` to `Strategy 13.bat` — Alternative pre-configured bypass combinations if the general methods do not work for your ISP.

---

## 🚀 How to Use

### Method 1: Using the Graphical Interface (Recommended)
1. Find `  GUI.bat` in the main folder.
2. Right-click it and select **"Run as administrator"**.
3. Use the interface to toggle features, apply presets, or adjust settings visually.

### Method 2: Console Presets
1. Right-click on `  Zapret.bat` (or `general.bat`).
2. Select **"Run as administrator"**.
3. Keep the console window open while using Discord or YouTube. Close it to stop the service.

### Method 3: Finding a Working Strategy
If the default preset does not restore your connection, your ISP might be using a stricter DPI filter.
1. Close any running presets or GUI windows.
2. Try alternative strategies (`Strategy 1.bat` through `Strategy 13.bat`).
3. Right-click the chosen strategy, select **"Run as administrator"**, and test your connection.

---

## ⚙️ Customization & User Lists

You can customize which websites are processed by editing the text files inside the `lists/` folder:
*   `list-general-user.txt` — Add custom domains you want to bypass here (one domain per line).
*   `list-exclude-user.txt` — Add domains that should **not** go through the bypass tool (whitelist).

---

## 🛠️ Troubleshooting

*   **Discord Voice/RTC Connecting Error:** Try switching between UDP strategies (look for scripts using `ACTIVE_DISCORD_UDP.bin`).
*   **WinDivert error 5 (Access Denied):** Make sure you strictly right-click and choose "Run as administrator" on the `.bat` file.
*   **GUI Not Opening:** Ensure your system has Python installed if you are modifying or running the `zapret_gui.py` script directly, though using `  GUI.bat` is highly recommended for standard users.
