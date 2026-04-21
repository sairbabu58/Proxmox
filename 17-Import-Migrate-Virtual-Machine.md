# How to import existing OVA image and create the Vms

```
> Create any kind of vms using the existing template
> Like: ova, qcow
```

## CLI process

### How to create a Vm using above template

```
> Login to pve
> Go to storage and getg the path

$ cd  /var/lib/vz
$ mkdir download
$ winscp or scp or wget the above image to this path ~/download
$ tar -xvf demp_vm.ova
$ ll

$ qm importovf <new-vm-id> <filename.ovf> <storage-name> --format <type>
$ qm importovf 301 demo_vmware.ovf local-lvm --format raw

> Update the vm CPU/Memory
> Choose the new vm 301
> Hardware
> cpu: 1
> memory: 2024
```

## Importing Existing Virtual Disk to create a vm on proxmox 

```
> Extract the OVA template or get the VMDK file
> Create a vm on PVE
> Go with all default setting and create a VM
> Noe selete the Vm and change the storage setting
> Hardware
> Remove the old Disk - Deteach - Remove

> Now do it using shell command

> cd  /var/lib/vz/path for that file
> qm importovf 302(your existing vm id) demo_vmware.demo.vmdk local-lvm --format raw
> Change the [boot order] to [DISK] from [Option]
```
