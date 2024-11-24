
# BIBLIA SACRA CONFIGURATIONUM RETIACULUM
## The Bible of Network Configurations

---

## EVANGELIUM GODWINUS / Gospel of Godwin
### The Invocation of Initialization:
*"Glory to the Omnissiah; let the network be set alight with divine packets!"*

### Initial Configurations
```
enable
configure terminal
banner motd #
***********************************************************
=][= IN THE NAME OF THE OMNISSIAH, ACCESS IS PROHIBITED! =][=
***********************************************************
#
host [name]
enable secret [password]
service password-encryption
```

### Line Configurations: The Litany of Line Sanctity
```
line con 0
password [password]
login
exec-timeout [min] [sec]
line vty 0 15
password [password]
login local
exec-timeout [min] [sec]
transport input ssh
```

### SSH Configuration: The Rite of Secure Communication
```
security passwords min-length [length]
ip domain-name [name]
crypto key generate rsa general-keys modulus [bits]
username [username] secret [password]
login block-for [seconds] attempts [number of attempts] within [seconds]
ip ssh version 2
```

### Interface Configurations: The Canticle of Connectivity
```
interface [int]
ip address [ipv4 add] [subnet]
ipv6 address [ipv6/prefix]
ipv6 address [ipv6] link-local
ipv6 rip [name] enable
no shut
ip helper-address [ip add of router int]
```

### Static Routes (IPv4): The Path of Righteous Packets
```
ip route 0.0.0.0 0.0.0.0 [exit int]
```

### Static Routes (IPv6): The Sacred Pathway of ::/0
```
ipv6 unicast-routing
ipv6 route ::/0 [exit int]
```

### Dynamic Routing (IPv4): Chant of Redistribution
```
router rip
version 2
no auto-summary
redistribute [protocol]
network [network add]
```

### Dynamic Routing (IPv6): Hymn of the IPv6 Routes
```
ipv6 router rip [name]
redistribute [protocol]
```

### DHCP Configuration: Litany of the Dynamic Host
```
ip dhcp excluded-address [first ip] [last ip]
ip dhcp pool [name]
network [network add] [subnet]
default-router [ip add]
dns-server [ip add]
domain-name [name]
```

---

## EVANGELIUM ARCHIVAL / Gospel of Archival
### VLAN Configuration: The Sermon of Segmentation
```
vlan [vlan no]
name [vlan name]
```

### Interface Descriptions: The Declaration of Duty
```
interface [int]
description [desc]
duplex [full/half]
speed [speed]
mdix auto
switchport mode [access/trunk/dynamic(auto/desirable)]
switchport access vlan [vlan]
switchport trunk native vlan [vlan]
switchport trunk allowed vlan [vlan list]
mls qos trust [cos/device cisco-phone/dscp/ip-precedence]
switchport voice vlan [vlan]
```

### Router on a Stick: The Ritual of Inter-VLAN Routing
```
interface [int].[vlan no]
encapsulation dot10 [vlan no]
ip address [ip add] [subnet]
no shutdown
```

### Boot System Configuration: The Blessing of the Machine Spirit
```
boot system flash:/[path to file system]/[IOS file name]
```

### Verification Commands: Litanies of Assurance
```
show interfaces [int]
show startup-config
show running-config
show flash
show version
show history
show ip interface [int]
show ipv6 interface [int]
show mac-address-table
show ip route
show ipv6 route
show vlan
```

### Saving Changes: The Sacred Rite of Preservation
```
copy running-config startup-config
```

### Loopback Address: The Virtual Sanctum
```
interface loopback [num]
ip address [ip add.] [subnet]
```

### Ping: Testing the Holy Connection
```
ping [ip]
```

### Filters: The Art of Focused Inquiry
```
show [verification] | section [keyword]
show [verification] | include [keyword]
show [verification] | exclude [keyword]
show [verification] | begin [keyword]
```

### History Configuration: Archiving the Sacred Commands
```
terminal history size [size]
show history
```
