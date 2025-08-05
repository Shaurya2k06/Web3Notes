# InterPlanetary File System (IPFS) 

## Introduction

The **InterPlanetary File System (IPFS)** is a **distributed, peer-to-peer protocol** for storing and sharing hypermedia in a content-addressable way. Developed by **Protocol Labs**, IPFS is designed to make the web faster, more secure, and more open by replacing location-based resource retrieval (HTTP) with a **content-based addressing model**.

IPFS enables the creation of **decentralized, resilient storage networks**, where content is uniquely identified by a cryptographic hash (CID) and can be retrieved from any participating node that hosts it.

---

## Core Principles

### 📌 Content Addressing

Instead of locating files by their address (e.g., `https://domain.com/file.txt`), IPFS identifies content via a **Content Identifier (CID)** — a cryptographic hash of the file's content. This ensures:

- **Integrity**: Any modification to the file alters its hash.
- **Immutability**: Files are tamper-proof once added.
- **Deduplication**: Identical content is stored only once.

### 🕸️ Peer-to-Peer Architecture

IPFS operates as a **distributed network of nodes** (peers), each capable of storing and sharing data. Files can be retrieved from **any node that hosts a copy**, removing dependency on a central server.

### 🧬 Merkle DAG

IPFS uses a **Merkle Directed Acyclic Graph (DAG)** as its data structure:

- Files are split into blocks, each hashed and linked.
- Each block forms a node in the DAG.
- Enables deduplication, versioning, and data verification.

---

## Key Components

| Component        | Description |
|------------------|-------------|
| **CID**          | A unique content identifier (SHA-256 multihash). |
| **Blocks**       | Small chunks of data stored and addressed by their hash. |
| **DAG-PB / DAG-CBOR** | Data encoding formats for DAG nodes. |
| **libp2p**       | Modular network stack for peer discovery, pubsub, NAT traversal, etc. |
| **Bitswap**      | IPFS’s data exchange protocol (like BitTorrent but generalized). |
| **IPLD**         | InterPlanetary Linked Data – a data model for linking across protocols. |
| **DHT**          | A distributed hash table used to locate peers and data. |

---

## Operational Flow

1. **Initialization**  
   A node is initialized via `ipfs init`, generating a peer ID and local datastore.

2. **Adding Files**  
   - Files are chunked, hashed, and stored as DAG nodes.
   - The root node receives a CID that represents the entire file/directory tree.

3. **Publishing & Pinning**  
   - Files can be pinned to prevent garbage collection.
   - Content can be made accessible via public gateways or IPNS (mutable naming).

4. **Retrieval**  
   - Users retrieve files via CID.
   - IPFS queries the DHT to locate peers storing the desired content.
   - Bitswap fetches the content in parallel from multiple peers.

---

## Use Cases

- **Decentralized Web Hosting**  
  Host static websites with no central origin (e.g., `Fleek`, `dweb.link`).

- **NFT Metadata & Asset Storage**  
  Ensure persistence and integrity of token-bound data on networks like Ethereum.

- **Scientific Data & Research**  
  Enable transparent and tamper-proof data sharing (e.g., MIT Open Access).

- **Decentralized Applications (dApps)**  
  Store frontend assets, user-generated content, or app state.

- **Archival & Backup**  
  Leverage content immutability for verifiable backups and archiving.

---

## IPFS vs HTTP - Technical Comparison

| Feature               | IPFS                                   | HTTP                                   |
|-----------------------|----------------------------------------|----------------------------------------|
| Addressing            | Content-based (CID)                    | Location-based (URL/domain)            |
| Centralization        | Decentralized (peer-to-peer)           | Centralized (client-server)            |
| Data Integrity        | Verified via hash                      | No built-in verification               |
| Offline Capability    | Yes (if content cached locally)        | No                                     |
| Performance           | Parallel retrieval from multiple peers | Single-origin latency bottleneck       |
| Fault Tolerance       | High (multiple nodes)                  | Low (single point of failure)          |

---

## Integration with Filecoin

While IPFS provides **decentralized file sharing**, it does not guarantee **permanent storage**. For long-term persistence with incentives, IPFS integrates with **Filecoin**, a blockchain-based decentralized storage network that allows users to:

- Make **storage deals** with miners.
- Cryptographically prove data is stored using **Proof of Replication** and **Proof of Spacetime**.
- Retrieve content via IPFS-compatible retrieval tools.

---

## Developer Tooling

- **IPFS CLI**  
  Command-line interface for managing nodes:  
  ```bash
  ipfs init  
  ipfs daemon  
  ipfs add <file>  
  ipfs cat <CID>  
