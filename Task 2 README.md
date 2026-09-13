TASK 2
# Banking Ledger Engine

## Overview

The Banking Ledger Engine is a Python-based banking application designed to demonstrate object-oriented programming, transaction processing, custom exception handling, and data persistence.

The system supports different types of bank accounts and provides operations such as deposits, withdrawals, balance management, transfers, and interest calculation.

The project focuses on applying software engineering concepts to a simple real-world financial system.

## Features

* Supports general bank accounts.
* Supports savings accounts.
* Supports current accounts.
* Deposit functionality.
* Withdrawal functionality.
* Account-to-account money transfer.
* Savings interest calculation.
* Current-account overdraft support.
* Custom exception handling.
* JSON-based data persistence.
* Object-oriented design.
* Automated testing using `pytest`.

## Technologies Used

* Python
* Object-Oriented Programming
* JSON
* `pytest`
* Python Standard Library

## Object-Oriented Concepts

The project demonstrates several important OOP concepts:

### Encapsulation

Account information such as account number, holder name, and balance is managed internally through class attributes and properties.

### Inheritance

`SavingsAccount` and `CurrentAccount` inherit common functionality from the `Account` base class.

### Polymorphism

Different account classes implement their own `account_type()` and withdrawal behavior.

### Abstraction

Common banking operations are defined at the account level while specialized behavior is implemented by individual account types.

## Banking Operations

The system supports:

```text
Deposit
Withdraw
Transfer
Balance Checking
Interest Calculation
Account Management
Data Persistence
```

## Custom Exceptions

The project includes custom exceptions for invalid transactions.

Examples include:

```text
InsufficientFundsError
InvalidAmountError
```

These exceptions help the application handle invalid operations without terminating unexpectedly.

## Data Persistence

Bank account information can be saved to:

```text
bank_accounts.json
```

The JSON file contains account information such as:

* Account number
* Account holder
* Account type
* Balance

## Running the Project

Run the Python application or execute the corresponding notebook cells.

Example:

```python
account.deposit(2000)
account.withdraw(500)
```

Money can also be transferred between accounts:

```python
ledger.transfer("S001", "C001", 2000)
```

## Testing

The project includes automated tests using `pytest`.

Run the tests with:

```bash
pytest project2_banking/test_banking.py -v
```

The tests cover important operations including:

* Deposits
* Withdrawals
* Transfers
* Insufficient balance handling
* Invalid deposit handling

## Example

```text
============================================================
BANKING LEDGER
============================================================

S001 | Aishwarya | Savings Account | Balance: ₹8500.00
C001 | Rahul | Current Account | Balance: ₹7000.00
```

## Project Objectives

* Understand object-oriented programming in Python.
* Implement inheritance and polymorphism.
* Build a simple transaction-processing system.
* Implement custom exception handling.
* Store application data using JSON.
* Develop automated tests.
* Apply software engineering practices to a real-world problem.

## Applications

The project provides a simplified model of a banking ledger and can serve as a foundation for learning how transaction-based financial applications are designed.

## Author

M. Ayshwarya
