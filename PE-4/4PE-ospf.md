router ospf 10
router-id 4.4.4.4
network 10.0.0.0 0.255.255.255 area 0
network 4.4.4.4 0.0.0.0 area 0
network 192.168.100.192 0.0.0.63 area 0
exit

int Gig0/3
ip ospf cost 8
ex

int Gig0/1
ip ospf cost 10
ex

int Gig0/2
ip ospf cost 8
ex
