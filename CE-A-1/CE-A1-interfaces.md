en
conf t
hostname CE-A-1

int Gig0/4
description to PE-1
ip add 192.168.100.2 255.255.255.192
no sh
exit

[[MPLS/mpls-l3-vpn/Checklist]]