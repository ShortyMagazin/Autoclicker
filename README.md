About
ForgeClick is a desktop auto clicker for Windows. Set a click interval, choose a mouse button, automate one position or a sequence of points, and control the session with global hotkeys.

The interface uses a distinctive ForgeByte FB mouse logo and a bold, comic-inspired visual style. The released Windows executable is designed to run without a separate Python installation.
Features
- Adjustable click intervals: hours, minutes, seconds, and milliseconds.
- Mouse actions: left, right, or middle button, with single, double, or triple clicks.
- Click position: follow the cursor or use fixed screen coordinates.
- Multi-Point mode: create an ordered sequence of up to 100 click points, each with its own coordinates, button, click count, and delay.
- Click limits: run continuously, stop after a specified number of actions, or set a session time limit.
- Timing controls: optional start delay and randomized timing variation.
- Profiles: save and load frequently used configurations.
- Live statistics: click counter, current CPS, elapsed runtime, and completed cycles.
- Global hotkeys: start or toggle clicking without switching back to the app, and use a dedicated emergency stop.
- Branded desktop app: ForgeByte icon in the app window and Windows executable.
Note: Click timing depends on Windows scheduling and the target application. Very short intervals do not guarantee an exact CPS rate. Some applications and games may block simulated mouse input.

Download and installation
1. Open the project's Releases page on GitHub once a release has been published.
2. Download the Windows release ZIP (for example, ForgeClick_v4_Windows_Release.zip).
3. Extract the ZIP into a folder of your choice.
4. Run ForgeClick.exe.
System requirements:
- Windows 10 or Windows 11
- Microsoft Edge WebView2 Runtime
- A standard Windows desktop session
The published .exe includes the application runtime. End users do not need Python or Node.js.
Quick start
1. Open Auto clicker.
2. Choose the interval, mouse button, and click type.
3. Select Current cursor or Fixed position.
4. Press Start Auto Clicker, or use the default start hotkey.
5. Press F7 to stop an active session or cancel a delayed start.
Keyboard shortcuts
Shortcut	Action
F6	Start / stop Auto Clicker (default; configurable)
F7	Emergency stop


The start hotkey can be changed to another supported function key in the app.
Multi-Point automation
Open Multi-point, add coordinates and settings for each point, then choose Start Multi-Point. The sequence executes in order and can be stopped with F7.
Saving profiles
Use My profiles to save your current settings and Multi-Point list. Settings are stored locally at:
%APPDATA%\ForgeByte\ForgeClickNeon\settings.json
The ForgeClickNeon folder name is retained for compatibility with earlier versions.
Build the Windows EXE from source
This section is for developers. It is not required to run the published Windows release.

1. Install Python 3.10+ on a Windows development machine.
2. Download or clone the full ForgeClick source project.
3. Run BUILD_EXE.bat from the project folder.
4. When the build succeeds, find the executable at dist\ForgeClick.exe.
5. Distribute dist\ForgeClick_v4_Windows_Release.zip after testing it on Windows.
The build script installs dependencies and packages the application with PyInstaller in windowed, single-file mode. A network connection is required during the dependency installation step.

To run the development version instead, use DEV_RUN.bat.
Project structure
ForgeClick/
├── assets/
│   ├── ForgeClick.ico          # Windows application icon
│   ├── forgebyte-logo.png     # Full-size logo
│   └── forgebyte-logo-256.png # UI and README logo
├── web/
│   ├── index.html             # Interface
│   ├── styles.css             # Theme and animation
│   └── app.js                 # UI behavior
├── tests/                     # Application and engine tests
├── main.py                    # Desktop app and UI bridge
├── core.py                    # Windows mouse click engine
├── requirements.txt
├── version_info.txt           # Windows EXE metadata
├── DEV_RUN.bat                # Development launcher
└── BUILD_EXE.bat              # Windows release builder
Windows security and code signing
A newly built executable may be flagged or blocked by Windows protection features, especially if it is unsigned or has little download reputation. This is not proof that the file is malicious, but it should still be verified before use.

For a public release, ForgeByte should sign the EXE with a valid Windows code-signing certificate, publish builds through a consistent official channel, and test the release on a clean Windows system. Do not disable Windows security features just to run an untrusted executable.
Responsible use
ForgeClick uses native Windows mouse input. It does not guarantee compatibility with protected applications or games. Use it only where automation is permitted and follow the rules of any software or service you interact with.
Credits
Developed by ForgeByte.cz.

Comic-card visual component adapted from:
From Uiverse.io by chandrasek_6406
https://uiverse.io/chandrasek_6406/white-starfish-90
MIT License, Copyright (c) chandrasek_6406 (Chandu Icon)

This attribution applies to the adapted Uiverse component. The licensing terms for the rest of the ForgeClick project have not been specified in this README.
