# copy-paste

## BASH

### Enable `apt` source packages
```
sed -i '/^#\sdeb-src /s/^# *//' "/etc/apt/sources.list"
```
