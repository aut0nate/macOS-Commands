# macOS Commands & Tools Cheatsheet

![macOS](https://img.shields.io/badge/mac%20os-000000?style=for-the-badge&logo=macos&logoColor=F0F0F0)

This repository contains a collection of macOS commands and tools that I’ve found particularly useful as part of my learning process. I have grouped this into categories for easy reference.

---

## Contents

- [Managing Files](#managing-files)
- [Software Management](#software-management)
- [Process Management](#process-management)
- [System Management](#system-management)
- [Network Management](#network-management)
- [Command Line Tools](#command-line-tools)

## Managing Files

```bash
# Opens files or folders using the default application.
open <file/folder>

# Enhanced copy command that preserves file attributes and can copy directories recursively.
ditto <source> <destination>

# Copies the output of a command to the clipboard.
<command> | pbcopy
```

## Software Management

```bash
# Checks for the latest available software updates.
softwareupdate -l

# Installs all available software updates and restarts the system after installation.
softwareupdate -iaR
```

## Process Management

```bash
# Displays a list of processes that are using internet connections.
lsof -P -i -n | cut -f 1 -d " " | uniq
```

## System Management

```bash
# Displays software version information.
sw_vers

# Displays detailed system information including software and hardware details.
system_profiler SPSoftwareDataType SPHardwareDataType

# Displays available data types that can be queried using the system_profiler command.
system_profiler -listDataTypes

# Displays detailed system security information (requires sudo privileges).
sudo /usr/libexec/mdmclient QuerySecurityInfo

# Displays detailed system device information (requires sudo privileges).
sudo /usr/libexec/mdmclient QueryDeviceInformation

# Prevents the Mac from sleeping for as long as the command is running.
caffeinate

# Configures sudo to use Touch ID for authentication.
sudo touch id
```

[⬆ ʀᴇᴛᴜʀɴ ᴛᴏ ᴄᴏɴᴛᴇɴᴛꜱ](#contents)

## Network Management

```bash
# Display network interface configuration, including IP addresses and status.
ifconfig

# Display the current IP address assigned to the network interface
ipconfig getifaddr en0

# Display the upload and download speed of the network connection.
networkQuality

# Retrieve saved Wi-Fi passwords for a specified network (requires password entry).
security find-generic-password -wa <WiFi_SSID>
```

## Command Line Tools

- **[iTerm2:](https://iterm2.com/)** A terminal emulator for macOS.
- **[Homebrew:](https://brew.sh/)** The missing package manager for macOS.
- **[OhMyZsh:](https://ohmyz.sh/)** Oh My Zsh is a framework for managing your Zsh configuration.
