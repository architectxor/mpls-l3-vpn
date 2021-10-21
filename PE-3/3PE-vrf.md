ip vrf VRF-A
rd 3.3.3.3:777
route-target both 64500:777
exit

ip vrf VRF-B
rd 3.3.3.3:888
route-target both 64500:888
exit


int Gig0/3
description to CE-B-2
ip vrf forwarding VRF-B
ip address 172.16.20.129 255.255.255.192
exit

int Gig0/4
description to CE-A-3
ip vrf forwarding VRF-A
ip address 192.168.100.129 255.255.255.192
exit