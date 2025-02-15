# Solana Program Structure

Solana programs (smart contracts) are the backbone of the blockchain, enabling developers to build decentralized applications (dApps). Here’s an overview of the structure of a Solana program.

---

## **Key Components**

### 1. **Entry Point**

- The main function that Solana calls when a program is invoked.
- Example:

  ```rust
  entrypoint!(process_instruction);
  ```

### 2. **Instruction Handler**

- Processes the specific logic for each instruction.
- Example:

  ```rust
  fn process_instruction(
      program_id: &Pubkey,
      accounts: &[AccountInfo],
      instruction_data: &[u8],
  ) -> ProgramResult {
      // Logic for handling the instruction
  }
  ```

### 3. **Accounts**

- Used to store data and interact with the program.
- Each account has:
  - **Owner**: The program that controls the account.
  - **Data**: The information stored in the account.
  - **Lamports**: The amount of SOL held in the account.

### 4. **State Management**

- Programs use **data accounts** to store state (e.g., user balances, program settings).

### 5. **Error Handling**

- Programs must handle errors gracefully and return a `ProgramResult`.
- Example:

  ```rust
  if !is_valid_account(&account) {
      return Err(ProgramError::InvalidAccountData);
  }
  ```

### 6. **Cross-Program Invocation (CPI)**

- Programs can call other programs using **Cross-Program Invocation (CPI)**.
- Example:

  ```rust
  invoke(
      &system_instruction::transfer(&from_pubkey, &to_pubkey, amount),
      &[from_account.clone(), to_account.clone()],
  )?;
  ```

### 7. **Program Derived Addresses (PDAs)**

- **PDAs** are special accounts controlled by a program.
- Example:

  ```rust
  let (pda, bump_seed) = Pubkey::find_program_address(&[b"seed"], program_id);
  ```

### 8. **Testing and Debugging**

- Use the **Solana Program Test** framework for testing.
- Debug using logs or the `solana-test-validator` for local testing.

---

## **Example Program**

```rust
use solana_program::{
account_info::{next_account_info, AccountInfo},
entrypoint,
entrypoint::ProgramResult,
pubkey::Pubkey,
msg,
};
// Entry point
entrypoint!(process_instruction);
// Instruction handler
fn process_instruction(
program_id: &Pubkey,
accounts: &[AccountInfo],
instruction_data: &[u8],
) -> ProgramResult {
// Log the program ID
msg!("Program ID: {}", program_id);
// Iterate over accounts
let accounts_iter = &mut accounts.iter();
let account = next_account_info(accounts_iter)?;
// Example logic: Check if the account is valid
if !account.is_signer {
return Err(ProgramError::InvalidAccountData);
}
Ok(())
}
```

---

## **Why Program Structure Matters**

- **Modularity**: Clear separation of concerns makes programs easier to maintain and extend.
- **Security**: Proper error handling and account validation prevent vulnerabilities.
- **Interoperability**: Cross-Program Invocation enables programs to work together seamlessly.

---

This file provides a quick reference for understanding the structure of Solana programs. Save it for future use!
