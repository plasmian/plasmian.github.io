![logo](https://raw.githubusercontent.com/plasmian/plasmian.github.io/02cb0f12465038b2a8de85b4f65aff00c934d095/plasmian_logo.png)

# Plasmian
## Debian with KDE Plasma: Sane Defaults and Noob-Friendly

Plasmian is a set of 'remastered' ISOs for installing Debian GNU/Linux 'testing' with KDE Plasma, with several modifications. It has a familiar look and feel and is user friendly for newcomers to the Linux desktop.

Plasmian is partially inspired by Linus Tech Tips' Linux daily driver challenge and partially by everything I do each time I install Debian with KDE. If you feel something should be changed in these builds, please create a Github issue [here.](https://github.com/plasmian/plasmian-script/issues)

###### _Plasmian is not associated with the Debian Project or KDE e.V._

## Download

[Download: 64-bit (amd64) image [Proprietary drivers and firmware included]](example.com) ← RECOMMENDED

Checksum: [SHA512](example.com)

[Download: 64-bit (amd64) image [Open-source drivers and firmware only]](example.com)

Checksum: [SHA512](Test.md)

_Please make sure to verify your download using the checksums. [Here's](example.org) how to check._

## Features
* Renaming strangely named apps like 'Kate' and 'Spectacle' to Text Editor and Screenshot
* Lots of bloat (anthy, goldendict, multilingual terminal, thai terminal, several input tools) preinstalled in the official images is removed
* Sane defaults for trivial stuff (double click to open folders, columns rather than rows on the desktop, template files for common office formats, disable splash screen,)
* Breeze theme for GTK, GRUB, Plymouth, SDDM is used
* Wine (latest builds from WineHQ), winetricks, wine-binfmt (to run .exe files by double-clicking etc.), Bottles (Flatpak) and Lutris are preinstalled
* OnlyOffice Desktop Editors (Flatpak) preinstalled
* Latest versions of commonly-updated apps like Firefox and OnlyOffice using Flatpak, and its backend for the Discover app store
* AppImage Pool (client for installing AppImages from AppImageHub) (Flatpak) and AppImageLauncher are preinstalled
* For convienence, proprietary drivers and firmware is preinstalled. Most modern hardware, especially wireless drivers and nVidia GPUs, require this. However **fully free images are also available.** (Free as in not listed by vrms.)
* Since it is based on Debian testing, it can more or less run packages meant for the latest Ubuntu release.

## Notes
* **What _exactly_ are your changes?** [This](https://github.com/plasmian/plasmian-script) is the script is used to build the ISO.
* **So this is basically just a modified version of an already available Debian ISO?** No, AFAIK there are no non-free firmware included images with a desktop environment preinstalled available on debian.org. Builds for stable _are_ available, but even they are messed up as in they do not include the non-free repo by default which means the installed non-free firmware and drivers will never be updated. Both fully free and non-free builds feature a bare minimum amount of configuration in these images.
* **Why does this exist.** I am tired of repeating the same steps again and again every time I distro hop and dislike the distro I hopped on to and switch back to Debian. Also I am frustrated by the lack of a proper 'newbie' distro which does everything from package management (looking at you, Steam in Pop OS) to having apps which are named so that someone outside the development team is not confused as to what it is supposed to be ('Spectacle', 'KCalc', 'Dolphin') right. Not that Plasmian is perfect, of course
* **Why Flatpak and AppImages.** Debian packages are very stable and secure which is why I am using them as the base distro. But since many packages are either not available (OnlyOffice, Bottles, AppImage Pool...) or outdated (Firefox ESR releases themselves are not very new, and they are not updated for some time after they are released in Debian) Flatpak is used in these cases, or AppImages, if the Flatpak is not available/ buggy. This is usually enough for most users' software needs. Snap packages are slow and increase boot time, and the server end for snap is closed-source. This is why it is not installed by default.
* **Why KDE Plasma.** I think it is the most complete and well-supported distro which supports modern standards like Wayland, Flatpak etc. without giving too much headache. GNOME is another option but I prefer the menubar and taskbar layout in KDE.
* **Where Pipewire.** Soon. Unfortunately Pipewire isn't quite as bug-free in KDE as I would like it to be yet. I _will_ switch to it, but after a release or two.
* **Why Wayland/systemd/whatever controversial software.** As more and more software are written with these being installed in mind, they are the future of Linux on the desktop. You are free to use any other distro (I recommend Devuan if you don't want to use systemd) as you like. I _may_ make Devuan based builds in the future if I have the time and interest, or you can do so and share it with the others (again, please make a Git issue.)
