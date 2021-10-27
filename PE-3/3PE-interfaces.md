en
conf t
hostname PE-3

int loopback 0
ip add 3.3.3.3 255.255.255.255
no sh
ex

int Gig0/0
ip add 10.2.3.3 255.255.255.0
no sh
ex

int Gig0/1
ip add 10.3.4.3 255.255.255.0
no sh
ex

int Gig0/2
ip add 10.3.6.3 255.255.255.0
no sh
ex

int Gig0/3
ip add 172.16.20.129 255.255.255.192
no sh
ex

int Gig0/4
ip add 192.168.100.129 255.255.255.192
no sh
ex

[[MPLS/mpls-l3-vpn/Checklist]]