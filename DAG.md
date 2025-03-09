# Directed Acyclic Graph (DAG)

A Directed Acyclic Graph (DAG) is a graph that is directed and without cycles connecting the other edges. This means that it is impossible to start at any node and follow a consistently directed sequence of edges that eventually loops back to the starting node.

## Key Characteristics
- **Directed**: Each edge has a direction, going from one vertex to another.
- **Acyclic**: There are no cycles, meaning there is no way to start at one vertex and follow a path that eventually loops back to the starting vertex.

## Applications
- **Data Processing**: DAGs are used in various data processing frameworks like Apache Spark and Apache Flink.
- **Version Control**: Systems like Git use DAGs to manage changes and versions.
- **Task Scheduling**: DAGs are used to represent tasks and their dependencies in scheduling algorithms.

## Comparison to Blockchain

While both DAGs and blockchains are used in distributed ledger technologies, they have some key differences:

- **Structure**: A blockchain is a linear sequence of blocks, each containing a list of transactions. In contrast, a DAG allows for multiple branches and paths, enabling more parallelism.
- **Scalability**: DAGs can handle higher transaction throughput due to their parallel structure, whereas blockchains can become bottlenecked as each block must be processed sequentially.
- **Confirmation Time**: Transactions in a DAG can be confirmed faster as they do not need to wait for the creation of a new block. In a blockchain, transactions are confirmed when they are included in a block, which can take time depending on the block interval.
- **Use Cases**: Blockchains are commonly used in cryptocurrencies like Bitcoin and Ethereum. DAGs are used in projects like IOTA and Hedera Hashgraph, which aim to provide scalable and fast transaction processing.

## Example
Consider a simple DAG with vertices A, B, and C, and directed edges A -> B and B -> C. There is no way to return to A once you leave it, ensuring there are no cycles.

```plaintext
A -> B -> C
```
