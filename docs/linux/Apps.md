# Apps

```sh
# Core

git
linux-headers
#iwd             # daemon for connecting to wireless networks
networkmanager  # daemon and CLI for connecting to networks (wired and wireless)
inetutils       # collection of common network programs
fontconfig      # library used by many apps for font access
brightnessctl   # tool to control screen brightness
man-db          # implements manual pages (man)
os-prober       # (optional) allows GRUB to detect other OS installations if dual-booting 

## Core - filesystems

exfatprogs  # add exFAT fs support

## Core - zen kernel

linux-zen
linux-zen-headers

# after installing linux-zen, run `sudo grub-mkconfig -o /boot/grub/grub.cfg` to create a boot entry for it.
# after confirming booting linux-zen works, then you can uninstall `linux` and `linux-headers`

## Core - NVidia

nvidia-open-dkms
nvidia-utils
nvidia-settings
linux-firmware-nvidia
lib32-nvidia-utils

## Core - power

upower
power-profiles-daemon

## Core - audio

pipewire
wireplumber

## Core - printing
  
cups
cups-filters
cups-browsed           # daemon for discovering printers on the network
cups-pdf               # allow printing to a PDF document
system-config-printer  # CUPS printer configuration tool and status applet

## Core - security

polkit
gnome-keyring
libsecret
ufw            # firewall

# Development

jdk-openjdk  # Java
rust         # Rust (official)
luarocks     # package manager for Lua modules

# Fonts

noto-fonts
noto-fonts-cjk
noto-fonts-emoji
noto-fonts-extra
woff2-font-awesome
ttf-fantasque-sans-mono
ttf-material-symbols-variable
inter-font

# Desktop / Essentials

sddm                # simple display manager
hyprland            # wayland window manager
hyprlock            # lock screen
hypridle            # provides idle timeouts for auto screen off/suspend
polkit-gnome        # authorization agent
quickshell          # toolkit for desktop widgets, bars, system tray icons, notifications, etc.
qt6-positioning
qt6-5compat
kitty               # terminal emulator
#alacritty
fish                # shell with auto-complete and syntax highlighting
starship            # customizable shell prompt
#dolphin
nautilus            # file explorer
nautilus-open-any-terminal  # (AUR)
sushi               # file previewer (integrates w/ nautilus)
file-roller         # file archive manager (integrates w/ nautilus)
ffmpegthumbnailer   # video thumbnail support for file managers
gvfs-mtp            # adds MTP support to nautilus
gvfs-nfs
gvfs-smb
gnome-disk-utility  # disk manager
gnome-tweaks        # settings app for GTK based apps
nwg-displays        # display manager for wayland
evince              # document viewer
udiskie             # 
#imv                 # image viewer

# Desktop - screen capture

gpu-screen-recorder  # (AUR) shadowplay-like screen recording

slurp                # wayland region selection utility
grim                 # wayland screenshot utility
satty                # screenshot annotator
#swappy

# Shell tools

7zip
tealdeer    # adds "tldr <cmd>" to print a summary of how to use the command
fzf         # fuzzy finding
ripgrep
eza         # nicer looking ls replacement
fd          # easier-to-use find replacement
bat         # cat replacement with syntax highlighting
bat-extras  # additional scripts for bat such as "batman" for syntax highlighted man pages
jq          # JSON processor
inxi        # system information tool
btop            # nicer looking htop replacement
fastfetch       # nicer looking neofetch replacement
dust            # nicer looking du replacement

# TUIs

neovim
impala          # wi-fi manager
bluetui         # bluetooth manager
playerctl       # media player controller
spotify_player  # terminal-based spotify client
wiremix         # pipewire audio mixer
plocate         # file finder

# GUIs

firefox
obsidian        # note taking app
libreoffice     # free office app suite
mpv             # media player
spotify         # official package for spotify
discord         # official package for discord
obs-studio
aesprite        # pixel art image editor
pinta           # image editor
swappy          # image snapshot editor

# Gaming
steam           # official package for steam
gamescope       # gaming-focused microcompositor for running games

# Game Emulation
igir-bin        # ROM database manager
flips-git       # ROM patcher (.ips/.bps files)
```

## `quickshell`

- is able to make lockscreens (possibly replacing `hyprlock`)
	- see https://git.outfoxxed.me/quickshell/quickshell-examples/src/branch/master/lockscreen/shell.qml
- is able to handle dbus notifications (replacing most notification apps)
	- test with `notify-send <msg> <submsg>`
- is able to manage Bluetooth (replacing any GUI that does the same thing)
	- requires `bluez` and `dbus`. `bluetooth.service` and `dbus-broker.service` need to be running.
- is able to make a system tray / show applets
- is able to make a media player controller
- is able to make a greeter (using [greetd](https://man.sr.ht/~kennylevinsen/greetd/#setting-up-greetd-with-gtkgreet), possibly replacing `sddm`)

## TO REMOVE:
```bash
sddm      # replace with greetd & login screen made in quickshell
hyprshot  # replace with slurp/grim
```

INTERESTING STUFF:
```bash
gum
tobi-try
typora    # markdown editor
mise
wayfreeze  # tool to freeze the wayland compositor (for screenshots)
zoxide     # cd replacement
```