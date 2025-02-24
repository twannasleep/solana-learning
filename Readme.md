# Solana Development Guide

## 1. Core Architecture

- [Introduction to Architecture](architecture/README.md)
- [1.1 Proof of History (PoH)](architecture/1.proof_of_history.md)
  - Cryptographic Clock
  - Verifiable Delay Function
  - Performance Benefits
- [1.2 Solana Cluster](architecture/2.solana_cluster.md)
  - Network Components
  - Node Types
  - Consensus Mechanism
- [1.3 Transaction Processing](architecture/3.solana_transaction_processing.md)
  - Transaction Lifecycle
  - Parallel Processing
  - Error Handling
- [1.4 Block Production](architecture/4.solana_block_production.md)
  - Leader Selection
  - Block Creation
  - Validation Process

## 2. Account Model

- [Account System Overview](account-model/README.md)
- [2.1 Account Types](account-model/1.solana_account_types.md)
  - System Accounts
  - Program Accounts
  - Data Accounts
  - Special Purpose Accounts
- [2.2 Account Ownership](account-model/2.solana_account_ownership.md)
  - Ownership Model
  - Permission System
  - Account Control
- [2.3 Rent Economics](account-model/3.solana_rent_economics.md)
  - Rent Mechanism
  - Cost Calculation
  - Rent Exemption
- [2.4 Data Storage](account-model/4.solana_data_storage.md)
  - Storage Models
  - Data Organization
  - Optimization Strategies

## 3. Program Development

- [Program Development Overview](solana-program/README.md)
- [3.1 Program Structure](solana-program/1.solana_program_structure.md)
  - Basic Components
  - Best Practices
  - Design Patterns
- [3.2 Entry Points](solana-program/2.solana_entry_points.md)
  - Program Interface
  - Parameter Handling
  - Execution Flow
- [3.3 Instructions](solana-program/3.solana_instructions.md)
  - Instruction Types
  - Data Serialization
  - Error Handling
- [3.4 State Management](solana-program/4.solana_state_management.md)
  - State Storage
  - Data Updates
  - Concurrency Handling

## 4. Development Tools

- [4.1 Local Development](development/README.md)
  - Development Environment
  - Testing Tools
  - Debugging Techniques
- [4.2 Wallet Integration](wallets/README.md)
  - Wallet Types
  - Integration Methods
  - Security Practices
- [4.3 Transaction Management](transactions/README.md)
  - Transaction Creation
  - Signing Process
  - Confirmation Handling
- [4.4 Account Operations](accounts/README.md)
  - Account Creation
  - Management
  - Best Practices

## 5. Token Standards

- [5.1 Token Operations](tokens/README.md)
  - Token Creation
  - Token Management
  - SPL Standards
  - NFT Development

## 6. Program Examples

- [6.1 Basic Programs](programs/README.md)
  - Hello World
  - Token Program
  - NFT Program
- [6.2 Advanced Programs](programs/advanced/README.md)
  - DeFi Examples
  - Gaming Programs
  - Cross-Program Invocation
