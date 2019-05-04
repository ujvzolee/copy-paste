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
