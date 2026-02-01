# CoffeeShop Manager ☁️
A serverless coffee shop inventory management system built on AWS using API Gateway, Lambda, DynamoDB, IAM, CloudWatch, and Amplify.

This project demonstrates how a Solutions Architect designs for scalability, security, performance efficiency, and cost optimization using an event-driven, pay-per-use architecture.

---

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
![Architecture Diagram](docs/architecture.png)

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
