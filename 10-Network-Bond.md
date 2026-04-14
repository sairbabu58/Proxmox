# Bond Network Configuration

> Required 2 physical NIC on the server
> Managed Switch
> Configure the bond0
> Add bondo to Linux Bridge - vmbr0 or vmbr1


```
-> Proxmox WebUI
    > Choose the host
    > System
    > Network
      > Create
      > Linux Bond [Create]
        > Name: bond0
        > Slave: [Physical nic-1 name [space] nic-2 name | ensp1s0 ensp2s1 ]
        > Mode: balance-rr [active-backup, balance-xor, broadcast, balance-tlb]
note: you may wish to configure static/dhcp ip for bond
```


