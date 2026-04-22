# Proxmox Backup Server configuration


### Create proxmox Backup server

```
> One Physical Server
> SSD-01 30 Gib for OS
> SSD-02 500/1TiB for backup storage
> [Optional] SSD-03 500/1TiB for backup storage with RAID configuration using [ssd-02 and ssd-03]
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



### Configure Backup Server

```
> Backup server web console
> Storage/Disks
> ZFS
  Name: backup-data
  RAID Level: Single [if you have multiple disk, please choose other option]
  [tik] the disk
> create

Note: Directory is for storing ISO images or any kind of template
```

### Validation

```
> Backup server web console
> Storage/Disks
> ZFS
See the status

> Datastore
See more details over here [backup-data]
  > Summury 
  - backup count
  - CT
  - Host
  - Vm
```

### Add Permission to get access this Backup server from proxmox 


```
> Backup server web console
> Datastore
> Backup-data
  > Permission
  > Add
  > User Permission
    Path: /datastorage/backup-data
    User: backup-admin [better to create the user and assign here] 
    Role: Datastore admin or Backup admin
> Add

Note: also possible to add multiple permission to same user
```


### Take the Backup from Proxmox

```
> Proxmox WebUI
> Datacenter
> Backup
> Add
General:
  Node: all
  Storage: [Choose the backup storage]
  Sehedule: when its going to execute

Notification:
  Global notofication
  Email id to send
    - Always
    - On Failure only

Retention:
  Keep all backups
  Keep Last
  Keep Daily
  Keep monthly
  Keep Hourly
  Keep Weekly
  Keep yearly


 > Run now 
  
```
