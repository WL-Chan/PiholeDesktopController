# PiHole Desktop Controller

PiHole Desktop Controller is a lightweight desktop application designed to manage a Pi-hole server directly from a Windows computer without opening the web interface. It provides fast access to essential controls and a real-time log viewer through SSH.

---

## Features

### Live Log Viewer
Displays the output of `pihole -t` in real time with:
- Color-coded lines
- Query grouping
- Smart auto-scroll
- Automatic trimming to the latest 600 lines

### Enable / Disable Controls
- One-click "Enable"
- One-click "Disable for 10 minutes" with countdown timer
- Button automatically unlocks when the timer completes

### SSH-Based Operation
All commands are executed over SSH:
- No API keys required
- Simple configuration
- Automatic reconnection every 5 seconds if the connection fails

### Connection Handling
- Displays connection attempts and errors in the log window
- Reconnects automatically if SSH fails
- Keeps the live log viewer running once connected

---

## Planned Features

The following improvements are planned for future versions:
- Cross-platform support using Avalonia (Windows, macOS, Linux)
- Login screen with optional credential storage
- Support for custom SSH ports
- A simplified single-Pi-hole version for public use
- Optional Pi-hole API integration
- Improved UI layout and theme options

---

## Installation

Compiled builds will be provided in the GitHub Releases section.

For developers who want to build the project from source:

### Requirements
- .NET 8 SDK
- Visual Studio 2022 or JetBrains Rider
- SSH.NET (installed via NuGet)

### Build Instructions

git clone https://github.com/
<your-username>/PiHoleDesktopController
cd PiHoleDesktopController
dotnet build

---

## Security Notes

This application requires SSH credentials in order to control Pi-hole.  
Please note the following:

- Passwords are not stored unless the user explicitly enables the option.
- All actions are performed locally; nothing is transmitted externally.
- Users are responsible for securing their Pi-hole servers and SSH access.

---

## License

This project is licensed under the Apache License 2.0.  
Refer to the `LICENSE` file for full details.  
Refer to the `NOTICE` file for attribution requirements.

---

## Acknowledgements

Pi-hole is developed and maintained by the Pi-hole Team.  
https://pi-hole.net

SSH connectivity is provided by SSH.NET.  
https://github.com/sshnet/SSH.NET

---

## Contributing

Contributions and suggestions are welcome.  
Please open an issue to discuss potential changes before submitting a pull request.



