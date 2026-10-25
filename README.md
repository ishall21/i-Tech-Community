# i-Tech Community — MikroTik 4-WAN Routing Method Selector

A static GitHub Pages tool that generates starter MikroTik RouterOS v7 configurations for four WANs.

## Selectable methods
- **PCC Method:** connection-based load balancing with configurable bucket ratios, policy routing tables, mangle rules, and optional NAT.
- **Recursive Method:** probe-based WAN failover using per-WAN probe host routes and distance-based recursive default routes. This is failover, not PCC load balancing.

## Features
- Four WAN interface and IPv4 gateway inputs
- Four independent recursive probe IP inputs
- PCC ratios: 1:1:1:1, 2:1:1:1, 1:2:1:1, 1:1:2:1, 1:1:1:2, 2:2:1:1, 2:2:2:1, and 3:2:1:1
- Optional NAT masquerade rules
- Optional disabled-by-default PCC mangle rules
- Script preview auto-displays on page load and refreshes whenever any field or option changes
- Generate, copy, and download generated `.rsc` (invalid inputs are blocked)
- Browser-only; no backend

## GitHub Pages deployment
1. Create repository `i-tech-community-four-wan-routing-method-selector`.
2. Upload `index.html` and `README.md` to the repository root.
3. Open **Settings → Pages**.
4. Select **Deploy from a branch**, choose `main` and `/(root)`, then save.

Expected URL for GitHub user `ishall21`:
`https://ishall21.github.io/i-tech-community-four-wan-routing-method-selector/`

## Important
Prefilled gateway IPs are documentation examples only; replace them with your real WAN gateways. Recursive mode is a failover template, not load balancing. Use four stable, unique probe IPs that respond to ICMP and ensure each probe host route truly exits only through its intended WAN. This is a starter template, not a verified drop-in configuration. Review duplicate routes, DHCP/PPPoE WAN handling, PCC mangle order, FastTrack, NAT, VPN/BGP exceptions, recursive route scope/target-scope, and probe behavior. Back up and test on a lab router before production deployment.

Official documentation: https://help.mikrotik.com/docs/
