### Integrade IDM server on Proxmox

```
-> Cluster - Permission - Realms - Add - Ldap
 Realme: cloud-lab.j2ctechnologies.intern
 BaseDomainName: cn=users,cn=accounts,dc=cloud-lab,dc=j2ctechnologies,dc=intern
 User Attr: uid

 Server: idm.cloud-lab.j2ctechnologies.intern
```

**Sync option**
```
Bind User: uid=admin,cn=users,cn=accounts,dc=cloud-lab,dc=j2ctechnologies,dc=intern
Bind Password:
Email Attr: mail

User Casses: person,user
Group Casses: groupOfNames,posixGroup
User Filter: (&(objectClass=person)(memberOf=cn=infra-admin,cn=groups,cn=accounts,dc=cloud-lab,dc=j2ctechnologies,dc=intern))
           : memberOf=cn=infra-*
Group Filter: (&(objectClass=groupofnames))
Scope: user and group
```
