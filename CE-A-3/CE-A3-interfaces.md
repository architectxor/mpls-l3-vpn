en
conf t
hostname CE-A-3

int Gig0/4
description to PE-3
ip add 192.168.100.130 255.255.255.192
no sh
exit

[[MPLS/mpls-l3-vpn/Checklist]]