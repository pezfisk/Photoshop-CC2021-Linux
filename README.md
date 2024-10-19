# Photoshop-CC2021-Linux

## Important

### You have to provide your own AdobePhotoshop2021.tar.xz file!

- Put AdobePhotoshop2021.tar.xz in the same directory as this script

#### PLEASE WHEN OPENING AN ISSUE FILL THE TEMPLATE OR GIVE ENOUGHT INFORMATION !!! "It doesn't work" ISN'T ENOUGH **

This git repo contains an installer for photoshop CC 2021 on linux with wine.

#### Credits:
- [LinSoftWin](https://github.com/LinSoftWin/Photoshop-CC2022-Linux): For making the original install script
- [cheeeeer](https://github.com/cheeeeer/Photoshop-CC2022-Linux): For cleaning up the installer

| Version  | Rating | Problems |
| ------------- | ------------- | ------------- |
| [CC 2021](https://github.com/MiMillieuh/Photoshop-CC2022-Linux/releases/tag/2.1.3)  | Small visual errors  |  Canvas rendered outside the main one may flicker, Copy/Pasting doesn't work under Wayland  |

Tested on Arch Linux (6.10.10-arch1-1) running Hyprland (v0.43.0)

![Screenshot from 2022-05-17 00-02-27](https://user-images.githubusercontent.com/52078885/168690419-274020b0-c993-4b86-a58f-f0f07237aa4f.png)

*File download is about 2GB*

## Requirements
- wine >=6.1 (Avoid 6.20 to 6.22 **DON'T USE STAGING**) 

(Wine 8.0+ are causing an issue with the windows version see workaround [here](https://github.com/MiMillieuh/Photoshop-CC2022-Linux/issues/94#issuecomment-1426776219))
- zenity
- appmenu-gtk-module
- tar
- wget
- curl
- All R/W rights on your home folder and the installer folder
- Vulkan capable GPU or APU (Older GPUs might encounter [This issue #100](https://github.com/MiMillieuh/Photoshop-CC2022-Linux/issues/100))


## Usage: 

**CLI:**

`sh photoshop2021install.sh /path/to/your/install/folder`

**Camera Raw**
You can install Camera Raw this way:

`sh photoshop2021install.sh /path/to/your/install/folder --camera-raw`

To use camera raw you need to change a settings
Edit -> preferences -> Camera raw... -> performance -> Use graphic processor: Off

If camera raw is sometimes grayed out, just go to: Edit -> preferences -> Tools, and uncheck show Tooltips.

**Uninstalling:**

To uninstall remove the photoshop desktop file in *~/.local/share/applications/* then your installation folder


## Special thanks to
- The WineHQ team: For making wine
- Gictorbit: For initial inspiration
- HansKristian-Work: For making VKD3D-Proton
- Adobe: For making Photoshop (also please release an official version for linux...)
