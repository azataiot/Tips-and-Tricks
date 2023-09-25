# Alpine Linux Tips and Tricks

## Apk Command Examples in Alpine Linux

To update the package index on your system, simply run the command:

```bash
apk update
```

Apk search allows you to search for packages in the Alpine Linux repository.

```bash
apk search
```

Installing New Packages

```bash
apk add <pkg>
```

**ssh:**

```bash
apk add openssh
```

```bash
rc-update add sshd
```

```
service sshd start
```



To run the upgrade, use the command apk upgrade.

```bash
apk upgrade
```

Apk del is used to remove packages from your system. 

```bash
apk del <pkg>
```

Apk info displays detailed information about a package. 

```bash
apk info <pkg>
```

Apk fix is used to fix package dependencies that are broken or missing.

```bash
apk fix
```

## OpenRC

Alpine Linux uses [OpenRC](https://wiki.gentoo.org/wiki/OpenRC) for its init system.

The following commands are available to manage the init system:

- Basics:

```bash
rc-update add <service> <runlevel>
```

```bash
rc-update del <service> <runlevel>
```

```bash
rc-service <service> <start stop restart> # ⇔ /etc/init.d/service <start stop restart>
```

- To check services and their set runlevels:

```bash
rc-status
```

- To change to a different runlevel:

```bash
openrc <runlevel>
```

- Reboot/Halt/Poweroff: (And their equivalent from traditional GNU/Linux systems)

```bash
reboot   # ⇔ shutdown now -r
```

```bash
halt     # ⇔ shutdown now
```

```bash
poweroff # ⇔ shutdown now -P
```

### Available Runlevels

The available runlevels are:

- **default** - Used if no runlevel is specified. (This is generally the runlevel you want to add services to.)
- **hotplugged**
- **manual**



