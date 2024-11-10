# nixos_configuros

> On a stock KDE plasma 6, fresh installation of NixOS.

```bash
## The main configuration file location.
sudo nano /etc/nixos/configuration.nix

## Build the system and switch to it.
sudo nixos-rebuild switch

## Clean up older iterations and packages.
...

## Updating the distribution
...
```

```bash
## Enabling awesome
services.xserver.windowManager.awesome.enable = true;
```

```bash
fonts.packages = with pkgs; [
  roboto
];
```

```bash

environment.systemPackages = with pkgs; [

  #########################################################
  ## Lean and Mean
  #########################################################

  ### Essentials
    gcc gnupg git gnumake openjdk coreutils-full util-linux alsa-utils

  ### Preliminary
    nano vim emacs htop tree neofetch wget unrar p7zip rsync srm openssh

  ### Terminal
    tmux irssi rtorrent lynx tty-clock slock weechat scrot

  ### Browser
    firefox chromium

  ### Email
    thunderbird

  ### Torrent
    deluge transmission transmission-qt

  ### Communication
    discord hexchat

  ### Security
    pass keepass veracrypt

  ### Multimedia
    vlc audacity handbrake lmms openshot-qt

  ### Graphics
    gimp blender inkscape imagemagick

  ### Office
    libreoffice pdfsam-basic staruml yacreader

  ### Accessories
    anki cherrytree xmind sublime vscode evince

  ### Networking
    akregator anydesk teamviewer filezilla wireshark

  ### System
    virtualbox

  ### Development
    codeblocks ruby texmaker

  ### Gaming
    steam lutris

  ### Miscellaneous, Fonts, Etc
    pkgs.roboto
    pkgs.awesome
    xfce.thunar

  #########################################################
  ## Extras
  #########################################################

  ### Primary (development)
    ghc ocaml opam nodejs

  ### Secondary (gaming)
    wine wine64 winetricks

  ### Alternatives
    # evolution qemu subversion mercurial

  ### KDE Flavours
    # kontact kleopatra korganizer kget kmail kdevelop konversation ktorrent krita ## okular kdenlive konqueror amarok

  ### Misc
    # fastfetch element-web guake yakuake scribus i3 desmume dolphin-emu ppsspp-qt iptables # gparted gnome-system-manager/monitor

  ### Not in Nixos Repository
    # freedownloadmanager citra nixnode2 caesium cheese clonespy # quiterss [some qtwebkit error]

  ### anything for ntfs mounter?
    # ???

  ### what about setting scheduler and kernel vm parameters?
    # ???

];

```
