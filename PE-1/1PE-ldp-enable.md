
! CEF technology for packet processing
ip cef

! Activating MPLS and LDP globally
mpls ip

! Setting LSR ID
mpls ldp router-id Loopback 0 force

int Gig0/0
mpls ip
no sh
ex

int Gig0/1
mpls ip
no sh
ex

int Gig0/2
mpls ip
no sh
ex

int Gig0/4
mpls ip
no sh
ex

[[MPLS/mpls-l3-vpn/Checklist]]