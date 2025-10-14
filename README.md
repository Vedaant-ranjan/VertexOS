# Vertex OS

A Linux-Based Operating System Built from Scratch
🚀 A Modern Replacement for Windows & macOS — Especially for Windows 10 Users

## 🌟 About

Vertex OS is a lightweight, custom-built Linux distribution designed as a clean, fast, and user-friendly alternative to mainstream operating systems like Windows 10/11 and macOS. Whether you're looking for speed, privacy, or a fresh start — Vertex OS is here to give your computer a new life.

## 💡 Built by Vedaant Ranjan — 12 Years Old 🇮🇳 | Made with ❤️ in India

## 🔧 Contribute

We welcome contributions to help make Vertex OS even better!

Here's how you can help:

- Fork this repository.
- Make improvements to the code or features.
- Test it using QEMU, VirtualBox, or directly on your system.
- Take a screenshot of the OS running.
- Submit a Pull Request with your changes and attach the screenshot.

## 📌 Goals

- Build an open, fast, and secure Linux-based OS from scratch.
- Offer a smooth transition for Windows and macOS users.
- Encourage young developers to explore operating system development.

## ❤️ Special Thanks

To the amazing open-source community that makes projects like this possible.
And a big thank you to everyone supporting this journey!

---

VertexOS is a unified operating system that combines Linux and Windows compatibility, featuring a modern GNOME desktop environment with WhiteSur theme and custom branding.

## Structure

- `/core/` - Linux kernel source + drivers
- `/system/` - Init system + vertexd daemon + boot scripts + GNOME configuration
- `/ui/` - Legacy HTML interface (deprecated, GNOME desktop now used)
- `/apps/` - Preloaded Linux apps (Chrome, VLC, Terminal, LibreOffice, GIMP, VTX Package Manager, APK Package Manager)
- `/apps/windows/` - Windows EXEs
- `/usr/bin/` - Wine binary + winget.exe + Linux binaries
- `/data/` - NTFS/FAT user partition (mount scripts included)
- `/icons/` - App icons (PNG format)
- `/build-scripts/` - Bash/Python scripts to compile kernel, install apps, configure Wine, build ISO

## Building VertexOS ISO

1. **Prerequisites:**
   - Ubuntu/Debian-based build system
   - Root privileges
   - Internet connection for package downloads

2. **Build Steps:**

   ```bash
   # 1. Build the Linux kernel
   sudo ./build-scripts/build-kernel.sh

   # 2. Build kernel drivers
   sudo python3 build-scripts/build-drivers.py

   # 3. Install preloaded applications
   sudo ./build-scripts/install-apps.sh

   # 4. Configure Wine for Windows compatibility
   ./build-scripts/configure-wine.sh

   # 5. Build the ISO
   sudo ./build-scripts/build-iso.sh
   ```

3. **Boot the ISO:**
    - Use VirtualBox, VMware, or burn to USB drive
    - Boot from the `vertex-os.iso` file
    - The system will start with the GNOME desktop environment featuring WhiteSur theme

## Features

- **Modern Desktop:** GNOME desktop environment with WhiteSur theme and custom VertexOS branding
- **Package Managers:** VTX (APT-based) and APK Package Manager for comprehensive software management
- **Cross-Platform Apps:** Run both Linux and Windows applications
- **Wine Integration:** Windows compatibility layer
- **NTFS/FAT Support:** Access Windows partitions
- **Security Hardened:** SELinux, AppArmor, and UFW firewall integration
- **Custom Kernel:** Optimized Linux kernel with custom drivers

## System Requirements

- x86_64 architecture
- 2GB RAM minimum
- 10GB disk space for installation
- Graphics card with OpenGL support

## Package Managers

VertexOS includes two comprehensive package managers:

- **VTX (APT Package Manager):** GUI-based Debian/Ubuntu package management using Synaptic
- **APK Package Manager:** Android package management via F-Droid web interface

Both package managers are accessible from the GNOME desktop and provide extensive software installation capabilities.

## Development

The system is designed to be modular. Each component can be developed independently:

- Desktop/GNOME: Edit `/system/gnome-config.sh` and GNOME settings
- Package Managers: Modify `/apps/apt.sh`, `/apps/apk.sh`, and webapp scripts
- System services: Modify `/system/` scripts
- Drivers: Update `/core/drivers/`
- Apps: Add to `/apps/` directory and update `/apps/manifest.json`

## Community Support

Join the VertexOS community for support, discussions, and contributions:

- **GitHub Issues:** Report bugs and request features
- **GitHub Discussions:** Community Q&A and general discussion
- **Documentation Wiki:** User guides and developer documentation
- **Discord Server:** Real-time community chat and support

### Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details on:

- Code style and standards
- Pull request process
- Development setup
- Testing guidelines

### Support Channels

- **Bug Reports:** [GitHub Issues](https://github.com/vertex-os/VertexOS/issues)
- **Feature Requests:** [GitHub Discussions](https://github.com/vertex-os/VertexOS/discussions)
- **General Help:** [Discord Server](https://discord.gg/vertex-os)
- **Documentation:** [Wiki](https://github.com/vertex-os/VertexOS/wiki)

## License

This project is released under the GPL v3 license.
