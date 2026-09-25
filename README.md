# Server Information
This repositories use is for documenting aspects of my servers security, storage, software, and hardware.
It's use is for keeping logs on backups, reports, and information that will help with learning more about servers and networking, while also being a vital backup of knowledge just in case anything breaks.

## System information
```
CPU    :    Intel i7 4790k
RAM    :    20GB mixed-speed ddr3
MOB    :    Gigabyte GA-H97M-D3H Micro ATX LGA1150 
HDD    :    Fujitsu 120GB 2.5" SATA 7200RPM
            Seagate Constellation 4TB SAS 7200RPM
            3x Seagate Constellation 3TB SAS 7200RPM
            2x IBM HGST 3TB SAS 7200RPM
PSU    :    650W Thermalright TR-SGFX
CASE   :    Jonsbo n4

```

<details>
<summary> Docker Services</summary>
    
### Jellyfin 

A public facing jellyfin media server.
Users must request account creation to access.
```
config is in a script
```
### Immich

A private photos app, like google photos.
No other users are to be added, but albums can be shared and downloaded by others.
```
/opt/
```
### Forjego

A public facing code base like github.
Users can view all public repos, but are not able to interact unless an account is created by an admin.
Mainly used as an alternative to github *just* for emi
```
/opt/
```
### glances dash

glances is protected and can only be accessed by emi

```
/opt/
```

</details>

TO DO:
- [ ] Add live error reporting for drives
- [ ] Add drive temperatures to glances, or new container 

<details>
<summary> Network Configuration</summary>

### Server
Server access is limited through docker containers and the network controller/network switch

```
IP ~~~.~~~.~~.72 - public network
IP ~~~.~~~.~~.73 - private network

```
NetworkControl

```
IP ~~.~~~.~~.113 
All access is heavily restricted
```

</details>

TO DO:
- [ ] Add physical public and private access through the onboard nic and PCI nic



<details>
<summary> Things to fix </summary>

|Directory                  |User                                       |Access|
|---------------------------|-------------------------------------------|------|
|/mnt/raid/media/forgejo    |DEFAULT                                    |NAN   | to be fixed

</details>

<details>
<summary> File system tree</summary>

4tb sas drive acts as a weekly backup for immich, jellyfin music, and forgejo.
```
Raid Array:
├── Backups for older media
├── media
│   ├── services 
│   ├── and 
│   ├── users
│   └── shared media
│       └── restricted private access with permission
├── shared media
│   └── restricted private access with permission
└── Boot drive backup
  

/mnt/4tb/
├── Backups
│   └── ....
......
```

</details>

<details>
<summary> Raid Info</summary>

### Information for raid scripts and backup process
```
TO BE ADDED (IN PROGRESS)
```
</details>
