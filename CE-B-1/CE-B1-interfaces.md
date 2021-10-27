en
conf t
hostname CE-B-1

int Gig0/3
description to PE-2
ip add 172.16.20.2 255.255.255.128
no sh
exit

[[MPLS/mpls-l3-vpn/Checklist]]