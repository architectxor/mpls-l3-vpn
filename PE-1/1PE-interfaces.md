en
conf t
hostname PE-1

int loopback 0
ip add 1.1.1.1 255.255.255.255
no sh
ex

int Gig0/0
ip add 10.1.6.1 255.255.255.0
no sh
ex

int Gig0/1
ip add 10.1.5.1 255.255.255.0
no sh
ex

int Gig0/2
ip add 10.1.2.1 255.255.255.0
no sh
ex

int Gig0/4
ip add 192.168.100.1 255.255.255.192
no sh
ex