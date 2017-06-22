# Notes

### Dependencies
These packages are required to create the ISO

```
sudo apt install curl git live-build cdebootstrap ubuntu-defaults-builder syslinux-utils genisoimage memtest86+ syslinux syslinux-themes-ubuntu-xenial gfxboot-theme-ubuntu livecd-rootfs
```

We also install these helper utilities for tracking the build and troubleshooting.

```
sudo apt install htop iotop iftop nmap lnav tmux
```

### Import config

```
lb config --config https://github.com/NHSbuntu/live-build-config
```

### Patch live-build

```
patch /usr/lib/live/build/lb_binary_disk < patches/lb_binary_disk.patch
```

### Build

```
export LB_ISO_TITLE="NHSbuntu"
export LB_ISO_VOLUME="NHSbuntu xenial $(date +%Y%m%d-%H:%M)"
sudo -E lb build
```

### References
[Oppourtunistic Live Build Tutorial/Notes](https://cmotc.github.io/personal-blog/Oppourtunistic-Live-Build-Basic-Tutorial/)
