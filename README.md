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
•⁠  ⁠*numNodes*: Total number of nodes in the P2P network.
•⁠  ⁠*numRequests*: Number of requests each node will issue.

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
⁠ bash
project3 10 100
 ⁠
This command initializes a Chord network with 10 nodes, with each node making 100 requests. The program will output the initialization progress, request completion progress, and the final average hops taken per request.

### Output
The output includes:
•⁠  ⁠Initialization status of each node.
•⁠  ⁠Real-time tracking of requests completed.
•⁠  ⁠Final statistics including the average number of hops and total requests completed.

### Largest Network Managed
This implementation successfully managed networks of up to *[Insert Number]* nodes under testing, with *[Insert Number]* requests per node.

### References
•⁠  ⁠*Chord Paper*: [Chord: A Scalable Peer-to-peer Lookup Service for Internet Applications](https://pdos.csail.mit.edu/papers/ton:chord/paper-ton.pdf)
