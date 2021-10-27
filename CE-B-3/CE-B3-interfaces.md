en
conf t
hostname CE-B-3

int Gig0/3
description to PE-5
ip add 172.16.20.194 255.255.255.192
no sh
exit

[[MPLS/mpls-l3-vpn/Checklist]]