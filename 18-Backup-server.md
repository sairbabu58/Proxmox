# Proxmox Backup Server configuration


### Create proxmox Backup server

```
> One Physical Server
> SSD-01 30 Gib for OS
> SSD-02 500/1TiB for backup storage
```

### Installation

```
> Go to the Proxmon Web Side
> https://proxmox.com/en/downloads/proxmox-backup-server
> Create the bootable disk
> Boot the VM and configure the Backup server
> Access the backup server over webUI
> https://192.168.0.105:8007
> User: root
> Password: 
```

### Update backup server

```
> Open Backup server webUi
> Administration
> Repositories
> [Disable] Enterprice repo

> Add the new repo for No-Subscription
> Follow the latest docs

$ apt-get update
$ apt-get dist-upgrade 
```
