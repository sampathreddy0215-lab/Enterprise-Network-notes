# BGP Path Selection Process

## Overview

BGP selects the best path when multiple routes to the same destination exist.

## BGP Best Path Order

1. Highest Weight
2. Highest Local Preference
3. Locally Originated Route
4. Shortest AS Path
5. Lowest Origin Type
6. Lowest MED
7. eBGP over iBGP
8. Lowest IGP Metric to Next Hop
9. Oldest Path
10. Lowest Router ID

## Verification Commands

### Cisco

show ip bgp
show ip bgp summary
show ip route bgp

### Juniper

show route protocol bgp
show bgp summary

## Common Troubleshooting Scenarios

- Route not preferred due to Local Preference
- Incorrect AS Path prepending
- MED influencing route selection
- Missing next-hop reachability
- Route filtering policies blocking prefixes

## Best Practices

- Use Local Preference for outbound path control
- Document routing policies
- Monitor BGP neighbor stability
- Validate route advertisements after changes
- Implement route filtering and prefix limits
