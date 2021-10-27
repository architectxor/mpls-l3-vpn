en
conf t
hostname CE-B-2

int Gig0/3
description to PE-3
ip add 172.16.20.130 255.255.255.192
no sh
exit

[[MPLS/mpls-l3-vpn/Checklist]]