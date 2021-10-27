en
conf t
hostname CE-A-4

int Gig0/4
description to PE-4
ip add 192.168.100.194 255.255.255.192
no sh
exit

[[MPLS/mpls-l3-vpn/Checklist]]