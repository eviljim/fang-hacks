## Modifications needed to base SD card image
  edited snx_autorun.sh (adds delay); needs to be done before boot

## Create log folder on SD card:
  mkdir /media/mmcblk0p2/data/log

## Deploy modified files:
```
  IP=192.168.86.
  scp data/usr/bin/watchdog root@$IP:/media/mmcblk0p2/data/usr/bin/watchdog
  scp data/etc/scripts/20-rtsp-server root@$IP:/media/mmcblk0p2/data/etc/scripts/20-rtsp-server
  scp data/etc/scripts/25-watchdog root@$IP:/media/mmcblk0p2/data/etc/scripts/25-watchdog
  scp bootstrap/www/scripts root@$IP:/tmp/www/cgi-bin/scripts
```
