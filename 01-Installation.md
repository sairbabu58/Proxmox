**Download Proxmox ISO to boot your Server**

```
https://www.proxmox.com/
https://www.proxmox.com/en/downloads/proxmox-virtual-environment
```

**Download and prepare the bootable media**
```
-> Download BalenaEtcher
-> Open it
-> Flasing from file
-> Choose ProxMox Iso
-> Choose your Pendrive storage
-> Flash
```

**Boot the Server**

```
-> Go to the BISO
-> Enable the Hyper-v / VT-D
-> Choose the Boot menu
-> Choose your external pendrive and boot it
```

**Install proxmox**

```
-> Out of 3 options
-> Choose Install Proxmox VE (Terminal UI) 
-> Enter
-> I agee
-> tarhet SSD (Choose your disk)
-> Optional (Advance, choose swap  size, root vol size, data vol size, free lvm)

-> file system [ext4]
-> optional (you can also configure RAID here)

-> Country
-> Time Zone
-> keyBoard

-> Root Password
-> Confirm root Password
-> Administrator Email

-> Managment Interface
-> Hostname
-> IP Address
-> Gateway
-> DNS Server

-> Review all the details
-> Install
```
