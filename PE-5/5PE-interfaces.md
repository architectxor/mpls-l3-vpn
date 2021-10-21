en
conf t
hostname PE-5

int loopback 0
ip add 5.5.5.5 255.255.255.255
no sh
ex

int Gig0/1
ip add 10.1.5.5 255.255.255.0
no sh
ex

int Gig0/2
ip add 10.4.5.5 255.255.255.0
no sh
ex

int Gig0/4
ip add 10.5.6.5 255.255.255.0
no sh
ex

int Gig0/3
ip add 172.16.20.193 255.255.255.192
no sh
ex

