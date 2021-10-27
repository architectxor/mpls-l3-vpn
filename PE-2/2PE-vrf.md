ip vrf VRF-A
rd 2.2.2.2:777
route-target both 64500:777
exit

ip vrf VRF-B
rd 2.2.2.2:888
route-target both 64500:888
exit

int Gig0/3
description to CE-B-1
ip vrf forwarding VRF-B
ip address 172.16.20.1 255.255.255.128
no sh
exit

int Gig0/4
description to CE-A-2
ip vrf forwarding VRF-A
ip address 192.168.100.65 255.255.255.192
no sh
exit

[[MPLS/mpls-l3-vpn/Checklist]]