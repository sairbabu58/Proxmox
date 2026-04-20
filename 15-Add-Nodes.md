# How to add additional nodes to Proxmox cluster

```
> Install Proxmox on both cluster
> Configure the networks
```
### Create Proxmox cluster
```
> Access the Proxmox one node https://192.168.0.100:8006
> DataCenter
> Cluster
> Create Cluster
  Name: j2c-cluster
> Create
```

### Add other nodes to proxmox cluster

```
> Collect the token from main cluster node
> Login second proxmox webui https://192.168.0.101:8006
> Cluster
> Join Cluster
> Paste the details.
> Create 
```
