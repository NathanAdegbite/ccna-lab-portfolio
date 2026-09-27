# Lab 03: Inter-VLAN Routing

## Objective

VLANs on their own only get you isolation, something has to actually move traffic between them. This lab covers the two standard ways to do that at the CCNA level, and instead of just describing the difference, I built both, starting from the same base topology, same VLANs, same IPs, same PCs, so the comparison is a fair one rather than theoretical.

- **[Router-on-a-Stick (ROAS)](./roas)**: a router with subinterfaces does the routing, over a single trunk link.
- **[SVIs on a Layer 3 Switch](./svi)**: no router at all, a Layer 3 switch routes internally through its own VLAN interfaces.

Same result both ways, PC1 (VLAN 10) reaching PC3 (VLAN 20), but the mechanism and the hardware involved are genuinely different.

## Comparison

| | Router-on-a-Stick | SVI / Layer 3 Switch |
|---|---|---|
| Devices needed | Router + switch(es) | Layer 3 switch only |
| Where routing happens | Subinterfaces on the router (`Gi0/0.10`, `Gi0/0.20`) | VLAN interfaces on the switch (`interface vlan 10`, `vlan 20`) |
| Routing enabled by default? | Yes, routers route by default | No, `ip routing` must be explicitly enabled |
| Physical links | One trunk per router | No extra physical link needed beyond the existing inter-switch trunk |
| Throughput ceiling | Limited by the router's single physical interface, all inter-VLAN traffic funnels through one link | Higher, routing happens in switch hardware (ASIC) without funneling through one port |
| Typical real-world use | Smaller networks, or where a router is already present for other reasons (WAN, VPN) | Larger networks, distribution/core layer, anywhere routing needs to scale |
| Platform used in this lab | Cisco 2911 | Cisco 3560 |

## What building both actually showed me

The most useful thing about doing this twice wasn't the config differences, both are honestly pretty short. It was that they fail differently. ROAS problems tend to show up as VLAN tagging or trunk allowed-list issues, since everything is squeezed through one physical link. The SVI version's problems were platform-specific instead, the 3560's trunk encapsulation defaulting to negotiate, and `ip routing` not being on by default the way it is on a router. Neither approach is "harder," they just have different failure modes, and knowing both means recognizing the right fix faster regardless of which one shows up on the job.

## Full Documentation

- [ROAS build: topology, config, verification, troubleshooting](./roas)
- [SVI build: topology, config, verification, troubleshooting](./svi)
