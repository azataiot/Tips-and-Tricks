# Debian

## Install Docker Engine

### [Uninstall old versions](https://docs.docker.com/engine/install/debian/#uninstall-old-versions)

```bash
for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do apt remove $pkg; done
```

### [Install using the convenience script](https://docs.docker.com/engine/install/debian/#install-using-the-convenience-script)

```bash
export LC_CTYPE=en_US.UTF-8
export LC_ALL=en_US.UTF-8
locale-gen
```

```bash
wget -O get-docker.sh https://get.docker.com && sh ./get-docker.sh
```

