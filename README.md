# Network Emergency Reset Tool

A small, standalone Windows utility (EXE) that helps recover from common network issues by performing a safe, automated reset of key network components: releasing and renewing IP, flushing DNS, resetting TCP/IP and Winsock, removing saved Wi-Fi profiles, clearing ARP cache, and refreshing NetBIOS name caches.

> **Important:** This tool is intended for emergency troubleshooting only. Running it will remove saved Wi-Fi profiles and may cause you to lose access to networks if you don't remember credentials.

## Features
- Releases and renews IPv4/IPv6 addresses
- Flushes the DNS resolver cache
- Resets TCP/IP stack and Winsock catalog
- Deletes all saved Wi-Fi profiles (removes SSIDs from the PC)
- Clears ARP cache and refreshes NetBIOS name caches
- Runs with elevated (administrator) privileges
- Displays native Windows confirmation dialogs before making changes

## Usage
1. Download the latest `NetworkReset.exe` from the Releases page.
2. Right-click and choose **Run as administrator**, or run from an elevated prompt.
3. Confirm the two warning dialogs:
   - First dialog explains the purpose and emergency-use restriction.
   - Second dialog contains additional warnings about Wi-Fi profile removal and system reboot recommendations.
4. If you accept, the tool will run the repair operations and show a completion message.

## Warning
- **DO NOT** run this tool if you do not remember your Wi-Fi password(s). All saved Wi-Fi profiles will be removed.
- Do not turn off or reboot your computer while the tool is running.
- Use only when you are experiencing network connectivity issues that cannot be resolved by simpler steps (restart router, reconnect Wi-Fi, check cables).

## Requirements
- Windows 7, 8, 10, 11 (64-bit or 32-bit)
- Administrator privileges to perform network resets

## Build / Source
This repository contains the original batch/PowerShell source used to create the executable along with build instructions. See `src/` for the script and `build.md` for packaging steps.

## License
Choose the license you prefer (e.g., MIT). This project is provided **as-is** without warranty. Use at your own risk.

## Support
If you encounter issues, open an issue on this repository and include:
- Windows version
- Steps you followed
- Exact output or error messages

