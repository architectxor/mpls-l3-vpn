address-family ipv4 vrf VRF-A
redistribute connected
exit

address-family ipv4 vrf VRF-B
redistribute connected
exit

[[MPLS/mpls-l3-vpn/Checklist]]