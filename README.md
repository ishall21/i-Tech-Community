# i-Tech Community MikroTik Dual-WAN Load Balancer

Static GitHub Pages tool that generates a starter MikroTik RouterOS v7 PCC (Per Connection Classifier) dual-WAN load-balancing template.

## Features
- Two WAN interface and gateway inputs
- Equal or weighted PCC ratios (1:1, 2:1, 3:1, 1:2)
- Separate routing-table names
- Optional NAT masquerade rules
- Optional disabled-by-default mangle rules
- Copy generated commands or download `.rsc`
- Runs entirely in the browser; no backend

## Publish to GitHub Pages
1. Create a repository, e.g. `i-tech-community-dual-wan-load-balance`.
2. Upload `index.html` and `README.md` to the repository root.
3. Open **Settings → Pages**.
4. Select **Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
5. Wait for GitHub Pages to publish.

If your GitHub username is `ishall21`, the expected URL is:
`https://ishall21.github.io/i-tech-community-dual-wan-load-balance/`

## Critical deployment notes
- Gateway values `192.0.2.1` and `198.51.100.1` are documentation examples only. Replace them with your actual gateways.
- The generated script is a starter template, not a tested drop-in config. Existing routing tables, routes, mangle rules, NAT, FastTrack, DHCP/PPPoE WANs, VPNs, BGP sessions, and connection tracking can affect the design.
- `check-gateway=ping` only checks reachability of the configured gateway; it does not guarantee end-to-end internet health.
- Review PCC bucket mapping for the selected ratio before enabling. Existing connections may behave differently after policy changes.
- Back up the router, test on a lab device, and validate against your RouterOS v7 release before production use.

Official documentation: https://help.mikrotik.com/docs/
