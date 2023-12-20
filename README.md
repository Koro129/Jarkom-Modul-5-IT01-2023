# Jarkom-Modul-5-IT01-2023
## Topologi
![image](https://github.com/Koro129/Jarkom-Modul-5-IT01-2023/assets/113784446/c19227a0-df85-4837-86b9-bf1cd504dc62)
## Rute
![image](https://github.com/Koro129/Jarkom-Modul-5-IT01-2023/assets/113784446/ae516c16-82a1-42c5-8716-f89cffb1f066)
## VLSM
![image](https://github.com/Koro129/Jarkom-Modul-5-IT01-2023/assets/113784446/4f96aa56-48f9-4062-bc20-0a0a8f598881)
![vlsm tree](https://github.com/Koro129/Jarkom-Modul-5-IT01-2023/assets/113784446/fc9e836f-057d-4671-b957-3832f2947d3e)
## Konfigurasi
### Aura
```
auto eth0
iface eth0 inet static
    address 192.168.122.2
    netmask 255.255.255.0
    gateway 192.168.122.1


auto eth1
iface eth1 inet static
    address 10.64.14.129
    netmask 255.255.255.252

auto eth2
iface eth2 inet static
    address 10.64.14.133
    netmask 255.255.255.252
```
### Heiter
```
auto eth0
iface eth0 inet static
    address 10.64.14.130
    netmask 255.255.255.252
    gateway 10.64.14.129
    up echo nameserver 192.168.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
    address 10.64.0.1
    netmask 255.255.248.0
    up echo nameserver 192.168.122.1 > /etc/resolv.conf

auto eth2
iface eth2 inet static
    address 10.64.8.1
    netmask 255.255.252.0
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```
### Frieren
```
auto eth0
iface eth0 inet static
    address 10.64.14.134
    netmask 255.255.255.252
    gateway 10.64.14.133
    up echo nameserver 192.168.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
    address 10.64.14.137
    netmask 255.255.255.252
    up echo nameserver 192.168.122.1 > /etc/resolv.conf

auto eth2
iface eth2 inet static
    address 10.64.14.141
    netmask 255.255.255.252
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```
### Himmel
```
auto eth0
iface eth0 inet static
    address 10.64.14.142
    netmask 255.255.255.252
    gateway 10.64.14.141
    up echo nameserver 192.168.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
    address 10.64.12.1
    netmask 255.255.254.0
    up echo nameserver 192.168.122.1 > /etc/resolv.conf

auto eth2
iface eth2 inet static
    address 10.64.14.1
    netmask 255.255.255.128
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```
### Fern
```
auto eth0
iface eth0 inet static
    address 10.64.14.2
    netmask 255.255.255.128
    gateway 10.64.14.1 
    up echo nameserver 192.168.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
    address 10.64.14.145
    netmask 255.255.255.252
    up echo nameserver 192.168.122.1 > /etc/resolv.conf

auto eth2
iface eth2 inet static
    address 10.64.14.149
    netmask 255.255.255.252
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```
### Sein
```
auto eth0
iface eth0 inet static
    address 10.64.8.2
    netmask 255.255.252.0
    gateway 10.64.8.1
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```
### Stark
```
auto eth0
iface eth0 inet static
    address 10.64.14.138
    netmask 255.255.255.252
    gateway 10.64.14.137
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```
### Richter
```
auto eth0
iface eth0 inet static
    address 10.64.14.146
    netmask 255.255.255.252
    gateway 10.64.14.145
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```
### Revolte
```
auto eth0
iface eth0 inet static
    address 10.64.14.150
    netmask 255.255.255.252
    gateway 10.64.14.149
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```
### Client
```
auto eth0
iface eth0 inet dhcp
```
## Routing
### Aura
```
route add -net 10.64.0.0 netmask 255.255.248.0 gw 10.64.14.130
route add -net 10.64.8.0 netmask 255.255.252.0 gw 10.64.14.130

route add -net 10.64.14.136 netmask 255.255.255.252 gw 10.64.14.134
route add -net 10.64.14.140 netmask 255.255.255.252 gw 10.64.14.134
route add -net 10.64.12.0 netmask 255.255.254.0 gw 10.64.14.134
route add -net 10.64.14.0 netmask 255.255.255.128 gw 10.64.14.134
route add -net 10.64.14.144 netmask 255.255.255.252 gw 10.64.14.134
route add -net 10.64.14.148 netmask 255.255.255.252 gw 10.64.14.134
```
### Frieren
```
route add -net 10.64.12.0 netmask 255.255.254.0 gw 10.64.14.142
route add -net 10.64.14.0 netmask 255.255.255.128 gw 10.64.14.142
route add -net 10.64.14.144 netmask 255.255.255.252 gw 10.64.14.142
route add -net 10.64.14.148 netmask 255.255.255.252 gw 10.64.14.142
```
### Himmel
```
route add -net 10.64.14.144 netmask 255.255.255.252 gw 10.64.14.2
route add -net 10.64.14.148 netmask 255.255.255.252 gw 10.64.14.2
```
## DHCP
### Revolte (Server)
```
apt-get update
apt-get install isc-dhcp-server -y

echo 'INTERFACES="eth0"' > /etc/default/isc-dhcp-server

echo '#eth0
subnet 10.64.14.148 netmask 255.255.255.252{
}
# TurkRegion
subnet 10.64.0.0 netmask 255.255.248.0 {
    range 10.64.0.2 10.64.7.254;
    option routers 10.64.0.1;
    option broadcast-address 10.64.7.255;
    option domain-name-servers 10.64.14.146;
    default-lease-time 180;
    max-lease-time 5760;
}

# GrobeForest
subnet 10.64.8.0 netmask 255.255.252.0 {
    range 10.64.8.3 10.64.11.254;
    option routers 10.64.8.1;
    option broadcast-address 10.64.11.255;
    option domain-name-servers 10.64.14.146;
    default-lease-time 180;
    max-lease-time 5760;
}

# LaubHills
subnet 10.64.12.0 netmask 255.255.254.0 {
    range 10.64.12.2 10.64.13.254;
    option routers 10.64.12.1;
    option broadcast-address 10.64.13.255;
    option domain-name-servers 10.64.14.146;
    default-lease-time 180;
    max-lease-time 5760;
}

# SchwerMountain
subnet 10.64.14.0 netmask 255.255.255.128 {
    range 10.64.14.3 10.64.14.126;
    option routers 10.64.14.1;
    option broadcast-address 10.64.14.127;
    option domain-name-servers 10.64.14.146;
    default-lease-time 180;
    max-lease-time 5760;
}' > /etc/dhcp/dhcpd.conf

service isc-dhcp-server restart
```
### Himmel & Heiter (Relay)
```
apt-get update
apt-get install isc-dhcp-relay -y
service isc-dhcp-relay start

echo 'SERVERS="10.64.14.150"  
INTERFACES="eth0 eth1 eth2"
' > /etc/default/isc-dhcp-relay

echo 'net.ipv4.ip_forward=1' > /etc/sysctl.conf

service isc-dhcp-relay restart
```
## DNS
`````
apt-get update
apt-get install bind9 -y

echo 'options {
    forwarders {
        192.168.122.1;
    };
    auth-nxdomain no;
    allow-query{any;};
    listen-on-v6 { any; };

};

' > /etc/bind/named.conf.options

service bind9 restart
```
## 1
### Aura
```
iptables -t nat -A POSTROUTING -s 10.64.0.0/20 -o eth0 -j SNAT --to-source 192.168.122.2
```
## 2
```
iptables -A INPUT -p tcp --dport 8080 -j ACCEPT
iptables -A INPUT -p tcp -j DROP
iptables -A INPUT -j DROP
```
## 3
```
iptables -A INPUT -p icmp -m connlimit --connlimit-above 3 --connlimit-mask 0 -j DROP
```
## 4
```
iptables -A INPUT -p tcp --dport 22 -s 192.168.1.0/24 -j ACCEPT
iptables -A INPUT -p tcp --dport 22 -j DROP
```
## 5
```
iptables -A INPUT -m time --timestart 08:00 --timestop 16:00 --days Mon,Tue,Wed,Thu,Fri -j ACCEPT
```
## 6
```
iptables -A INPUT -m time --timestart 12:00 --timestop 13:00 --days Mon,Tue,Wed,Thu -j DROP
iptables -A INPUT -m time --timestart 11:00 --timestop 13:00 --days Fri -j DROP
```
## 8
```
iptables -A INPUT -s 10.64.14.148/30 -m time --datestop 2024-02-15T23:59:59 -j DROP
```
## 9
```
iptables -A INPUT -p tcp --dport 1:65535 -m recent --set --name PORTSCAN
iptables -A INPUT -p tcp --dport 1:65535 -m recent --update --seconds 600 --hitcount 20 --rttl --name PORTSCAN -j DROP
```
Tutup dengan
```
iptables -A INPUT -j DROP
```
