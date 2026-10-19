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

### Immich

Emi's private photos app

### Forjego

A public facing code base
Users can view all public repos, but are not able to interact unless an account is created by an admin.

### Protected Services
dash, container control, vpn - All are private

</details>

TO DO:
- [ ] Add live error reporting for drives
- [ ] Add drive temperatures to glances, or new container
- [ ] Add network switch control from other pc to layer 3 switch

<details>
<summary> Network Configuration</summary>

Router - Layer 2/1 switch - Layer 3 switch

</details>

TO DO:
- [ ] Update physical Switch config and VLAN systems. 


<details>
<summary> File system tree</summary>

4tb is a weekly backup for ALL non replaceable media.

```
Raid Array:
├── Backups for older media
├── media
│   ├── services 
│   ├── and 
│   ├── users
│   └── shared media
│       └── 
├── shared media
│   └── 
└── Boot drive backup
  

/mnt/4tb/
├── Backups
│   └── Raid Array
......
```

</details>

<details>
<summary> Raid Info</summary>
A systemd service is used on a weekly timer to back up contents.

</details>

TO DO:
- [ ] Update Script and put config here (it shouldn't be a vulnerability lol)
