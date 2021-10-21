en
conf t
hostname PE-4

int loopback 0
ip add 4.4.4.4 255.255.255.255
no sh
ex

int Gig0/3
ip add 10.4.6.4 255.255.255.0
no sh
ex

int Gig0/1
ip add 10.3.4.4 255.255.255.0
no sh
ex

int Gig0/2
ip add 10.4.5.4 255.255.255.0
no sh
ex

int Gig0/4
ip add 192.168.100.193 255.255.255.192
no sh
ex

