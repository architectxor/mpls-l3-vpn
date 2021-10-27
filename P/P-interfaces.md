en
conf t
hostname P

int loopback 0
description local loopback
ip add 6.6.6.6 255.255.255.255
no sh
ex

int Gig0/0
description to PE-1
ip add 10.1.6.6 255.255.255.0
no sh
ex

int Gig0/1
description to PE-2
ip add 10.2.6.6 255.255.255.0
no sh
ex

int Gig0/2
description to PE-3
ip add 10.3.6.6 255.255.255.0
no sh
ex

int Gig0/3
description to PE-4
ip add 10.4.6.6 255.255.255.0
no sh
ex

int Gig0/4
description to PE-5
ip add 10.5.6.6 255.255.255.0
no sh
ex

[[MPLS/mpls-l3-vpn/Checklist]]