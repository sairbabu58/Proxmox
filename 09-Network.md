## Network Configuration

```
- Network IP configuration for proxmox host
- DNS configuration
```


```
- Proxmox WebUI
    > Host-01
        > System
            > Network [Add/modify the IP details]
        > DNS
            > Edit [Add/update new dns details]

- Apply Configuration
```


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
