# Arch Linux

Some of our friends have started putting together all the install instructions for Arch over on the [arch wiki](https://wiki.archlinux.org/title/Waydroid)

# Postmarket OS

Thanks to the Postmarket community, you can also find instructions and troubleshooting tips on their wiki:

{% embed url="https://wiki.postmarketos.org/wiki/Waydroid" %}

# Zorin OS

User @Aman9das has put together a detailed guide for installing Waydroid on Zorin OS:

{% embed url="https://github.com/Aman9das/Waydroid_Setup_Guide" %}

# Sailfish OS

A few of the contributors to sailfishos-open have put together a resource for installing Waydroid on the OS:

{% embed url="https://github.com/sailfishos-open/waydroid" %}

# Fedora

Waydroid can be installed from the official package repository.

```bash
sudo dnf install waydroid
```

After installing, launch Waydroid from the applications menu and proceed with the initialization by pasting these URLs in the OTA fields:

System OTA: `https://ota.waydro.id/system`

Vendor OTA: `https://ota.waydro.id/vendor`

## Silverblue/Kinoite/...

The same instructions apply to the Fedora Immutable variants, but you should use `rpm-ostree` instead of `dnf`

```bash
rpm-ostree install waydroid
```

# KISS Linux

User Mederim has come up with a guide for getting Waydroid on KISS Linux:

{% embed url="https://github.com/Mederim/kiss-waydroid" %}

# Void Linux

Waydroid can be installed from the official package repository; also check `/usr/share/doc/waydroid/README.voidlinux` after installation for further instructions!

```bash
sudo xbps-install -S waydroid
```

# Ubuntu/Debian and derivatives

For Droidian and Ubuntu Touch, skip directly to the last step

Make sure you have Wayland Session enabled (Ubuntu 22.04+)

{% embed url="https://linuxconfig.org/how-to-enable-disable-wayland-on-ubuntu-22-04-desktop" %}

* Install pre-requisites
```bash
sudo apt install curl ca-certificates -y
```

* Add the official repository
```bash
curl https://repo.waydro.id | sudo bash
```
If the script fails to detect your distribution, you can provide a valid option by appending `-s <DISTRO>`.
Currently supported values are: **mantic**, **focal**, **jammy**, **kinetic**, **lunar**, **noble**, **bookworm**, **bullseye**, **trixie**, **sid**

* Install waydroid
```bash
sudo apt install waydroid -y
```

Then start Waydroid from the applications menu.

# NixOS

NixOS community has a wiki page for WayDroid:

{% embed url="https://wiki.nixos.org/wiki/Waydroid" %}