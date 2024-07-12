# The Source Code of Resilient Subpath-Based NDN Transport Protocol (RNTP) for Ad-Hoc Stationary Wireless Sensor Networks

## What is the RNTP?
In the Internet of Things, ad-hoc stationary wireless sensor networks (WSNs) often grapple with significant packet losses in harsh environments, necessitating robust data transport protocols. Unfortunately, existing protocols overlook subpaths, including critical alternative routes between nodes. This oversight limits rerouting options, essential for effective congestion control and retransmission strategies. The core challenges lie in efficiently constructing and selecting reliable subpaths, crucial for network resilience. Named-data networking (NDN) enables in-network data processing and caching, fostering advanced strategy development. In response, we propose RNTP, a resilient subpath-based NDN transport protocol to minimize the end-to-end packet delivery failure rate (EEFR) and delivery time (EEDT) through streamlined processes. RNTP efficiently builds subpath routes using a single packet propagation method, and then selects the reliable subpath based on signal quality and hop count. Its congestion control operates with fast retransmission, governed by the AIMD policy in efficiently response to implicit and explicit feedback, ensuring minimal messaging. Implementation includes state transition machines with protocol adherence and correctness validation. Simulation results consistently demonstrate RNTP's superiority across various WSN setups, under significant noise interference.  For example, in a 64-node topology with 15 nodes encountering 30dB mean noise, RNTP achieves an impressive EEFR of 0.02%, EEDT of 5.54s and energy consumption per received payload packet of 0.19mWh, outperforming its comparative schemes significantly. Extensive experiments confirm RNTP’s scalability across networks ranging from 36 to 144 nodes, as the number of subpaths per hop under a bound limit, being irrelevant to network scale. These findings highlight RNTP’s effectiveness in ensuring reliable data delivery for the WSNs.

## How do I run the source code?
1. You need to download both the RNTP from github and the recent ndnSIM from https://ndnsim.net/current/. 
2. Simply copy all files of the RNTP to the ndnSIM folder in an override manner. 
3. You need to edit the rntp-config.ini file under the ndnSIM/ns-3 folder with the correct output log path and some simulation parameters. 
4. Run RNTP testers. 
cd ns-3
./waf --run scratch/rntp-sim --command-template="%s rntp-config.ini"
5. Afterwards, you can find the simulation results under the LOG_DIR directory defined in the above ini file.

 ## Paper in submission
Boyang Zhou, et al., "A Resilient Subpath-Based NDN Transport Protocol (RNTP) for Ad-Hoc Stationary Wireless Sensor Networks," in IEEE Internet-of-Things Journal, 2024.
 
We are looking forward to new project opportunity in making the RNTP growing up. 

 *********************************************************************************
This work is licensed under CC BY-NC-SA 4.0
(https://creativecommons.org/licenses/by-nc-sa/4.0/).

Copyright (c) 2021-2024 Boyang Zhou @ Zhejiang Lab

This file is a part of "Resilient Subpath-Based NDN Transport Protocol (RNTP) for Ad-Hoc Stationary Wireless Sensor Networks"
(https://github.com/zhouby-zjl/rntp/).

 **********************************************************************************
