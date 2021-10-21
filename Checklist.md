# Checklist

## Configure addresses on all routers
- [x] [[MPLS/MPLS-lab4/PE-1/1PE-interfaces| on PE-1]]
- [x] [[MPLS/MPLS-lab4/PE-2/2PE-interfaces| on PE-2]]
- [x] [[MPLS/MPLS-lab4/PE-3/3PE-interfaces| on PE-3]]
- [x] [[MPLS/MPLS-lab4/PE-4/4PE-interfaces| on PE-4]]
- [x] [[MPLS/MPLS-lab4/PE-5/5PE-interfaces| on PE-5]]
- [x] [[MPLS/MPLS-lab4/P/P-interfaces| on P]]
- [x] [[CE-A1-interfaces| on CE-A-1]]
- [x] [[CE-A2-interfaces| on CE-A-2]]
- [x] [[CE-A3-interfaces| on CE-A-3]]
- [x] [[CE-A4-interfaces| on CE-A-4]]
- [x] [[CE-B1-interfaces| on CE-B-1]]
- [x] [[CE-B2-interfaces| on CE-B-2]]
- [x] [[CE-B3-interfaces| on CE-B-3]]
- [x] Screenshoot all this


## (Not Sure) Configure IGP on all routers
- [x] [[MPLS/MPLS-lab4/PE-1/1PE-ospf| OSPF on PE-1]]
- [x] [[MPLS/MPLS-lab4/PE-2/2PE-ospf| OSPF on PE-2]]
- [x] [[MPLS/MPLS-lab4/PE-3/3PE-ospf| OSPF on PE-3]]
- [x] [[MPLS/MPLS-lab4/PE-4/4PE-ospf| OSPF on PE-4]]
- [x] [[MPLS/MPLS-lab4/PE-5/5PE-ospf| OSPF on PE-5]]
- [x] [[MPLS/MPLS-lab4/P/P-ospf| OSPF on P]]
- [x] [[CE-A1-ospf| OSPF on A1]]
- [x] [[CE-A2-ospf| OSPF on A2]]
- [x] [[CE-A3-ospf| OSPF on A3]]
- [x] [[CE-A4-ospf| OSPF on A4]]
- [x] [[CE-B1-ospf| OSPF on B1]]
- [x] [[CE-B2-ospf| OSPF on B2]]
- [x] [[CE-B3-ospf| OSPF on B3]]


## Create VRF on all PE LSRs
- [x] [[1PE-vrf| PE-1 VRF creation]]
- [x] [[2PE-vrf| PE-2 VRF creation]]
- [x] [[3PE-vrf| PE-3 VRF creation]]
- [x] [[4PE-vrf| PE-4 VRF creation]]
- [x] [[5PE-vrf| PE-5 VRF creation]]


## Check status of VRF interfaces
- [x] Run `show ip vrf interfaces`
- [x] Screenshoot the output


## Configure Multiprotocol BGP support
- [x] [[1PE-mbgp| MBGP on PE-1]]
- [x] [[2PE-mbgp| MBGP on PE-2]]
- [x] [[3PE-mbgp| MBGP on PE-3]]
- [x] [[4PE-mbgp| MBGP on PE-4]]
- [x] [[5PE-mbgp| MBGP on PE-5]]


## Enable VPNv4 Address Family redistribution
- [x] [[1PE-vpnv4| Redistribution enable on PE-1]]
- [x] [[2PE-vpnv4| Redistribution enable on PE-2]]
- [x] [[3PE-vpnv4| Redistribution enable on PE-3]]
- [x] [[4PE-vpnv4| Redistribution enable on PE-4]]
- [x] [[5PE-vpnv4| Redistribution enable on PE-5]]


## Check out list of routers that supports specified Address Family
- [x] Run `show bgp vpnv4 unicast all summary`
- [x] Screenshoot the output


## Configure `connected` routes redistribution
- [x] [[1PE-afc-redistribution| For PE-1]]
- [x] [[2PE-afc-redistribution| For PE-2]]
- [x] [[3PE-afc-redistribution| For PE-3]]
- [x] [[4PE-afc-redistribution| For PE-4]]
- [x] [[5PE-afc-redistribution| For PE-5]]


## Check out VRF Tables
- [x] Run on 2-VRF PE `show ip route vrf VRF-A`
- [x] Run on 2-VRF PE `show ip route vrf VRF-B`

show ip route vrf VRF-A
show ip route vrf VRF-B


## Try-to-reach [from PE-2]
- [ ] `traceroute vrf VRF-A 192.168.100.1`
- [ ] `traceroute vrf VRF-A 192.168.100.129`
- [ ] `traceroute vrf VRF-A 192.168.100.193`
- [ ] `traceroute vrf VRF-B 172.16.20.129`
- [ ] `traceroute vrf VRF-B 172.16.20.193`


## Check out new labels on PE-2
- [ ] Run `show mpls forwarding-table vrf VRF-B`


## Check out that there's `nolabel` on PE-5
- [ ] Run `show bgp vpnv4 unicast vrf VRF-B labels`




## Troubleshoot traceroute
- [ ] Check PE-1 vrf routing tables
	- [x] 192.168.100.0 directly connected
	- [x] 192.168.100.64 via 2.2.2.2
	- [x] 192.168.100.128 via 3.3.3.3
	- [x] 192.168.100.192 via 4.4.4.4
	- [ ] 172.16.20.0 via 2.2.2.2
	- [ ] 172.16.20.128 via 3.3.3.3
	- [ ] 172.16.20.192 via 5.5.5.5
	- [ ] VRF B doesn't exits, because it's P-router VPN Customer B traffic
- [ ] Check PE-2 vrf routing tables
- [ ] Check PE-3 vrf routing tables
- [ ] Check PE-4 vrf routing tables
- [ ] Check PE-5 vrf routing tables


## Fixing Routers
- [ ] Remove VRF-B from PE-4 `no ip vrf VRF-B`
- [ ] Remove VRF-A from PE-5 `no ip vrf VRF-A`


## Try to define static routes between CE<->PE 
