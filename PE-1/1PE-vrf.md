ip vrf VRF-A
rd 1.1.1.1:777
route-target both 64500:777
exit

int Gig0/4
description to CE-A-1
ip vrf forwarding VRF-A
ip address 192.168.100.1 255.255.255.192
exit

