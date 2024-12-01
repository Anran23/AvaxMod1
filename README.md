# Error Handling Smart Contract

This repository contains a Solidity smart contract, `errorHandling`, that demonstrates error handling techniques in Ethereum blockchain development. The contract includes functionality for deposits, transfers, withdrawals, and a deliberate use of the `revert` statement to demonstrate transaction rollback.

---

## Features

- **Deposit Funds**: Users can deposit funds into their account.
- **Transfer Funds**: Users can transfer funds to other accounts.
- **Withdraw Funds**: Users can withdraw their funds.
- **Demonstration of `revert`**: Includes a function that intentionally reverts a transaction to showcase error handling.

---

## Smart Contract Overview

### **State Variables**
- `balances`: A mapping to store user balances, keyed by address.

### **Events**
- `Deposit`: Emitted when a user deposits funds.
- `Transfer`: Emitted when a user transfers funds to another address.
- `Withdraw`: Emitted when a user withdraws funds.
- `SentEther`: Emitted when Ether is sent between accounts.

### **Functions**
1. **`deposit(uint amount)`**
   - Deposits a specified amount into the caller's account.
   - Validates the amount is non-zero.

2. **`transfer(address to, uint value)`**
   - Transfers a specified amount to another account.
   - Checks that the sender has sufficient balance and the recipient's address is valid.

3. **`withdraw(uint value)`**
   - Withdraws a specified amount from the caller's account.
   - Ensures the caller has sufficient balance.

4. **`sendEtherWithRevert(address to, uint value)`**
   - Transfers funds but intentionally reverts the transaction for demonstration purposes.
   - Ensures balance validity before attempting the transfer.

---

## Error Handling Techniques

1. **`require`**: Validates inputs and conditions. Reverts the transaction if conditions are not met.
2. **`assert`**: Used for checking internal invariants. Consumes all gas if it fails.
3. **`revert`**: Explicitly rolls back the transaction with a custom error message.

---

## Deployment

1. Install dependencies:
   ```bash
   npm install
