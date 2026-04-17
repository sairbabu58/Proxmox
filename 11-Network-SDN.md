# Install and configure Proxmox SDN

### Preparation and validation 
```
https://pve.proxmox.com/pve-docs/chapter-pvesdn.html

> all the pve nodes
$ apt update
$ apt install libpve-network-perl

$ cat /etc/network/interfaces
....
/etc/network/interfaces.d/* [this should existing]

$ source /etc/network/interfaces.d/*

$ apt update
$ apt install dnsmasq
# disable default instance
$ systemctl disable --now dnsmasq

$ apt update
$ apt install frr-pythontools
$ systemctl enable frr.service
```


### SDN Configuration

#### Zone
```
> Proxmox web console
> DataCenter
> SDN
> Zones [Simple | VLAN | QinQ | VXLAN | EVPN]
> Create [Simple]
  > ID : internal-zone
  > MTU: auto
  > Nodes: all
  > IPAM: pve 
  > DNS Server: [your dns server to resolve name, else leave blank to get local dns]
  > Reverse DNS:
  > DNS Zone:
  > Automatic DHCP [checked]
  > Add
```
#### VNet

```
> Proxmox web console
> DataCenter
> SDN
> VNet
> Create
  > Name: internal-VNet-dev
  > Alias:
  > Zone: internal-zone
  > Tag: [nothing]
  > VLAN Aware: [nothing]
  > Create
```

#### Subnets [VNet]
```
> Proxmox web console
> DataCenter
> SDN
> VNet
  > Choose created vnet
  > [Subnet Tab]
  > Create
    > Subnet: 10.10.10.0/24
    > Gataway: 10.10.10.1
    > SNAT: [checked]
    > DNS Zone Prefix: [nothing]

##DHCP Configuration
    > DHCP Range
    > Add
    > Start Addr: 10.10.10.100
    > End Addr: 10.10.10.200
    > ok 
```

Note: The status looks new, How to apply it

```
> Proxmox web console
> DataCenter
> SDN
> Apply
```

#### Validation

```
> Proxmox web console
> DataCenter
> SDN
> IPAM
```


#### Assign new Ip to VM/Container

```
> Proxmox webui
> VM/COntainer
> Network
> Bridge: [VNet name]
```

#### Validation and get the VM new IP Address

```
> Proxmox web console
> DataCenter
> SDN
> IPAM
```
