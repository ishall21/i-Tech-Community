# i-Tech Community MikroTik Triple-WAN Load Balancer

A static GitHub Pages generator for a MikroTik RouterOS v7 triple-WAN PCC (Per Connection Classifier) starter configuration.

## Features
- Three WAN interfaces and IPv4 gateways
- Equal and weighted PCC ratios: 1:1:1, 2:1:1, 1:2:1, 1:1:2, 2:2:1, and 3:2:1
- Separate policy routing tables
- Optional masquerade rules for all three WANs
- Disabled-by-default PCC mangle rules option
- Copy generated script or download an `.rsc` file
- Runs entirely in the browser

## Publish on GitHub Pages
1. Create a repository named `i-tech-community-triple-wan-load-balance`.
2. Upload `index.html` and `README.md` to the repository root.
3. Go to **Settings → Pages**.
4. Choose **Deploy from a branch**, select `main` and `/(root)`, then save.
5. Wait for the GitHub Pages deployment to finish.

Expected URL for GitHub user `ishall21`:
`https://ishall21.github.io/i-tech-community-triple-wan-load-balance/`

## Important
The prefilled gateways (192.0.2.1, 198.51.100.1, 203.0.113.1) are documentation-only example addresses. Replace them with your real gateways. This is a starter template, not a verified drop-in config. Review duplicate routes/tables, DHCP/PPPoE WAN behavior, mangle rule order, FastTrack, NAT, VPN/BGP exceptions, and end-to-end failover monitoring. Back up and test on a lab router before production use.

Official documentation: https://help.mikrotik.com/docs/
