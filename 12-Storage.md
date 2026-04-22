# Storage setup and configuration 

#### Resizing Disk for VM 
```
> Choose the VM
> Hardware
> Harddisk
> Disk Action
> Resize [2]
```
#### Resizing Disk for Container

```
> Choose the Container
> Stop
> [PVE shell] pct resize 101 rootfs 20G
```


#### Integrate TrueNAS

```
> Proxmox WebUI
> DataCenter
> Storage
> Add
  > NFS
    ID: Any-Name
    Server: TrueNAS IP
    Export: /path/path-to-path
    Content: Selete one by one everythings
    Nodes: 
    Enable:
> Add
    
```
