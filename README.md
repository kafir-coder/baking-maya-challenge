# Maya Banking Challenge

## Project Overview

The **Basic Banking API** is a simple API that allows users to perform basic banking operations such as creating accounts, depositing and withdrawing money, checking balances, and transferring funds between accounts. This project is built using Python and the Flask framework, providing a RESTful interface to interact with bank accounts.

## Features

- **Create a new account**: Users can create a new account with an initial deposit.
- **Deposit money**: Users can deposit money into their account.
- **Withdraw money**: Users can withdraw money from their account (subject to balance).
- **Check balance**: Users can check the balance of their account.
- **Transfer money**: Users can transfer funds between two accounts.

## Setup Instructions

### Prerequisites

Make sure you have Python 3.x installed. You will also need `pip` to install dependencies.

1. Install Python (if not already installed):
   - [Python Downloads](https://www.python.org/downloads/)

2. Install dependencies:
   - Flask is required for creating the API.
   - You can install Flask using `pip`:

   ```bash
   pip install flask


Clone the repository
Clone the project repository to your local machine.

bash
Copy code
git clone https://github.com/your-username/banking-api.git
cd banking-api
Run the Application
To start the API, navigate to the project directory and run the Flask application.

# API Endpoints
The following endpoints are available:

1. Create Account (POST /accounts)
Request Body:
```json
{
  "name": "John Doe",
  "initial_deposit": 1000
}
```


Response:
```json
{
  "account_number": "123456789",
  "name": "John Doe",
  "balance": 1000
}
```
2. Deposit Money (POST /accounts/{account_number}/deposit)
Request Body:
```json
{
  "amount": 500
}
```
Response:
```json
{
  "message": "Deposit successful.",
  "new_balance": 1500
}
```
3. Withdraw Money (POST /accounts/{account_number}/withdraw)
Request Body:
```json
{
  "amount": 200
}
```
Response:
```json
{
  "message": "Withdrawal successful.",
  "new_balance": 1300
}
```
4. Check Balance (GET /accounts/{account_number}/balance)
Response:
```json
{
  "balance": 1300
}
```
5. Transfer Money (POST /accounts/{sender_account_number}/transfer)
Request Body:
```json
{
  "receiver_account_number": "987654321",
  "amount": 300
}
```
Response:
```json
{
  "message": "Transfer successful.",
  "sender_balance": 1000,
  "receiver_balance": 1200
}
```
