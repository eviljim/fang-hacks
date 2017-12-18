## Modifications needed to base SD card image
  edited snx_autorun.sh (adds delay); needs to be done before boot

## One time setup for new files and new log directory
```
  mkdir /media/mmcblk0p2/data/log
  chmod ugo+x /media/mmcblk0p2/data/usr/bin/watchdog
  chmod ugo+x /media/mmcblk0p2/data/etc/scripts/25-watchdog
```

## Update modified files
```
  IP=192.168.86.
  scp data/usr/bin/watchdog root@$IP:/media/mmcblk0p2/data/usr/bin/watchdog
  scp data/etc/scripts/20-rtsp-server root@$IP:/media/mmcblk0p2/data/etc/scripts/20-rtsp-server
  scp data/etc/scripts/25-watchdog root@$IP:/media/mmcblk0p2/data/etc/scripts/25-watchdog
  scp bootstrap/www/scripts root@$IP:/tmp/www/cgi-bin/scripts
```
