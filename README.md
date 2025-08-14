# FluxOS

<div align="center">
  <img src="https://github.com/berkucuk/FluxOS/blob/main/fluxos-logo.png?raw=true" alt="FluxOS Logo" width="400"/>
  
  **Modern, Secure and User-Friendly Arch Linux Based Operating System**
  
  [![Build Status](https://img.shields.io/badge/build-passing-brightgreen)](https://github.com/berkkucukk/fluxos)
  [![License](https://img.shields.io/badge/license-GPL--3.0-blue)](LICENSE)
  [![Arch Linux](https://img.shields.io/badge/based%20on-Arch%20Linux-1793d1)](https://archlinux.org)
  [![KDE Plasma](https://img.shields.io/badge/desktop-KDE%20Plasma-blue)](https://kde.org/plasma-desktop/)
</div>

## 📖 Table of Contents

- [About](#-about)
- [Features](#-features)
- [System Requirements](#-system-requirements)
- [Installation](#-installation)
  - [ISO Download](#iso-download)
  - [Creating Bootable USB](#creating-bootable-usb)
  - [Installation Steps](#installation-steps)
- [Calamares Installer](#-calamares-installer)
- [Pre-installed Applications](#-pre-installed-applications)
- [FluxAI Chat](#-fluxai-chat)
- [Custom SDDM Theme](#-custom-sddm-theme)
- [Security Features](#-security-features)
- [Development](#-development)
- [Contributing](#-contributing)
- [Support](#-support)
- [License](#-license)

## 🚀 About

FluxOS is a modern, secure and user-friendly operating system based on Arch Linux. Designed for both beginners and advanced users, FluxOS combines the powerful Arch Linux infrastructure with an easy installation and usage experience.

## ✨ Features

### 🎨 Desktop Environment
- **KDE Plasma Desktop** - Modern, customizable desktop environment
- **Custom SDDM Theme** - FluxOS branded login screen
- **Beautiful Wallpapers** - Custom designs that complement the system

### 🔧 System Features
- **Arch Linux Based** - Latest package updates and rolling release model
- **UEFI and BIOS Support** - Works on modern and legacy systems
- **Multi Filesystem Support** - ext4, btrfs, xfs, f2fs and more
- **LUKS Disk Encryption** - Full disk encryption for security
- **Calamares Installer** - Offline installation support

### 🛡️ Security
- **ClamAV Antivirus** - Built-in security scanning
- **Firewalld** - Advanced firewall management
- **Tor Browser** - Anonymous web browsing
- **OnionShare** - Secure file sharing

### 🔌 Network and Connectivity
- **NetworkManager** - Easy network management
- **BlueZ** - Bluetooth support
- **WireGuard** - Modern VPN technology
- **KDE Connect** - Mobile device integration

### 🎯 Custom Applications
- **FluxAI Chat** - PyQt5-based AI assistant (Google Gemini integration)
- **Custom Archinstall** - FluxOS branded installation tool

## 💻 System Requirements

### Minimum Requirements
- **Processor**: 64-bit x86_64 processor
- **RAM**: 2 GB (4 GB recommended)
- **Storage**: 20 GB free disk space
- **UEFI/BIOS**: UEFI or Legacy BIOS support
- **Network**: Internet connection (for post-installation updates)

### Recommended Requirements
- **Processor**: Multi-core 64-bit processor
- **RAM**: 8 GB or more
- **Storage**: 50 GB+ SSD
- **Graphics**: Modern GPU (Intel/AMD/NVIDIA)

## 🔽 Installation

### ISO Download

You can download the FluxOS ISO file from Google Drive:

**📥 Download Link:** [FluxOS ISO - Google Drive](https://drive.google.com/drive/folders/1HW3jsPIsAfc14sPSyx1frohGKV81qnwQ?usp=sharing)

#### Download Steps:
1. Click on the Google Drive link above
2. Find the latest `fluxos-YYYY.MM.DD-x86_64.iso` file
3. Right-click on the file and select "Download"
4. Wait for the download to complete

> **Note:** The ISO file size is approximately 3 GB. A fast internet connection is recommended.

### Creating Bootable USB

#### On Linux (using dd):
```bash
# Identify your USB device (example: /dev/sdb)
lsblk

# Write ISO to USB (CAUTION: Choose the correct target disk!)
sudo dd if=fluxos-YYYY.MM.DD-x86_64.iso of=/dev/sdX bs=4M status=progress sync
```

#### On Windows:
- Use [Rufus](https://rufus.ie/) or [Balena Etcher](https://www.balena.io/etcher/)

#### On macOS:
```bash
# Use Disk Utility or dd command:
sudo dd if=fluxos-YYYY.MM.DD-x86_64.iso of=/dev/rdiskX bs=4m
```

### Installation Steps

1. **Boot from USB**
   - Enable USB boot from BIOS/UEFI settings
   - Start the system from FluxOS USB

2. **Live Environment**
   - The system will automatically boot into FluxOS live environment
   - You will see the installation icon on the desktop

3. **Start Installation**
   - **GUI Installation**: Double-click the "Install FluxOS" icon on the desktop
   - **Terminal Installation**: Run `sudo fluxos-install` command in terminal

4. **Installation Wizard**
   - Select language
   - Configure disk partitioning options
   - Create user account
   - Configure network settings

5. **Complete Installation**
   - After installation is complete, restart the system
   - Remove the USB drive
   - Welcome to FluxOS!

## 🎯 Calamares Installer

FluxOS uses the Calamares installer with offline mode. The installation sequence is as follows:

1. **partition** - Disk partitioning
2. **mount** - Mounting filesystems
3. **unpackfs** - Unpacking system files
4. **machineid** - Creating machine ID
5. **fstab** - Creating filesystem table
6. **locale** - Locale settings
7. **keyboard** - Keyboard layout
8. **localecfg** - Local configuration
9. **luksbootkeyfile** - LUKS boot key file
10. **users** - User accounts
11. **networkcfg** - Network configuration
12. **displaymanager** - Display manager
13. **hwclock** - Hardware clock
14. **grubcfg** - GRUB configuration
15. **bootloader** - Bootloader installation
16. **services-systemd** - Systemd services
17. **preservefiles** - Preserving files
18. **umount** - Unmounting filesystems

## 📦 Pre-installed Applications

### Desktop Applications
- **Firefox** - Web browser
- **Dolphin** - File manager
- **Konsole** - Terminal emulator
- **Kate** - Text editor
- **Partition Manager** - Disk management

### Security and Privacy
- **ClamAV & ClamTK** - Antivirus solution
- **Tor Browser Launcher** - Anonymous internet
- **OnionShare** - Secure file sharing
- **Firewalld** - Firewall

### System Management
- **Virt-Manager** - Virtual machine management
- **ISO Image Writer** - ISO writing tool
- **System Monitor** - System monitoring
- **Hardware Sensors** - Hardware sensors

### Development Tools
- **Git** - Version control system
- **Base-devel** - Development tools
- **Python** - Python programming language
- **Vim & Nano** - Command line editors

## 🤖 FluxAI Chat

FluxOS's custom AI assistant, a modern desktop application developed with PyQt5.

### Features:
- **Google Gemini Integration** - Advanced AI capabilities
- **Voice Output** - TTS support
- **Linux Command Agent** - Safe command generation and execution
- **Weather Agent** - 3-day weather forecast
- **Tech Chat** - Linux and system administration support

### Usage:
1. Launch "Flux AI Chat" from the applications menu
2. Add your Gemini API key in Settings
3. Optionally add Weather API key
4. Configure language and voice settings

## 🎨 Custom SDDM Theme

FluxOS comes with a custom designed SDDM login theme:

- **FluxOS Breeze Theme** - Plasma-compatible design
- **Custom Logos** - FluxOS branding
- **Modern Interface** - User-friendly login screen

Theme files are located at `/usr/share/sddm/themes/fluxos-breeze/`.

## 🛡️ Security Features

### Disk Encryption
- **LUKS2** full disk encryption support
- Encryption option during installation
- Secure key management

### Network Security
- **Firewalld** - Advanced firewall
- **WireGuard** - Modern VPN technology
- **Tor** support for anonymous browsing

### System Security
- **ClamAV** real-time protection
- **Polkit** privilege management
- **AppArmor** support (optional)

## 🛠️ Development

### Building ISO

To build FluxOS ISO yourself:

```bash
# Install required packages
sudo pacman -S archiso

# Clone the project
git clone https://github.com/berkkucukk/fluxos.git
cd fluxos

# Build ISO
cd releng
sudo ./build.sh
```

### Archinstall Customization

FluxOS uses customized archinstall:

```bash
# For development
cd fluxos/archinstall
python -m archinstall
```

### Calamares Configuration

Calamares settings are located in the `releng/airootfs/usr/share/fluxos/calamares/` directory.

## 🤝 Contributing

FluxOS is an open source project and we welcome your contributions!

### How to Contribute:

1. **Fork** - Fork the project on GitHub
2. **Create branch** - `git checkout -b feature/amazing-feature`
3. **Commit** - `git commit -m 'Add amazing feature'`
4. **Push** - `git push origin feature/amazing-feature`
5. **Open Pull Request** - Create PR on GitHub

### Contribution Areas:
- 🐛 Bug reports and fixes
- ✨ New feature suggestions
- 📚 Documentation improvements
- 🌍 Translation contributions
- 🎨 UI/UX improvements

## 💬 Support

Need help? Contact us:

- **ISO Download**: [Download from Google Drive](https://drive.google.com/drive/folders/1HW3jsPIsAfc14sPSyx1frohGKV81qnwQ?usp=sharing)
- **GitHub Issues**: [Report issues](https://github.com/berkkucukk/fluxos/issues)
- **Discussions**: [Join discussions](https://github.com/berkkucukk/fluxos/discussions)
- **Email**: support@fluxos.com.tr
- **Website**: https://www.fluxos.com.tr

### Bug Reporting

When reporting issues, please include:
- Detailed issue description
- System information (`uname -a`, `lscpu`, `free -h`)
- Error messages and logs
- Steps to reproduce the issue

## 📄 License

This project is licensed under the GPL-3.0 license. See [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

FluxOS is made possible thanks to these amazing projects:

- [Arch Linux](https://archlinux.org) - Base system
- [Calamares](https://calamares.io) - Installation tool
- [KDE Plasma](https://kde.org/plasma-desktop/) - Desktop environment
- [Archiso](https://gitlab.archlinux.org/archlinux/archiso) - ISO creation
- [ArchInstall](https://github.com/archlinux/archinstall) - Installation script

---

<div align="center">
  <p><strong>Experience the future of Linux with FluxOS! 🚀</strong></p>
  <p>Made with ❤️ by FluxOS Team</p>
</div>
