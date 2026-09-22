ATM Application

A console-based ATM (Automated Teller Machine) simulator written in Java. It models a simple banking system where users can create an account, log in with a customer number and PIN, and manage a checking and a savings account — all through a text-based menu.

Features
Account creation – Register a new customer with a unique customer number and PIN.
Login – Authenticate with a customer number and PIN before accessing any account.
Dual accounts – Every customer has both a Checkings and a Savings account.
View balance – Check the current balance of either account.
Deposit funds – Add money to either account.
Withdraw funds – Take money out of either account (blocked if it would go negative).
Transfer funds – Move money between your own Checkings and Savings accounts.
Input validation – Handles invalid/non-numeric input and prevents balances from going negative.
Project Structure
ATMApplication/
├── ATM/
│   ├── ATM.java          # Entry point — starts the application
│   ├── Account.java      # Account model: balances, deposits, withdrawals, transfers
│   └── OptionMenu.java   # Menu navigation, login, account creation, and account access
├── Jenkinsfile           # CI pipeline (runs a Semgrep security scan)
├── LICENSE                # MIT License
└── README.md
Prerequisites
Java Development Kit (JDK) 8 or later
A terminal / command prompt, or a Java IDE (Eclipse, IntelliJ IDEA, NetBeans, VS Code, etc.)
Getting Started
Clone the repository
bash
   git clone https://github.com/sarikondaKarthik/ATMApplication.git
   cd ATMApplication/ATM
Compile the source files
bash
   javac ATM.java
Run the application
bash
   java ATM

You should see:

Welcome to the ATM Project!

 Type 1 - Login
 Type 2 - Create Account

Choice:
Usage
Demo accounts

Two demo accounts are pre-loaded when the application starts, so you can log in immediately without creating a new account:

Customer Number	PIN	Checkings Balance	Savings Balance
952141	191904	$1,000.00	$5,000.00
123	123	$20,000.00	$50,000.00
Typical flow
From the main menu, choose 1 - Login and enter a customer number and PIN (or 2 - Create Account to register a new one).
Select which account to access: Checkings or Savings.
From there, choose to:
View Balance
Withdraw Funds
Deposit Funds
Transfer Funds (to your other account)
Exit
Follow the on-screen prompts to enter amounts. The application re-prompts on invalid input and prevents any balance from going negative.
Continuous Integration

This repository includes a Jenkinsfile that runs a Semgrep static analysis scan (p/ci ruleset) on every pipeline run to catch common security issues early.

Contributing

Contributions are welcome!

Fork the repository.
Create a feature branch (git checkout -b feature/my-feature).
Commit your changes with clear messages.
Push to your branch and open a pull request, describing the change and referencing any related issue.

Please open an issue first to discuss significant changes before submitting a pull request.
