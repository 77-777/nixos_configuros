# nixos_configuros

> On a stock KDE plasma 6, fresh installation of NixOS.

```bash
## The main configuration file location.
sudo nano /etc/nixos/configuration.nix

## Build the system and switch to it.
sudo nixos-rebuild switch
```


```bash

environment.systemPackages = with pkgs; [

  #########################################################
  ## Lean and Mean
  #########################################################

  ### Essentials
    gcc gnupg git gnumake openjdk

  ### Preliminary
    nano vim htop tree neofetch wget unrar p7zip rsync srm openssh

  ### Terminal
    tmux rtorrent lynx

  ### Browser
    firefox chromium

  ### Email
    thunderbird

  ### Torrent
    deluge

  ### Communication
    discord hexchat

  ### Security
    pass keepass veracrypt

  ### Multimedia
    vlc audacity handbrake

  ### Graphics
    gimp blender inkscape imagemagick

  ### Office
    libreoffice pdfsam-basic staruml yacreader

  ### Accessories
    anki cherrytree xmind sublime

  ### Networking
    akregator anydesk filezilla wireshark

  ### System
    virtualbox

  ### Development
    codeblocks ruby

  ### Gaming
    steam lutris

  #########################################################
  ## Extras
  #########################################################

  ### ghc ocaml

  ### anything for ntfs mounter?

  #########################################################
  ## KDE Flavours
  #########################################################

];

```