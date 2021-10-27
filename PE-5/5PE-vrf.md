
ip vrf VRF-B
rd 5.5.5.5:888
route-target both 64500:888
exit

int Gig0/3
description to CE-B-3
ip vrf forwarding VRF-B
ip address 172.16.20.193 255.255.255.192
no sh
exit

[[MPLS/mpls-l3-vpn/Checklist]]