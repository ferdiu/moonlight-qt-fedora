# Moonlight-Qt RPM Package

## Overview

Moonlight-Qt is an open-source PC client for **NVIDIA GameStream** and **Sunshine**, enabling users to stream games from their PC to other devices.

This repository contains the RPM packaging specification for Moonlight-Qt, making it easier to install on Fedora-based Linux distributions.

## Package Information

- **Name:** moonlight-qt
- **Version:** 6.1.0
- **Release:** 1
- **License:** GPL-3.0
- **Source Repository:** [GitHub - Moonlight-Qt](https://github.com/moonlight-stream/moonlight-qt)

## Build Dependencies

Ensure the following packages are installed before attempting to build:

```sh
sudo dnf install -y \
    qt6-qtsvg-devel qt6-qtdeclarative-devel openssl-devel SDL2-devel SDL2_ttf-devel \
    ffmpeg-devel libva-devel libvdpau-devel opus-devel pulseaudio-libs-devel \
    alsa-lib-devel libdrm-devel libplacebo-devel gcc-c++ make git
```

## Building the Package

To build the RPM package, follow these steps:

```sh
# Set up the build environment
rpmbuild -bb moonlight-qt.spec
```

This will create an RPM package ready for installation.

## Installation

Once built, install the package using:

```sh
sudo dnf install ./RPMS/x86_64/moonlight-qt-6.1.0-1.x86_64.rpm
```

## Running Moonlight-Qt
After installation, you can launch Moonlight-Qt from the applications menu or via the terminal:

```sh
moonlight
```

## Changelog

- **6.1.0-1 (Feb 22, 2025)**
  - Initial packaging of Moonlight-Qt

## License

Moonlight-Qt is licensed under **GPL-3.0**. See the [LICENSE](https://github.com/moonlight-stream/moonlight-qt/blob/master/LICENSE) file for more details.

---
**Maintainer:** Federico Manzella (AKA [ferdiu](https://github.com/ferdiu))

