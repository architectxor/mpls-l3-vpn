router ospf 10
router-id 2.2.2.2
network 10.0.0.0 0.255.255.255 area 0
network 2.2.2.2 0.0.0.0 area 0
network 192.168.100.64 0.0.0.63 area 0
network 172.16.20.0 0.0.0.127 area 0
exit

int Gig0/0
ip ospf cost 10
ex

int Gig0/1
ip ospf cost 8
ex

int Gig0/2
ip ospf cost 10
ex

[[MPLS/mpls-l3-vpn/Checklist]]