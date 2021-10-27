ip vrf VRF-A
rd 4.4.4.4:777
route-target both 64500:777
exit




int Gig0/4
description to CE-A-4
ip vrf forwarding VRF-A
ip address 192.168.100.193 255.255.255.192
no sh
exit

[[MPLS/mpls-l3-vpn/Checklist]]