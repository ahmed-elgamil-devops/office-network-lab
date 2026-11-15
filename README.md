# Office Network Lab (Cisco Packet Tracer)

A small office network with VLANs, DHCP, inter-VLAN routing, a guest Wi-Fi ACL and documented troubleshooting.

## Design

| VLAN | Name | Subnet | Gateway |
| --- | --- | --- | --- |
| 10 | Staff | 192.168.10.0/24 | 192.168.10.1 |
| 20 | Guest Wi-Fi | 192.168.20.0/24 | 192.168.20.1 |
| 30 | Printers | 192.168.30.0/24 | 192.168.30.1 |
| 99 | Management | 192.168.99.0/24 | 192.168.99.1 |

Devices: 1 router (router-on-a-stick), 1 switch, 4 PCs, 1 printer, 1 wireless access point, 1 server.

## Tasks

1. Create the VLANs on the switch and assign access ports.
2. Trunk port to the router; create sub-interfaces for each VLAN.
3. DHCP pools on the router for VLANs 10 and 20; static IPs for printers.
4. ACL: guests (VLAN 20) can reach the internet only, not the staff or printer VLANs.
5. Wi-Fi: SSID `Staff` on VLAN 10 with WPA2, SSID `Guest` on VLAN 20.
6. Test: PCs get DHCP addresses, staff can print, guests cannot ping staff PCs.
7. Troubleshoot two faults on purpose (wrong VLAN on a port, missing trunk) and write how you found them.

Save the `.pkt` file here ; the router and switch configs are in `configs/`.
