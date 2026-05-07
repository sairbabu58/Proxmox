**How to Manage Subscription for proxmox**

```
https://syncbricks.com/how-to-disable-the-proxmox-enterprise-repository-and-enable-the-no-subscription-repository/
https://syncbricks.com/how-to-disable-the-proxmox-subscription-nag-warning/
```

```
-> Proxmox
-> Host
-> System
-> Updates
-> Repositories
-> From here you can Enable and Disable the repos

-> or Follow the above link steps

```

```
$ apt update
$ apt upgrade
$ apt full-upgrade -y 
```

**How to Disable Supscription Warning**


```
sed -Ezi.bak "s/(function ?\\(orig_cmd\\) \\{)/\\1\\n\\torig_cmd\\(\\);\\n\\treturn;/g" /usr/share/javascript/proxmox-widget-toolkit/proxmoxlib.js && systemctl restart pveproxy.service

```

**Upgrade Proxmox from 8.X to 9.X***

```
-> Upgrade to 8.3
https://syncbricks.com/how-to-upgrade-proxmox-virtual-environment-to-version-8-3/


-> Upgrade to 9.X
https://syncbricks.com/proxmox-ve-8-to-9-upgrade-guide-debian-bookworm-to-trixie/
```

**Multiple Nodes Proxmox Update**
```
-> Update the Ceph storge
-> Update all the nodes one by one 
```



### PROXMOX 9 No-Subscription repo
```
https://soporte.telecu.cloud/kb/en-us/17-proxmox/43-how-to-enable-the-no-subscription-repository-in-proxmox-ve-using-the-cli
```


