en
conf t
hostname PE-2

int loopback 0
ip add 2.2.2.2 255.255.255.255
no sh
ex

int Gig0/0
ip add 10.2.3.2 255.255.255.0
no sh
ex

int Gig0/1
ip add 10.2.6.2 255.255.255.0
no sh
ex

int Gig0/2
ip add 10.1.2.2 255.255.255.0
no sh
ex

int Gig0/3
ip add 172.16.20.1 255.255.255.128
no sh
ex

int Gig0/4
ip add 192.168.100.65 255.255.255.192
no sh
ex


