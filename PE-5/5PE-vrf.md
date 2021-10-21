ip vrf VRF-A
rd 5.5.5.5:777
route-target both 64500:777
exit

ip vrf VRF-B
rd 5.5.5.5:888
route-target both 64500:888
exit

int Gig0/3
description to CE-B-3
ip vrf forwarding VRF-B
ip address 172.16.20.193 255.255.255.192
exit
