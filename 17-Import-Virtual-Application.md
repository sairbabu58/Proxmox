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
