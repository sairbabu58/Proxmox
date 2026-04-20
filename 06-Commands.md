### Proxmox CLI Commands

```
$ pve status
$ pveperf (All details with resources)
$ pvesm status (Device disk details for all vm, container)

$ qm list (Virtual Machine list)
$ qm start <vm-id>
$ qm stop <vm-id>
$ qm reboot <vm-id>

$ qm clone <existing-node-id> <new-node-id>
$ qm clone 105 109

$ vzdump <vm-id> (backup of the Vm)
$ cd /var/lib/vz/

$ qm config <vm-id>  (Details config for the VM)

$ pct list (all container list)
$ pct enter <container-id> (login to the container)

$ lsblk
$ df -h

$ pvecm status
$ pvecm nodes

```
