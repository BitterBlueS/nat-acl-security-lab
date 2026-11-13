# Test Cases


## Approach
A final set of regression runs against the completed configuration with NAT translations and ACL counters cleared beforehand. Each test covers allowed or denied flows tied to specific mechanisms


## Results

| # | Test | Expected | Result |
| 1 | PC1 to Outside-PC ping | Allowed (PAT) | pass/fail |
| 2 | PC2 to Outside-PC ping | Allowed (PAT, shared address) | |
| 3 | Outside-PC to http://203.0.113.3 | Allowed (static NAT) | |
| 4 | Admin-PC SSH to R1 | Allowed | |
| 5 | Outside-PC to 192.168.10.10 | Denied (private address) | |
| 6 | Outside-PC ping to 203.0.113.3 | Denied (rule 80) | |
| 7 | Outside-PC SSH to R1 | Denied (rule 60) | |
| 8 | Outside-PC Telnet to R1 | Denied (rule 70) | |
| 9 | PC1 SSH to R1 | Denied (MGMT-ACCESS) | |
| 10 | Outside-PC to PC1 | Denied (no translation ) | |

## Verification


## Additional Notes

