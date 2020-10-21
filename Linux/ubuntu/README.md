# 우분투

## Ubuntu 18.04 to 20.04

From : https://www.cyberciti.biz/faq/upgrade-ubuntu-18-04-to-20-04-lts-using-command-line/

1. Upgrade all installed packages of Ubuntu version 18.04 by running `sudo apt update && sudo apt upgrade` command.
2. Reboot the Ubuntu Linux system by tying the `sudo reboot` command
3. Install the Ubuntu update tool, run: `sudo apt install update-manager-core`
4. Start the upgrade procdure by running `sudo do-release-upgrade`
5. Reboot the box by running `sudo reboot`
6. Verify upgrades : `lsb_release -a`