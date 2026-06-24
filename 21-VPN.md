### How to setup and configure WireGuard  VPN

```
https://www.youtube.com/watch?v=Cs-QnRl0Qho
```

### WireGuardVPN Server Configuration

#### Create Instance
```
-> VPN
  - WireGuard
  - Instances
  - Create [+]
  - Name: WireGuardVPN
  - Puplic And private Key [Click the Setting Icon]
  - Listen Port: 51825 [51820 is default]
  - Tunnel Address: 192.168.20..1/24
  - Save
  - Apply
```
#### Create Peer Generator
```
-> VPN
  - WireGuard
  - Peer generator
  - Instance: [Auto filled] WireGuardVPN
  - Endpoint: [your internet provider Private IP- get to from ISP route details] 168.52.69.205:51825
  - Name: Client-1
  - Rest of details will get auto filled
  - Enable: [checked]
  - Apply
```
Note: some times 'what is my ipaddress is not the real Ip addredd. always get to from ISP route details page'
