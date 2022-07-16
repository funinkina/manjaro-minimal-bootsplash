# Manjaro Minimal Bootsplash

Plymouth theme for manjaro Linux using Manjaro logo and a custom spinner.

This project is a fork of [this project](https://github.com/trdmm/bootsplash-theme-alien).

The spinner base gif was created using Preloaders.net and heavily modified afterwards.

## Preview:
![preview](https://github.com/funinkina/manjaro-minimal-bootsplash/blob/main/preview.gif)

## Installation:

- use `git clone https://github.com/funinkina/manjaro-minimal-bootsplash.git` to clone this repository to your home folder.
  
- `cd manjaro-minimal-bootsplash`
  
- run `chmod +x bootsplash-minimal.sh`
- run `chmod +x bootsplash-packer`
- run `./bootsplash-minimal.sh` to generate the STL model.
- run `makepkg -sci` to create and and install the package automatically _(alternatively you can use `makepkg -s` to create the arch package and install it with: `pacman -U $package_name`)_.
- append `manjaro-minimal-bootsplash` hook at the end of HOOKS string in `/etc/mkinitcpio.conf`  
  it should look something like this:
  >HOOKS="base udev autodetect modconf block keyboard keymap consolefont plymouth resume filesystems fsck manjaro-minimal-bootsplash"
- add `bootsplash.bootfile=bootsplash-themes/minimal/bootsplash` at the end of `GRUB_CMDLINE_LINUX` string in `/etc/default/grub` and don't forget to remove the `quiet` parameter!  
  it should look something like this:  
  >GRUB_CMDLINE_LINUX_DEFAULT="bootsplash.bootfile=bootsplash-themes/minimal/bootsplash"
- run `sudo mkinitcpio -P`
- run `sudo update-grub`
