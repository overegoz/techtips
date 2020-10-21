# 우분투

## Ubuntu 18.04 to 20.04

From : https://www.cyberciti.biz/faq/upgrade-ubuntu-18-04-to-20-04-lts-using-command-line/

1. Upgrade all installed packages of Ubuntu version 18.04 by running `sudo apt update && sudo apt upgrade` command.
2. Reboot the Ubuntu Linux system by tying the `sudo reboot` command
3. Install the Ubuntu update tool, run: `sudo apt install update-manager-core`
4. Start the upgrade procdure by running `sudo do-release-upgrade`
5. Reboot the box by running `sudo reboot`
6. Verify upgrades : `lsb_release -a`

중간에 GRUB을 어디에 설치할지를 물어보는 화면이 나오는데, "잘 모를 경우 모두 선택하라"라는 안내가 있어서 모든 드라이브에 GRUB을 설치하도록 선택했음 (내 경우, VirtualBox에 가상머신을 만들어서 우분투를 사용하고 있고, 드라이브는 sda, sda1 이렇게 두 개가 있고, 두 개 모두에 GRUB을 설치하는 것으로 설정했음)
