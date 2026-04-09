# Network Configuration

```
- Network IP configuration for proxmox host
- DNS configuration
```

## Basic Network setup
```
- Proxmox WebUI
    > Host-01
        > System
            > Network [Add/modify the IP details]
        > DNS
            > Edit [Add/update new dns details]

- Apply Configuration
```

## Additional options to create Network
```
- Proxmox WebUI
    > Host-01
        > System
            > Network
                > Create
                    - Linux Bridge [If you want to create , its required additional physical NIC]
                    - Linux Bond
                    - Linux VLAN
```

## Create new Linux bridge vmbr-2
```
- Proxmox WebUI
    > Host-01
        > System
            > Network
                > Create
                    - Linux Bridge
                      Name: vmbr2
                      Rest of configuration blank
- Apply Configuration
```

## Use new create Linux-Bridge network between the VMs


```
> Create 2 Vms
> VM01
> VM02

>VM01
> Edit the nework
> Choose Vm > Network > Edit
> Change the bridge [vmbr-2]
> Assign some static IP [172.10.10.101]

> Do same for VM02
> Assign some static IP [172.10.10.102]

> test the connection between 2 vms 
```
