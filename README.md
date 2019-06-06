# copy-paste

## BASH

### Enable `apt` source packages
```
sed -i '/^#\sdeb-src /s/^# *//' "/etc/apt/sources.list"
```

### Disable (laptop) server lid switch
```
nano /etc/systemd/logind.conf
HandleLidSwitch=ignore
```

### Mount using `fstab`
```
blkid
nano /etc/fstab
UUID=aa917989-5538-48f5-9dfb-d595ac4ac041    /mnt/external    ext4    defaults    0    0
mount -a
```
