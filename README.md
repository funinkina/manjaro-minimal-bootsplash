# Manjaro-minimal-bootsplash

Kernel Bootsplash theme for manjaro Linux using Manjaro logo and a custom spinner.

This project is a fork of the follwing project:
https://github.com/trdmm/bootsplash-theme-alien

The spinner base gif was created using Preloaders.net and heavily modified afterwards.


# Installation:

- `git clone https://github.com/trdmm/manjaro-minimal-bootsplash.git`
- `cd manjaro-minimal-bootsplash`
- run `chmod +x bootsplash-minimal.sh`
- run `chmod +x bootsplash-packer`
- run `./bootsplash-minimal.sh` to generate STL model.
- run `makepkg -s` to create an Arch package and install it with `pacman -U $package_name`or alternatively make and install with one single command: `makepkg -sci`
- append `manjaro-minimal-bootsplash` hook at the end of HOOKS string in `/etc/mkinitcpio.conf`
- add `bootsplash.bootfile=bootsplash-themes/minimal/bootsplash` at the end of `GRUB_CMDLINE_LINUX` string in `/etc/default/grub` and don't forget to remove the `quiet` parameter!
- run `sudo mkinitcpio -P`
- run `sudo update-grub`
