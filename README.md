# ip-aliasing-proxy-lab

## IP Aliasing setup

CLAB using ip-aliasing and proxy-arp functionality in DCs.
Configs for the devices can be seen at (e.g., for leaf1) ip-aliasing-proxy-lab/clab-ip-aliasing-proxy-lab/leaf1/config/

Diagram for the IP Aliasing functionality is shown below. Subscriber prefixes are advertised in an EVPN IFL route with a non-zero ESI. Leaf1 and Leaf2 are attached to the same layer-3 ES.

![ip-al](https://user-images.githubusercontent.com/27307831/236813352-8c1f81f7-2b36-4c56-a5cf-ae119e362683.png)

On ip-vrf-2 there is a typical ip-aliasing scenario, with a BGP PE-CE session between CE1 and leaf1's loopback. The
layer-3 ES is associated with the CE1 address.

On ip-vrf-42 there are BGP PE-CE sessions to the IRB interfaces of leaf1, leaf2 and leaf3, to demonstrate that BGP
sessions can be established to IRB addresses configured as primary.

## Proxy-ND setup

Proxy-ND along with EVPN multi-homing tested in this setup.

![proxy](https://user-images.githubusercontent.com/27307831/236814067-789a24bc-3e83-4375-93b9-bb9f707c3dfc.png)
