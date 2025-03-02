
# zk-SNARKs and zk-STARKs

zk-SNARK stands for zero-knowledge succinct non-interactive argument of knowledge, and zk-STARK represents zero-knowledge succinct transparent argument of knowledge. zk-SNARK proofs are used by cryptocurrency projects (such as Zcash), on blockchain-based payment systems, and as a way to securely authenticate clients to servers. But while zk-SNARKs have made significant headway to being well-established and adopted, zk-STARK proofs are now being touted as the new and improved version of the protocol, addressing many of the previous drawbacks of zk-SNARKs.

[Read more about zk-SNARKs and zk-STARKs](https://pages.cs.wisc.edu/~mkowalcz/628.pdf)

Zero-knowledge proofs allow one individual to prove to another that a statement is true without disclosing any information beyond the validity of the statement. The parties involved are commonly referred to as a prover and a verifier, and the statement they hold in secret is called a witness. The main objective of these proofs is to reveal as little data as possible between the two parties. In other terms, one can use zero-knowledge proofs to prove that they have certain knowledge without revealing any information about the knowledge itself.

Within the SNARK acronym, “succinct” means that these proofs are smaller in size and can be quickly verified. “Non-interactive” means that there is little to no interaction between the prover and the verifier. Older versions of zero-knowledge protocols usually require the prover and verifier to communicate back and forth and, therefore, are considered “Interactive” ZK proofs. But in “non-interactive” constructions, provers and verifiers only have to exchange one proof.

Moving onto the “Arguments of Knowledge” piece of the acronym. zk-SNARKs are considered computationally sound, meaning that a dishonest prover has a very low chance of successfully cheating the system without actually having the knowledge (or witness) to support their statement. This property is known as soundness and assumes that the prover has limited computing power.

Theoretically, a prover with enough computational power could create fake proofs, and this is one of the reasons quantum computers are considered by many to be a threat to zk-SNARKs (and blockchain systems).

Zero-knowledge proofs are quickly verifiable and usually take up much less data than a standard Bitcoin transaction. This opens up a pathway for zk-SNARK technology to be used as both a privacy and a scalability solution.

## Advantages of zk-SNARKs
1. **Privacy**: zk-SNARKs allow for transactions to be verified without revealing the transaction details, ensuring user privacy.
2. **Scalability**: Due to their succinct nature, zk-SNARKs can help in reducing the amount of data that needs to be processed and stored, thus improving the scalability of blockchain systems.
3. **Security**: zk-SNARKs provide a high level of security by ensuring that only valid transactions are processed without revealing sensitive information.

## Limitations of zk-SNARKs
1. **Trusted Setup**: zk-SNARKs require a trusted setup phase, which if compromised, can undermine the security of the entire system.
2. **Quantum Vulnerability**: As mentioned earlier, zk-SNARKs are potentially vulnerable to attacks from quantum computers.
3. **Complexity**: Implementing zk-SNARKs can be complex and computationally intensive, which may limit their adoption.

## zk-STARKs: The Next Generation
zk-STARKs aim to address some of the limitations of zk-SNARKs. They do not require a trusted setup and are believed to be more resistant to quantum attacks. Additionally, zk-STARKs are designed to be more transparent and scalable, making them a promising alternative for future applications.