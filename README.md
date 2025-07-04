# TELE 5360 – Internet Protocols and Architecture

# Lab Series README

## Author: Jeevanandh Ravi
## Instructor: Prof. Rajiv Shridhar
## Student ID: 002313120
## Semester: Spring 2025

## Overview
This README provides guidance for the set of lab reports submitted for TELE 5360, covering network configuration, troubleshooting, and protocol implementation. Each lab builds on foundational networking concepts, focusing on OSPF, BGP, MPLS VPNs, redistribution, and route filtering.

## Lab Summaries
## LAB 1: Network Configuration

Objective:
-Configure an OSPF-based topology (R1–R6).
-Ensure R1 can reach R6 via a specific path.
-Block R6 from accessing R1’s loopback and the R1–R3 network.

Key Steps:
OSPF area assignments and interface configuration.
OSPF cost manipulation to enforce path selection.
Use of prefix lists and distribute-lists to filter routes.
Verification with ping and traceroute commands.

Results:
R1 successfully reaches R6 through the intended path.
R6 is unable to access R1’s loopback or the R1–R3 subnet.
OSPF summarization and filtering optimize routing tables.

## LAB 2: Network Troubleshooting

Objective:
Diagnose and resolve multi-protocol connectivity issues (OSPF, EIGRP).

Key Issues & Fixes:
OSPF–EIGRP Redistribution:
Resolved area mismatch and stub configuration on R4.
OSPF Adjacency:
Addressed OSPF protocol blocking on R2.
EIGRP Metric Issues:
Adjusted interface bandwidth to correct high EIGRP metrics.
General Reachability:
Ensured all routers can reach each other’s loopbacks and interfaces.

Results:
All routers achieve full connectivity.
Proper redistribution and metric tuning ensure optimal routing.

## LAB 3: Network Troubleshooting (Advanced)

Objective:
Further troubleshooting with OSPF, ISIS, and BGP.

Key Issues & Fixes:
OSPF Loopback Advertisement:
Ensured loopbacks are advertised in correct areas.
OSPF–ISIS Redistribution:
Configured redistribution with appropriate metrics.
Connectivity Verification:
Used ping to confirm reachability across all routers and interfaces.

Results:
100% success rate in connectivity tests.
All protocol redistributions function as intended.

## LAB 4: Network Configuration (MPLS VPN & BGP)

Objective:
Configure MPLS VPNs and troubleshoot BGP/OSPF issues.

Key Issues & Fixes:
BGP Neighbor Configuration:
Added missing BGP neighbor in VRF on R3.

Route-Map Filtering:
Removed a route-map injecting a “no-advertise” community on R1.

OSPF Adjacency for MPLS:
Restored OSPF adjacencies among core routers to enable label distribution.

Results:
Successful end-to-end VPN connectivity.
All BGP and OSPF sessions established and stable.

How to Use These Labs
Review the Topology:
Each lab assumes a multi-router topology with specific interface and area assignments.
Refer to the configuration snippets for interface IPs and OSPF/BGP/ISIS area numbers.
Apply Configurations Sequentially:
-Start with basic OSPF setup (Lab 1).
-Progress to redistribution and troubleshooting (Labs 2 & 3).
-Implement MPLS VPN and advanced BGP (Lab 4).

Verify Connectivity:
Use ping and traceroute to confirm reachability.
Check routing tables and protocol adjacencies after each major change.

Troubleshooting Tips:
Always check for area mismatches, missing network statements, and protocol filters.
Use show commands (show ip route, show ip ospf neighbor, show bgp, etc.) for diagnostics.

## File Structure
File Name	Description
TELE-5360_RAVI_JEEVANANDH_002313120_LAB1.pdf	OSPF configuration, path enforcement, filtering
TELE-5360_RAVI_JEEVANANDH_002313120_LAB_2.pdf	OSPF/EIGRP troubleshooting, redistribution
TELE-5360_RAVI_JEEVANANDH_002313120_LAB_3-2.pdf	Advanced troubleshooting, ISIS, BGP
TELE-5360_RAVI_JEEVANANDH_002313120_Lab4.pdf	MPLS VPN, BGP, OSPF label distribution
![image](https://github.com/user-attachments/assets/ee95852d-d9dc-4a09-9d8d-d71b325d25ff)

