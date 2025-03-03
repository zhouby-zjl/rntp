# The Source Code of Resilient Subpath-Based NDN Transport Protocol (RNTP) for Ad-Hoc Stationary Wireless Sensor Networks

## What is the RNTP?
In the Internet of Things, ad-hoc stationary wireless sensor networks (WSNs) often suffer from packet losses due to harsh conditions like noise interference, necessitating robust data transport protocols. Existing protocols frequently overlook subpaths -- available routes between nodes and the sink -- essential for efficient transport. The key challenging is to construct scalable subpaths with minimal messaging and exploit them for reliable transport control. To address this challenge, we propose RNTP, a resilient subpath-based protocol leveraging named-data networking (NDN) to reduce the end-to-end packet delivery failure rate (EEFR) and delivery time (EEDT). RNTP constructs subpath routes using a single packet propagation method to identify sources. At each hop, it dynamically selects a locally reliable subpath prioritizing a balanced metric of channel quality and hop count. It adopts efficient congestion control with fast retransmission, responding to both the payload-sending events and acknowledgements from downstream nodes with minimal messaging overhead. The implementation of RNTP involves 9 executable state transition machines to ensure protocol adherence and correctness. Simulations in ndnSIM under significant noise interference demonstrate RNTP's superiority over existing data transport schemes. For example, in a 64-node topology with 15 nodes at 30dB mean noise, RNTP achieves an EEFR of 0.02%, EEDT of 5.54s, and energy consumption of 0.19mWh per payload packet, compared to at least 22.58%, 13.91s, and 0.23mWh in other schemes. Experiments across WSNs with 36 to 144 nodes confirm RNTP’s performance in scalability, maintaining subpath limits per hop regardless of network size. These statistics underscore RNTP's efficiency for WSNs.

## Techical Report of RNTP
https://github.com/zhouby-zjl/rntp/blob/main/rntp-tech-report.pdf

## How do I run the source code?
1. You need to download both the RNTP from github and the recent ndnSIM from https://ndnsim.net/current/. The version ndnSIM-ns-3.30.1 has been tested and is compliant with the RNTP code.
2. Simply copy all files of the RNTP to the ndnSIM folder in an override manner. 
3. You need to edit the rntp-config.ini file under the ndnSIM/ns-3 folder with the correct output log path and some simulation parameters. 
4. Run RNTP testers. 
cd ns-3
./waf --run scratch/rntp-sim --command-template="%s rntp-config.ini"
5. Afterwards, you can find the simulation results under the LOG_DIR directory defined in the above ini file.
 
We are looking forward to new project opportunity in making the RNTP growing up. 

 *********************************************************************************
This work is licensed under CC BY-NC-SA 4.0
(https://creativecommons.org/licenses/by-nc-sa/4.0/).

Copyright (c) 2021-2025 Boyang Zhou @ Zhejiang Lab

This file is a part of "Resilient Subpath-Based NDN Transport Protocol (RNTP) for Ad-Hoc Stationary Wireless Sensor Networks"
(https://github.com/zhouby-zjl/rntp/).

 **********************************************************************************
