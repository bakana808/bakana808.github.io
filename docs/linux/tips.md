[adding Gamecube Controller Adapter support](https://wiki.dolphin-emu.org/index.php?title=How_to_use_the_Official_GameCube_Controller_Adapter_for_Wii_U_in_Dolphin#Linux)

[udisks - changing default mount point to `/media`](https://wiki.archlinux.org/title/Udisks#Mount_to_/media)

```markdown
/etc/udev/rules.d/99-udisks2.rules
```
```sh
# UDISKS_FILESYSTEM_SHARED
# ==1: mount filesystem to a shared directory (/media/VolumeName)
# ==0: mount filesystem to a private directory (/run/media/$USER/VolumeName)
# See udisks(8)
ENV{ID_FS_USAGE}=="filesystem|other|crypto", ENV{UDISKS_FILESYSTEM_SHARED}="1"
```