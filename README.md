# ATM Application

A console-based ATM (Automated Teller Machine) simulator written in Java. It models a simple banking system where users can create an account, log in with a customer number and PIN, and manage checking and savings accounts through a text-based menu.

## Features

- **Account creation** - Register a new customer with a unique customer number and PIN.
- **Login** - Authenticate with a customer number and PIN before accessing an account.
- **Dual accounts** - Every customer has both a **Checkings** and a **Savings** account.
- **View balance** - Check the current balance of either account.
- **Deposit funds** - Add money to either account.
- **Withdraw funds** - Take money out of either account without allowing a negative balance.
- **Transfer funds** - Move money between your own Checkings and Savings accounts.
- **Input validation** - Handles invalid input and rejects transactions that would create a negative balance.

## Project Structure

```text
ATMApplication/
├── ATM/
│   ├── ATM.java          # Entry point - starts the application
│   ├── Account.java      # Account model and transaction operations
│   └── OptionMenu.java   # Menu navigation, login, and account creation
├── Jenkinsfile           # CI pipeline for Semgrep security scanning
├── LICENSE               # MIT License
└── README.md
```

## Prerequisites

- [Java Development Kit (JDK) 8](https://www.oracle.com/java/technologies/downloads/) or later
- A terminal, command prompt, or Java IDE such as Eclipse, IntelliJ IDEA, NetBeans, or VS Code

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/sarikondaKarthik/ATMApplication.git
cd ATMApplication/ATM
```

### 2. Compile the source files

```bash
javac ATM.java
```

### 3. Run the application

```bash
java ATM
```

You should see:

```text
Welcome to the ATM Project!

 Type 1 - Login
 Type 2 - Create Account

Choice:
```

## Usage

### Demo accounts

Two demo accounts are loaded when the application starts, so you can log in immediately without creating a new account:

| Customer Number | PIN    | Checkings Balance | Savings Balance |
|-----------------|--------|-------------------|-----------------|
| `952141`        | `191904` | $1,000.00       | $5,000.00       |
| `123`           | `123`    | $20,000.00      | $50,000.00      |

### Typical flow

1. From the main menu, choose **1 - Login** and enter a customer number and PIN, or choose **2 - Create Account** to register a new customer.
2. Select **Checkings** or **Savings**.
3. Choose one of the available actions:
	- View Balance
	- Withdraw Funds
	- Deposit Funds
	- Transfer Funds to your other account
	- Exit
4. Follow the prompts to enter transaction amounts. Invalid input is rejected, and withdrawals or transfers cannot make an account balance negative.

## Continuous Integration

This repository includes a `Jenkinsfile` that runs a [Semgrep](https://semgrep.dev/) static analysis scan using the `p/ci` ruleset on every pipeline run. The scan helps identify common security issues early.

## Contributing

Contributions are welcome:

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature/my-feature`
3. Commit your changes with a clear message.
4. Push your branch and open a pull request describing the change.

Please open an issue first to discuss significant changes before submitting a pull request.