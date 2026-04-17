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

```
> Proxmox web console
> DataCenter
> SDN
> Zones  [Smiple | VLAN | QinQ | VXLAN | EVPN]


```

