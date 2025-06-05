# UERANSIM Debian Package

## Overview

This repository contains the makedeb PKGBUILD file for building UERANSIM as a Debian package. UERANSIM is an open-source 5G UE and RAN (gNodeB) simulator implementation.

## Prerequisites

- Ubuntu 22.04 or later / Debian-based distribution
- [makedeb](https://www.makedeb.org/) installed on your system

## Build Process

1. Clone this repository:
   ```bash
   git clone https://github.com/jerry73204/UERANSIM-debian-packages.git
   cd UERANSIM-debian-packages
   ```

2. Build and install the package:
   ```bash
   makedeb -si
   ```

## Usage

After installation, the following commands will be available:

- `nr-gnb` - 5G gNodeB (base station)
- `nr-ue` - 5G User Equipment
- `nr-cli` - Command line interface tool
- `nr-binder` - Internet connectivity tool

Example configuration files are installed in `/usr/share/ueransim/config/`.

For detailed usage instructions, refer to the [official UERANSIM documentation](https://github.com/aligungr/UERANSIM/wiki).

## License

UERANSIM is licensed under GPL-3.0. See the LICENSE file for details.
