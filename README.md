# project3

# Chord Protocol Implementation

### Project Overview
This project implements the Chord Protocol in a Peer-to-Peer (P2P) network using Pony and the Actor Model. The project simulates a scalable lookup service with multiple nodes, each capable of issuing requests to locate keys within the network. The Chord Protocol ensures efficient routing and lookup, utilizing a circular ID space and finger tables to minimize the number of hops.

### Team Members
- ⁠*Yaswanth Attaluri* 
      UFID : 1013 6560
- *Shruthi Yaramada*
      UFID : 2649 7222

### Usage
To execute the program, use the following command:
⁠ bash
project3 <numNodes> <numRequests>
 ⁠
- ⁠*numNodes*: Total number of nodes in the P2P network.
- ⁠*numRequests*: Number of requests each node will issue.

### Project Details
#### Features Implemented
1.⁠ ⁠*Node Initialization and Joining*:
   - Each node initializes itself and establishes connections within the network.
   - Nodes set up their finger tables and establish successor/predecessor relationships.
   
2.⁠ ⁠*Lookup and Routing*:
   - Nodes perform lookup requests to locate keys. If a node does not contain the key, it forwards the lookup request to the next closest node based on its finger table.
   - The average number of hops taken to resolve each request is tracked and displayed at the end of execution.

3.⁠ ⁠*Timers for Stabilization*:
   - Nodes periodically stabilize and update their finger tables to maintain efficient routing as nodes join or leave.
   
4.⁠ ⁠*Data Storage and Retrieval*:
   - Each node has a key-value store, allowing it to store and retrieve data associated with unique keys.
   
5.⁠ ⁠*Performance Metrics*:
   - At the end of execution, the average number of hops per request and the total hops across all requests are printed.

### Execution Example
```bash
./PROJECT3 <numNodes> <numRequests>
```

### Largest Network Managed
1. Successfully tested with a network of 10,000 peers and 100 requests per node.
2. System maintained stable routing performance:
      - Average Hop Count remained within expected limits for a Distributed Hash Table (DHT).
Beyond this scale:
   - Noticeable delays were observed.
   - Occasional resource limitations arose due to increased message-handling and finger table maintenance overhead.
