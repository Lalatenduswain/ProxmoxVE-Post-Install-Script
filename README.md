# Proxmox VE Post Install Script

**Author:** Lalatendu Swain  
[GitHub](https://github.com/Lalatenduswain) | [Website](https://blog.lalatendu.info/)

This script is designed to automate the post-installation setup of Proxmox VE. It streamlines the configuration of repositories, high availability, and system updates. Use this script responsibly and ensure your environment is backed up before proceeding.

## Disclaimer | Running the Script

**Author:** Lalatendu Swain | [GitHub](https://github.com/Lalatenduswain) | [Website](https://blog.lalatendu.info/)

This script is provided as-is and may require modifications or updates based on your specific environment and requirements. Use it at your own risk. The authors of the script are not liable for any damages or issues caused by its usage.

## Donations

If you find this script useful and want to show your appreciation, you can donate via [Buy Me a Coffee](https://www.buymeacoffee.com/lalatendu.swain).

## Description

This script automates post-installation routines for Proxmox VE, including repository configurations, enabling/disabling high availability, and system updates. It interacts with the Proxmox VE environment using sudo privileges.

## Prerequisites

- **Operating System:** Debian-based Linux system (Ubuntu, Debian, Proxmox VE 8.x or higher)
- **Sudo Privileges:** Ensure the user has sudo access to execute apt commands.
- **Network Access:** Internet access is required for downloading repository packages.

## Installation

Clone this repository using:

```bash
git clone https://github.com/Lalatenduswain/ProxmoxVE-Post-Install-Script.git
cd ProxmoxVE-Post-Install-Script
```

## Usage

1. **Make the script executable:**

   ```bash
   chmod +x post-pve-install.sh
   ```

2. **Run the script:**

   ```bash
   ./post-pve-install.sh
   ```

## Script Overview

This script automates several post-installation configurations for Proxmox VE:

### Features:

1. **Repository Management**:
   - Correcting Proxmox VE sources.
   - Disabling `pve-enterprise` repository (for non-subscribers).
   - Enabling `pve-no-subscription` repository.
   - Managing `Ceph` package repositories.
   - Adding/Disabling `pvetest` repository.

2. **High Availability Management**:
   - Enabling or disabling high availability (HA) services (e.g., `pve-ha-lrm`, `corosync`).

3. **System Updates**:
   - Updating Proxmox VE and its components.
   - Rebooting the system post-upgrade for changes to take effect.

## Contributing

If you would like to contribute to this script, feel free to fork the repository and submit a pull request. Make sure to include tests and documentation for any changes made.

## Support or Contact

Encountering issues? Don't hesitate to submit an issue on our [GitHub page](https://github.com/Lalatenduswain/ProxmoxVE-Post-Install-Script/issues).
