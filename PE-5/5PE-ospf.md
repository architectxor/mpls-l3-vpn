router ospf 10
router-id 5.5.5.5
network 10.0.0.0 0.255.255.255 area 0
network 5.5.5.5 0.0.0.0 area 0
network 172.16.20.192 0.0.0.63 area 0
exit

int Gig0/1
ip ospf cost 10
ex

int Gig0/2
ip ospf cost 10
ex

int Gig0/4
ip ospf cost 8
ex

[[MPLS/mpls-l3-vpn/Checklist]]