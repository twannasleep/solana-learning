# Solana Transaction Processing

Here’s a step-by-step diagram of how transactions are processed in Solana:

```mermaid

sequenceDiagram

participant User

participant RPCNode

participant LeaderNode

participant Validators

participant Blockchain

User->>RPCNode: 1. Create & Sign Transaction

RPCNode->>LeaderNode: 2. Forward Transaction

LeaderNode->>LeaderNode: 3. Assign PoH Timestamp

LeaderNode->>LeaderNode: 4. Process Transaction (Sealevel)

LeaderNode->>Blockchain: 5. Add Transaction to Block

LeaderNode->>Validators: 6. Broadcast Block for Validation

Validators->>Validators: 7. Verify Block & Transactions

Validators->>Blockchain: 8. Vote to Finalize Block

Blockchain-->>User: 9. Transaction Confirmed

```

## Steps Explained

1. **User**: Creates and signs a transaction (e.g., sending SOL).
2. **RPC Node**: Receives the transaction and forwards it to the leader node.
3. **Leader Node**: Uses **Proof of History (PoH)** to timestamp the transaction.
4. **Leader Node**: Processes the transaction in parallel using **Sealevel**.
5. **Leader Node**: Adds the transaction to a new block.
6. **Leader Node**: Broadcasts the block to other validators for verification.
7. **Validators**: Check the block and transactions for validity.
8. **Validators**: Vote to finalize the block and add it to the blockchain.
9. **Blockchain**: Confirms the transaction to the user
