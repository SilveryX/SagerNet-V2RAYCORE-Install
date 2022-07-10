# SagerNet-V2RAYCORE-Install

Bash script for installing v2ray in operating systems such as CentOS / Debian / OpenSUSE that support systemd.

[Filesystem Hierarchy Standard (FHS)](https://en.wikipedia.org/wiki/Filesystem_Hierarchy_Standard)

```
installed: /etc/systemd/system/v2ray.service
installed: /etc/systemd/system/v2ray@.service

installed: /usr/local/bin/v2ray
installed: /usr/local/etc/v2ray/*.json

installed: /usr/local/share/v2ray/geoip.dat
installed: /usr/local/share/v2ray/geosite.dat

installed: /var/log/v2ray/access.log
installed: /var/log/v2ray/error.log
```

Notice: v2ray will NOT log to `/var/log/v2ray/*.log` by default. Configure `"log"` to specify log files.

## Basic Usage

**Install & Upgrade v2ray-core and geodata with `User=nobody`, but will NOT overwrite `User` in existing service files**

```
bash -c "$(curl -L https://github.com/SilveryX/SagerNet-V2RAYCORE-Install/raw/main/install-release.sh)" @ install
```

**Update geoip.dat and geosite.dat only**

```
bash -c "$(curl -L https://github.com/SilveryX/SagerNet-V2RAYCORE-Install/raw/main/install-release.sh)" @ install-geodata
```

**Remove v2ray, except json and logs**

```
bash -c "$(curl -L https://github.com/SilveryX/SagerNet-V2RAYCORE-Install/raw/main/install-release.sh)" @ remove
```

## Advance

**Install & Upgrade v2ray-core to a pre-release version**

```
bash -c "$(curl -L https://github.com/SilveryX/SagerNet-V2RAYCORE-Install/raw/main/install-release.sh)" @ install --version 5.0.16
```

**Install & Upgrade v2ray-core and geodata with `User=root`, which will overwrite `User` in existing service files**

```
bash -c "$(curl -L https://github.com/SilveryX/SagerNet-V2RAYCORE-Install/raw/main/install-release.sh)" @ install -u root
```

**Install & Upgrade v2ray-core without geodata**

```
bash -c "$(curl -L https://github.com/SilveryX/SagerNet-V2RAYCORE-Install/raw/main/install-release.sh)" @ install --without-geodata
```

**Remove v2ray, include json and logs**

```
bash -c "$(curl -L https://github.com/SilveryX/SagerNet-V2RAYCORE-Install/raw/main/install-release.sh)" @ remove --purge
```

## More Usage

```
bash -c "$(curl -L https://github.com/SilveryX/SagerNet-V2RAYCORE-Install/raw/main/install-release.sh)" @ help
```

