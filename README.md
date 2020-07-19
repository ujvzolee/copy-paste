# copy-paste

## Bash

### Enable `apt` source packages
```bash
sed -i '/^#\sdeb-src /s/^# *//' "/etc/apt/sources.list"
```

### Disable lid switch
```bash
nano /etc/systemd/logind.conf
HandleLidSwitch=ignore
```

### Mount using `fstab`
```bash
blkid
nano /etc/fstab
UUID=aa917989-5538-48f5-9dfb-d595ac4ac041    /mnt/external    ext4    defaults    0    0
mount -a
```

### Build Docker ARM on x86
```bash
docker run --privileged multiarch/qemu-user-static:register
```

### Create checksum for directory tree
```bash
find directory -type f -print0 | xargs -0 md5sum >> checksum.md5
```

## JavaScript

### String to uint32 hash function
```javascript
String.prototype.hashCode = function () {
  let hash = 0;

  if (this.length == 0) {
    return hash;
  }

  for (let i = 0; i < this.length; i++) {
    const char = this.charCodeAt(i);
    hash = ((hash << 5) - hash) + char;
    hash = hash & hash;
  }

  return hash >>> 0;
}
```
