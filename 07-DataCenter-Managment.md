# PDM Proxmox Datacenter Managment

This is a single Web-UI interface to manage multiple PVE. like vSphere

```
-> Create a VM over Proxmox
-> Install the proxmox Datacenter Managment
-> Add proxmox Hosts/PVE
```
### How to add proxmox hosts

```
-> login to PDM
-> https://ip:8443
-> Dashboard
-> Remotes
-> Add
-> probe remote
    Server Address: 10.10.0.100:8006
    Fingerprint: <add the PVE Certificate>
        - Login to PVE
        - System > Certificate >  pve.ssl.pem
-> Setting
    RemoteID: pve1
    user: root
    Password:
-> Endpoint
    hostname
    10.10.0.100:8006

```
