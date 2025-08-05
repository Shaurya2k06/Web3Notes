# Ethereum Virtual Machine (EVM)

The Ethereum Virtual Machine is a decentralized virtual environment that executes code consistently and securely across all nodes in the Ethereum Network.Nodes run the EVM to execute smart contracts, using gas to measure computational effort required for operations.

### Introduction
The analogy of a distributed ledger is a record of activity that must adhere to a set of rules that govern what someone can and cannot do to modify the ledger. While Ethereum has its own native cryptocurrency that follows almost exactly the same inituitive rules as Bitcoin, it also has a more complex set of rules that allow for the creation of smart contracts. These smart contracts are executed by the EVM, which is a Turing-complete virtual machine that can run any code written in a compatible programming language.

### Execution 
The EVM executes as a stack machine with a depth of 1024 items. Each item is a 256 bit word, which was chosen for the ease of use with the Keccak-256 hashing algorithm used in Ethereum. The EVM operates on a state machine model, where each transaction modifies the state of the blockchain.

### Key Features
- **Turing Completeness**: The EVM can execute any computable function, allowing
for complex smart contracts and decentralized applications (dApps).
- **Gas Mechanism**: Every operation in the EVM requires gas, which is a unit of computational work. This prevents spam and ensures that resources are used efficiently.
- **Deterministic Execution**: The EVM ensures that the same input will always produce the same output across all nodes, maintaining consensus in the network.
- **Isolation**: Smart contracts run in a sandboxed environment, preventing them from directly accessing the underlying system or other contracts, enhancing security.

