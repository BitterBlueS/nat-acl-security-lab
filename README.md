# NAT ACL & Security Lab
Cisco Packet Tracer lab using NAT overload (PAT) and static NAT with ACL-based security controls, logging, and structured traffic testing.

Built as a self-directed project to develop hands-on experience with core network edge security tasks: configuring static NAT and NAT overload (PAT) on a Cisco edge router, restricting management and inbound traffic with ACLs, and validating the configuration with structured allowed and denied test cases in Cisco Packet Tracer.


## Environment
- Cisco Packet Tracer
- Topology: Simple top-down topology with an internal and external network. Two opposing routers representing the internal router of the corporate network and the other the ISP provider. An endhost beyond the ISP router to represent some external user. A switch for the internal network to connect endhosts and servers to the router and connect to the 'internet.' One web server, two regular end users, one admin end user, and a syslog server that I used to verify logging capabilities.


## Contents
Build Documentation
- [Topology Addressing](docs/01-topology-addressing.md)
- [Static NAT](docs/02-static-nat.md)
- [NAT Overload & PAT](docs/03-nat-overload-pat.md)
- [ACL Security Controls](docs/04-acl-security-controls.md)
- [Logging](docs/05-logging.md)
- [Test Cases](docs/06-test-cases.md)


## What This Covers
- NAT: static NAT exposing an internal web server at a fixed public address, and PAT (overload) letting multiple inside hosts share a single public address for outbound access to the
- ACLs: a standard ACL on the VTY lines limiting router management to the trusted admin host, and an extended ACL on the outside interface permitting only HTTP traffic to the exposed server plus return traffic for inside-initiated connections
- Logging and verification: syslog and NAT debug output, with ACL enforcement confirmed through match counters and Simulation mode checks
- Testing: ten structured test cases covering allowed and denied flows, each tied to the NAT translation or ACL rule that decides it
- Documentation: each build phase includes real setup steps and actual issues encountered along the way (not idealized writeups), including simulator limitations


### Status
Complete 
WSL2 functioning

