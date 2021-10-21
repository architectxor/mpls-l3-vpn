! CEF technology for packet processing
ip cef

! Activating MPLS and LDP globally
mpls ip

! Setting LSR ID
mpls ldp router-id Loopback 0 force 

! Enabling MPLS and LDP on interfaces
int Gig0/0
mpls ip
ex

int Gig0/1
mpls ip
ex

int Gig0/2
mpls ip
ex
end
