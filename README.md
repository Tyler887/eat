# 🛑 Reminder
`eat` is moving from `Tyler887/eat` to `EatInstall/Eat` for better maintaining of
the package manager. You may need to [uninstall `eat`](https://github.com/EatInstall/Eat/wiki/Uninstall)
and do the [installation steps below](#install).
# `eat`
[![Status](https://img.shields.io/badge/status-alpha-red)](https://github.com/Tyler887/eat/commits/main) + [![GitHub download](https://img.shields.io/github/downloads/Tyler887/eat/total)](https://github.com/Tyler887/eat/releases) + [![License](https://img.shields.io/github/license/Tyler887/eat)](https://github.com/Tyler887/eat/blob/main/LICENSE)

Eat is the package manager for Linux. It:
* **Does not even require  `sudo`!**
* Adds the programs to your PATH
* Does total web scraping to download files
* Makes sharing L\*nux programs easier
<!--
## Install
Simple (this script was made for BASH):
```bash
git clone htttps://github.com/Tyler887/eat
cd eat
bash ./inst-script.sh
# Then, restart your shell and run 'eathelp' for the manpage
```
**Note:** The example above uses `git`, which might not be installed on your Linux distribution. If `git` does not seem to be a command (which you can look for by running `which git`), you can run:
```bash
bash -c "$(curl -fsSL https://raw.githubusercontent.com/Tyler887/eat/main/inst-script.sh -#)"
```
Usally, `eat` only works in BASH shells. If you would like to edit your shell's own init script, run:
```bash
nano .<shell>rc
```
### Ubuntu recovery mode install
1. Hold <kbd>Shift</kbd> on boot until the GRUB2 menu appears.
2. Select `Advanced options for Ubuntu` and choose the second option.
3. When Ubuntu starts up recovery mode, select `network` then confirm with "Yes".
   This is because Git and APT cannot reach the internet without networking mode.
5. Select `root` after networking mode for Recovery Mode is set up, then enter `root`'s password.
6. Run `su <your own UNIX user name>` to actually install to your user (else `eat` only works for the `root` user).
7. Follow the steps above.
8. Run `reboot`, hold <kbd>Shift</kbd>, select `Advanced options for Ubuntu` -> the second option, select `network` > `Yes` > `root`, enter `root`'s password, run `su <your own UNIX user name>`, and try it out using `eatinst setup-eat`. This will usally initiate the sources, because there's no `setup-eat.yaml` in the manifest network.
9. `reboot` your system without going into GRUB.
## Upgrading
If your installation is out of date (which Eat normally tells you) or you have out-of-date sources,
you should upgrade both of them.

To upgrade Eat and the source manifests, the fastest way is to run `bash ~/Eat-PKG-Manager/update.sh`.
Using `git pull` also works, but your sources will need to be upgraded manually.
-->
## New manifests
A manifest goes into the [network](https://github.com/Tyler887/eat-network), and not in this repo.
To add more manifests to eat, please contribute there.

The specification of an Eat package is:
```yaml
uri: # URI for package archive (.zip or .tar.gz). Eat will not install packages without this.
depends:
   - # Array of dependencies. Eat will fail installation if one of these are not installed. Empty by default
should_install:
   - # Array of suggested packages (e.g. "soft dependencies"). Empty by default
sudo_necessary: # Whether the app touches the system or not. "true" or "false" accepted only. Default is "false"
```

A manifest must be named `<manifest name>.yaml`, not something like `<manifest name>.json` or `<manifest name>.yml`.
