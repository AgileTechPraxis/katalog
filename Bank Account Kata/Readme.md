# Bank Account Kata

## Requirements

Implement using Test-Driven Development a bank account class that supports the following features:

1. **Deposit**: Add funds to the account.
2. **Withdraw**: Remove funds from the account.
3. **Display Statement**: Display a statement that includes the current balance and a list of all transactions in chronological order.

### Rules

- The account balance cannot go below zero (no overdrafts allowed).
- The system must allow retrieving the transaction history in chronological order.
- The statement must display the balance at the top, followed by the list of transactions and their timestamp.

---

### Example Scenarios

#### 1 Deposit

- Initial balance: $0
- Deposit $100 on 2023-10-01
- New balance: $100
- Statement:

```text
Balance: $100
2023-10-01: Deposit $100
```

#### 2 Deposits

- Initial balance: $0
- Deposit $100 on 2023-10-01
- Deposit $50 on 2023-12-25
- New balance: $150
- Statement:

```text
Balance: $150
2023-10-01: Deposit $100
2023-12-25: Deposit $50
```

#### 3 Overdraft Prevention

- Initial balance: $50
- Attempt to withdraw $100
- Result: Error.
    Transaction rejected: balance too low.
- Balance stays the same.

### 1 deposit and 1 withdraw

- Deposit $200 on 2023-10-01
- Withdraw $50 on 2023-10-02
- Statement:

```text
Balance: $150
2023-10-01: Deposit $200
2023-10-02: Withdraw $50
```
