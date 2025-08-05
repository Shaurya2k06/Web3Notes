## Atomic Swaps

Atomic swaps consist of a technique that allows the quick exchange of two different cryptocurrencies, running on distinct blockchain newtworks. Such a proccess is based on smart contracts, and allows users to directly trade crypto from their personal wallets

### Base Idea: 
Peer to Peer trades across different blockchains. 

### Mechanism:
In a nutshell, lets say one user wants to trade Bitcoin for Ethereum. The process would look like this:
1. **Hash Time-Locked Contracts (HTLC)**  
   - User A creates a hash of a secret and locks their Bitcoin in a contract.
   - User B does the same with Ethereum, locking it in a separate contract.
2. **Secret Sharing**  
   - User A shares the secret with User B, allowing them to unlock the Bitcoin.
   - User B uses the secret to unlock the Ethereum.
3. **Completion**  
   - Both users complete the transaction, ensuring that either both trades happen or none do, preventing loss of funds.

### Hash Time-Locked Contracts (HTLC)
Even though Hash Time-Locked contracts are part of the Bitcoin Lightning Network, they are also used in atomic swaps. They consist of two main components: The Hash and the Time Lock. Timelock is a function that ensures that contracts can only be executed within a predefined timeframe. The Hash function is used to create a unique identifier for the contract, which is based on a secret known only to the parties involved in the swap.

