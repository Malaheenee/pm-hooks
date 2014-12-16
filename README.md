# Collection of usable hooks for pm-utils #

## Description ##
You can manage many options without laptop-mode-tools.

## Installation ##
1. Copy "*-power" to /etc/pm/power.d and make it executable.
2. Copy "*-settings" to /etc/pm/config.d.

## Troubleshooting ##
1. Check /var/log/pm-powersave.log - what is wrong?
2. Check owner of both files. It **MUST** be "root".
3. Check state of acpid.service (in case of systemd).
4. If your Radeon card don't has file */sys/class/drm/card0/device/power_dpm_state*:
   Create */etc/modprobe.d/radeon-kms.conf* with following text:
   `options radeon modeset=1 dynclks=1 hw_i2c=1 aspm=1 dpm=1`
   And reboot.

## Notebook models: ##
* ASUS F3Sr
* ASUS K43e
