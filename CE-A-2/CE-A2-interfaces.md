en
conf t
hostname CE-A-2

int Gig0/4
description to PE-2
ip add 192.168.100.66 255.255.255.192
no sh
exit

[[MPLS/mpls-l3-vpn/Checklist]]