router bgp 64500
neighbor AS64500 peer-group
neighbor AS64500 remote-as 64500
neighbor AS64500 update-source Loopback 0
neighbor AS64500 next-hop-self
neighbor 1.1.1.1 peer-group AS64500
neighbor 2.2.2.2 peer-group AS64500
neighbor 3.3.3.3 peer-group AS64500
neighbor 4.4.4.4 peer-group AS64500
neighbor 6.6.6.6 peer-group AS64500

[[MPLS/mpls-l3-vpn/Checklist#Configure Multiprotocol BGP support]]