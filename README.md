# SmartExpenseTracker

A secure serverless expense tracker built using AWS services. The application allows authenticated users to manage and view their financial transactions through a web interface.

## 🚀 Features

- User registration and authentication with Amazon Cognito
- Secure login through Cognito Hosted UI
- Add income and expense transactions
- View transaction history
- Delete transactions
- Calculate balance, income, and expenses
- User-specific transaction storage
- REST API using Amazon API Gateway
- Serverless backend using AWS Lambda
- No traditional server or EC2 instance required

## 🏗️ Architecture

```text
                    User
                     │
                     ▼
              ┌─────────────┐
              │  Frontend   │
              │  HTML/CSS/JS│
              └──────┬──────┘
                     │
                     ▼
              ┌─────────────┐
              │   Cognito   │
              │     Auth    │
              └──────┬──────┘
                     │
                     ▼
              ┌─────────────┐
              │ API Gateway │
              └──────┬──────┘
                     │
                     ▼
              ┌─────────────┐
              │   Lambda    │
              │ SmartExpense│
              │     API     │
              └──────┬──────┘
                     │
                     ▼
              ┌─────────────┐
              │  DynamoDB   │
              │ Transactions│
              └─────────────┘
