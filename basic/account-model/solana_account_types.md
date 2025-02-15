# Solana Account Types

Solana uses various account types to manage different aspects of the blockchain. Below is a summary of the main account types and their purposes.

---

## 1. **System Accounts**

- **Purpose**: Hold SOL (native cryptocurrency).
- **Owner**: System Program.
- **Key Features**:
  - Used for basic SOL transfers.
  - Cannot store arbitrary data.

---

## 2. **Program Accounts**

- **Purpose**: Store executable programs (smart contracts).
- **Owner**: BPF Loader.
- **Key Features**:
  - Contains compiled bytecode.
  - Cannot hold SOL directly.

---

## 3. **Data Accounts**

- **Purpose**: Store data associated with a program or user.
- **Owner**: Program-specific.
- **Key Features**:
  - Can store arbitrary data.
  - May hold SOL if the program allows it.

---

## 4. **Token Accounts**

- **Purpose**: Hold SPL tokens and manage token balances.
- **Owner**: SPL Token Program.
- **Key Features**:
  - Stores token balance, mint address, and owner address.
  - Each account is associated with a specific token mint.

---

## 5. **Mint Accounts**

- **Purpose**: Define token properties (e.g., supply, decimals).
- **Owner**: SPL Token Program.
- **Key Features**:
  - Stores metadata about a token.
  - Used in conjunction with Token Accounts.

---

## 6. **Stake Accounts**

- **Purpose**: Stake SOL for network validation.
- **Owner**: Stake Program.
- **Key Features**:
  - Stores staked SOL and validator delegation.
  - Used to earn staking rewards.

---

## 7. **Vote Accounts**

- **Purpose**: Used by validators to vote on blocks.
- **Owner**: Vote Program.
- **Key Features**:
  - Tracks validator voting activity.
  - Used for consensus and reward distribution.

---

## 8. **Nonce Accounts**

- **Purpose**: Manage durable transaction nonces.
- **Owner**: Nonce Program.
- **Key Features**:
  - Enables advanced transaction handling.
  - Used for specific sequencing requirements.

---

## Summary Table

| Account Type      | Purpose                          | Owner Program          |
|-------------------|----------------------------------|------------------------|
| System Account    | Hold SOL                        | System Program         |
| Program Account   | Store executable code           | BPF Loader             |
| Data Account      | Store program-specific data     | Program-specific       |
| Token Account     | Hold SPL tokens                 | SPL Token Program      |
| Mint Account      | Define token properties         | SPL Token Program      |
| Stake Account     | Stake SOL                       | Stake Program          |
| Vote Account      | Validator voting                | Vote Program           |
| Nonce Account     | Manage transaction nonces       | Nonce Program          |

---

This file provides a quick reference for understanding the different account types in Solana. Save it for future use!
