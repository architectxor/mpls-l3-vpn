end
! Show information about LDP-neighbors
show mpls ldp neighbor 1.1.1.1
show mpls ldp neighbor 2.2.2.2
show mpls ldp neighbor 4.4.4.4
show mpls ldp neighbor 5.5.5.5
show mpls ldp neighbor 6.6.6.6

! Show LFIB table
show mpls forwarding-table


! Show information about specified FEC
show mpls forwarding-table 1.1.1.1 32
show mpls forwarding-table 2.2.2.2 32
show mpls forwarding-table 4.4.4.4 32
show mpls forwarding-table 5.5.5.5 32
show mpls forwarding-table 6.6.6.6 32

! Show information about label distribution
show mpls ldp bindings

! Show information about active LSP for specified FEC (look for "inuse")
show mpls ldp binding 1.1.1.1 32
show mpls ldp binding 2.2.2.2 32
show mpls ldp binding 4.4.4.4 32
show mpls ldp binding 5.5.5.5 32
show mpls ldp binding 6.6.6.6 32

! Show information about backward LSP for FEC defined on
show ip cef detail | begin 1.1.1.1
show ip cef detail | begin 2.2.2.2
show ip cef detail | begin 4.4.4.4
show ip cef detail | begin 5.5.5.5
show ip cef detail | begin 6.6.6.6
