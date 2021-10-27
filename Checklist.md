# Checklist

## First of all configure CE Equipment of customers A and B
### Configure and up interfaces
- [x] [[CE-A1-interfaces| on CE-A-1]]
- [x] [[CE-A2-interfaces| on CE-A-2]]
- [x] [[CE-A3-interfaces| on CE-A-3]]
- [x] [[CE-A4-interfaces| on CE-A-4]]
- [x] [[CE-B1-interfaces| on CE-B-1]]
- [x] [[CE-B2-interfaces| on CE-B-2]]
- [x] [[CE-B3-interfaces| on CE-B-3]]

### Configure some routing mechanism
- [x] [[CE-A1-ospf| OSPF on A1]]
- [x] [[CE-A2-ospf| OSPF on A2]]
- [x] [[CE-A3-ospf| OSPF on A3]]
- [x] [[CE-A4-ospf| OSPF on A4]]
- [x] [[CE-B1-ospf| OSPF on B1]]
- [x] [[CE-B2-ospf| OSPF on B2]]
- [x] [[CE-B3-ospf| OSPF on B3]]


#### That's all for CE's you don't need to touch it after this step at all

## Another pretty straightforward configuration is P router
- [x] [[MPLS/mpls-l3-vpn/P/P-interfaces| Configure interfaces on the Provider Core router]]
- [x] [[MPLS/mpls-l3-vpn/P/P-ospf | Configure routing on it]]
- [x] [[MPLS/mpls-l3-vpn/P/P-cef-mpls]]


## Now configure interfaces of PE
- [x] [[1PE-interfaces| on PE-1]]
- [x] [[2PE-interfaces| on PE-2]]
- [x] [[3PE-interfaces| on PE-3]]
- [x] [[4PE-interfaces| on PE-4]]
- [x] [[5PE-interfaces| on PE-5]]
- [ ] Screenshoot all this


## Configure Link-state IGP on PE
- [x] [[1PE-ospf| OSPF on PE-1]]
- [x] [[2PE-ospf| OSPF on PE-2]]
- [x] [[3PE-ospf| OSPF on PE-3]]
- [x] [[4PE-ospf| OSPF on PE-4]]
- [x] [[5PE-ospf| OSPF on PE-5]]


## Now enable LEP globally and on each interface for each PE in MPLS-domain
### It's LDP in my case
- [x] [[1PE-ldp-enable| On PE-1]]
- [x] [[2PE-ldp-enable| On PE-2]]
- [x] [[3PE-ldp-enable| On PE-3]]
- [x] [[4PE-ldp-enable| On PE-4]]
- [x] [[5PE-ldp-enable| On PE-5]]



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
- [x] `traceroute vrf VRF-A 192.168.100.1`
- [x] `traceroute vrf VRF-A 192.168.100.129`
- [x] `traceroute vrf VRF-A 192.168.100.193`
- [x] `traceroute vrf VRF-B 172.16.20.129`
- [x] `traceroute vrf VRF-B 172.16.20.193`


## Check out new labels on PE-2
- [x] Run `show mpls forwarding-table vrf VRF-B`


## Check out that there's `nolabel` on PE-5
- [x] Run `show bgp vpnv4 unicast vrf VRF-B labels`

