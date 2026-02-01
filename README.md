# CoffeeShop Manager ☁️
A serverless coffee shop inventory management system built on AWS using API Gateway, Lambda, DynamoDB, IAM, CloudWatch, and Amplify.

This project demonstrates how a Solutions Architect designs for scalability, security, performance efficiency, and cost optimization using an event-driven, pay-per-use architecture.

---
<img width="817" height="848" alt="Coffe List" src="https://github.com/user-attachments/assets/e90966e9-8ae7-44f0-87c6-01ec9dae73c4" />

## What I Built
A complete inventory system where a coffee shop owner can:

- View inventory (GET)
- Add new coffee items (POST)
- Update coffee details (PUT)
- Delete sold-out items (DELETE)

**Flow**
Amplify (React frontend) → API Gateway → Lambda → DynamoDB  
CloudWatch provides logs + metrics across the stack.

---

## AWS Services Used
- **Amazon DynamoDB**: Inventory data store (coffeeId, name, price, available)
- **AWS Lambda**: CRUD business logic
- **AWS Lambda Layers**: Shared SDK + utilities
- **Amazon API Gateway (HTTP API)**: REST endpoints + CORS
- **Amazon CloudWatch**: Logs and monitoring
- **AWS IAM**: Least-privilege permissions for Lambda to access DynamoDB
- **AWS Amplify**: React frontend hosting and deployment

---

## Architecture Diagram
> Add your diagram image here once you export it from your notes / draw.io

Example:
<img width="1287" height="623" alt="Coffe Shop Architecture" src="https://github.com/user-attachments/assets/25afeae5-5a3d-45fe-8b0e-3b2f4fc78efc" />

---

## Data Model (DynamoDB)
**Table Name:** `CoffeeShop`  
**Partition Key:** `coffeeId` (String)

Example item:
```json
{
  "coffeeId": "c123",
  "name": "new cold coffee",
  "price": 456,
  "available": true
}
