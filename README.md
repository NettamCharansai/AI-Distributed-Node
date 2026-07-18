# AI-Distributed-Node
A decentralized peer-to-peer (P2P) network node implementation utilizing the Chord protocol. 

## 📖 Overview
This project demonstrates core concepts in distributed systems, including scalable data routing, concurrent node management, and decentralized hash tables (DHT). It serves as a foundational architecture for building robust backend services and cloud infrastructure.

## 🚀 Project Outcomes & Engineering Impact
* **High Scalability:** Proves the ability to build systems where adding more servers (nodes) increases capacity without degrading performance.
* **Fault Tolerance & Resilience:** Demonstrates an understanding of highly available systems. If a peer goes down, the network automatically heals and reroutes data.
* **Efficient Data Routing:** Showcases a grasp of advanced algorithms ($O(\log N)$ search complexity) and consistent hashing, which is the exact technology used behind load balancers and databases at enterprise companies.
* **Concurrency Management:** Highlights Java skills in handling multiple active network socket connections and background threads simultaneously.

## 🛠️ Tech Stack
* **Language:** Java
* **Architecture:** Decentralized P2P / Chord Protocol
* **Focus:** Backend Development & Distributed Systems


## 🌐 Chord Ring Topology
```mermaid
graph TD
    subgraph Decentralized Hash Table Ring
        direction TB
        P1((Peer 1<br/>Owner)) -->|Successor| P2((Peer 2))
        P2 -->|Successor| P3((Peer 3))
        P3 -->|Successor| P4((Peer 4))
        P4 -->|Successor| P5((Peer 5))
        P5 -->|Successor| P6((Peer 6))
        P6 -->|Successor| P1
        
        %% Finger Table Routing Example
        P1 -.->|Finger Table Jump O log N| P4
        P2 -.->|Finger Table Jump| P5
    end
    
    style P1 fill:#0e75b6,stroke:#fff,stroke-width:2px,color:#fff
    style P4 fill:#28a745,stroke:#fff,stroke-width:2px,color:#fff

