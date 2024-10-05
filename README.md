# Introduction
High-Level Overview

DomiPago is a cutting-edge remittance platform that streamlines money transfers between the USA and the Dominican Republic, offering a seamless experience via WhatsApp, mobile app and website. With transactions completed in under 60 seconds, DomiPago removes the need for recipients to visit physical remittance locations, making the process faster, safer, and more convenient by enabling transfers from and to debit cards.

As a proven solution for fiat transfers, DomiPago is now expanding its capabilities by integrating Stellar’s blockchain. This powerful integration allows users to request and receive stablecoins like USDC and Dominican peso tokens directly into a simple WhatsApp-based wallet. By leveraging Stellar’s secure, low-cost, and fast blockchain technology, DomiPago enhances financial inclusion for those who lack access to traditional banking services.

DomiPago’s mission is to bridge the gap between everyday communication tools and cutting-edge financial solutions, improving the social and financial impact of remittances in developing economies by reducing costs and eliminating the hassle of cash dependency. With this Stellar integration, DomiPago is set to transform the remittance landscape and bring digital finance to underserved populations.

## Architecture Overview
### C4 L1 Diagram: High-Level Architecture
This high-level diagram shows the system's broader context, depicting its interactions with external entities such as customers, systems, or external services.

![DomiPago-C4-L2-StellarCamp-v1 drawio](https://github.com/user-attachments/assets/4324bf82-f37e-486f-8b2a-c3a8364cfa1e)



### C4 L2 Diagram: Zoom into the DomiPago System
This diagram illustrates a more technical overview of the DomiPago System.

![DomiPago-C4-L1-StellarCamp-v1 drawio](https://github.com/user-attachments/assets/ff7582bb-30fa-42d8-9ccd-b5da28a4024e)

## Deliverables
### Deliverable 1 (Already done)
#### **User Story 1: Bot Introduction**

As a user, I want to receive an invitation message to start using DomiPago.

##### Acceptance Criteria:
1. **Given** that the user has initiated a WhatsApp conversation. 
2. **When** the bot sends the initial message.
3. **Then** the message should say, "Hey {user name}, Thanks for choosing DomiPago the best way to request and send funds to the Dominican Republic from USA.


#### **User Story 2: Main Menu Options**

As a user, I want to be able to select whether to request or send funds using the bot.

##### Acceptance Criteria:

1. **Given** that the user has received the initial bot message,
2. **When** the bot sends a follow-up message,
3. **Then** the message should say, "What would you like to do?" with options:
"Request funds from Dominican Republic"
"Send funds from USA."


#### **User Story 3: Requesting Funds from the Dominican Republic**

As a user, I want to provide my details to request funds from the Dominican Republic.

##### Acceptance Criteria:

1. **Given** that the user selected "Request funds from Dominican Republic,"
2. **When** the bot prompts for personal details,
3. **Then** the bot should ask for "Your name and last name" and "Your date of birth (dd/mm/yyyy)."
4. **Given** that the user sends the requested information,
5. **When** the user submits the details,
6. **Then** the information should be validated and stored for further processing.


#### **User Story 4: Sending Funds from the USA**

As a user, I want to provide my details to send funds from the USA.

##### Acceptance Criteria:

1. **Given** that the user selected "Send funds from USA,"
2. **When** the bot prompts for personal details,
3. **Then** the bot should ask for necessary information like the recipient's name, amount, and any required verification.
4. **Given** that the user sends the requested information,
5. **When** the user submits the details,
Then the information should be validated and stored for further processing.


#### **User Story 5: Confirming Fund Request Information**

As a user, I want the bot to confirm my provided information for fund requests.

##### Acceptance Criteria:

1. **Given** that the user has provided their name and date of birth,**
2. When** the bot receives the details,
3. **Then** the bot should say, "Great!! Thanks for providing the information."
4. **Given** that the bot confirms the information,
5. **When** the confirmation message is sent,
6. **Then** the bot should ask, "How do you like to receive funds?" with options:
"Account deposit"
"Debit card deposit."


#### **User Story 6: Providing Payment Information for Account Deposit**

As a user, I want to add my bank account details to receive funds.

##### Acceptance Criteria:

1. **Given** that the user selects "Account deposit,"
2. **When** the bot prompts for payment details,
3. **Then** the bot should ask for:
"Account number"
"Bank Name."
4. **Given** that the user provides the requested details,
5. **When** the user sends the account and bank information,
6. **Then** the bot should validate and store the payment information.


#### **User Story 7: Providing Payment Information for Debit Card Deposit**

As a user, I want to add my debit card details to receive funds.

##### Acceptance Criteria:

1. **Given** that the user selects "Debit card deposit,"
2. **When** the bot prompts for card details,
3. **Then** the bot should ask for:
"Card number"
"Expiration date."
4. **Given** that the user provides the requested details,
5. **When** the user sends the card information,
6. **Then** the bot should validate and store the card information.

### Deliverable 2

#### User Story 1: User Authentication via OTP (SMS)
As a user, I want to authenticate my identity via OTP (one-time password) sent to my phone, so that I can securely access my account on WhatsApp.

##### Acceptance Criteria:
1. **Given** I want to send a remittance via WhatsApp,
2. **When** I initiate the process,
3. **Then** I should receive an OTP via SMS to verify my identity before proceeding.
4. **Given** I have received the OTP,
5. **When** I input the correct code in the WhatsApp conversation,
6. **Then** I should be able to proceed with my transaction.

### Deliverable 3

#### User Story 1: Recurrent Payments

As a user, I want to set up recurring payments, so that I can automatically send remittances regularly without manual intervention.
##### Acceptance Criteria:

1. **Given** I am interacting with the AI-bot via WhatsApp,
2. **When** I choose the option to schedule a recurring payment,
3. **Then** I should be able to specify the amount, frequency, and recipient for automatic transfers.
4. **Given** I have set up a recurring payment,
5. **When** the scheduled payment is processed,
6. **Then** I should receive a confirmation message in WhatsApp.

### Deliverable 4

#### User Story 2: Transactional History
As a user, I want to view my transaction history, so that I can keep track of all my past remittances.
#####Acceptance Criteria:

1. **Given** I am chatting with the AI-bot in WhatsApp,
2. **When** I ask for my transaction history,
3. **Then** the AI-bot should display a list of my recent transactions with details like date, amount, and recipient.

### Deliverable 5
User Story 1: Update or Change Form of Payment
As a user,
I want to update or change my form of payment,
So that I can modify my payment preferences for future remittances via WhatsApp.
##### Acceptance Criteria:

1. **Given** I am interacting with the AI-bot in WhatsApp,
2. **When** I ask to update my payment method,
3. **Then** I should be able to add, update, or remove payment options (e.g., bank accounts) through the WhatsApp conversation.
4. **Given** I have changed my payment method,
5. **When** I confirm the update,
6. **Then** the new payment method should be used for all future transactions.

### Deliverable 6.

User Story 1: KYC and Stellar Integration
As a user, I want to complete KYC (Know Your Customer) verification, so that I can use DomiPago services for sending and receiving funds.
#####Acceptance Criteria:

1. **Given** I want to use DomiPago for remittances,
2. **When** I provide my personal details for KYC verification via WhatsApp,
3. **Then** the system should validate my identity and notify me when the process is complete.

### Deliverable 7
User Story 1: Notifications
As a user, I want to receive notifications about my transactions via WhatsApp, So that I can stay informed about the status of my remittances.

##### Acceptance Criteria:
1. **Given** I have completed a remittance,
2. **When** the payment is processed successfully,
3. **Then** I should receive a confirmation message via WhatsApp.
4. **Given** I have set up a recurring payment,
5. **When** a scheduled payment is processed,
6. **Then** I should receive a WhatsApp notification informing me about the transaction.

## Stack
### Backend
Node.js & Typescript 
For building scalable, real-time APIs and services.

### MySQL 
As the primary database for managing transactional data.

### Firebase 
Is used for additional real-time data synchronisation and user authentication.

### Frontend
Flutter
Is employed for building cross-platform mobile app, providing a consistent user experience across devices.

## Infrastructure

### AWS
Is used to host and scale the application’s infrastructure, ensuring reliability and performance.

### Amazon RDS
To manage the MySQL database in a scalable and managed environment, ensuring high availability and automated backups.

### Amazon SNS
To send notifications to users, especially for transaction confirmations or OTPs.

### AWS Secrets Manager
To securely store and manage sensitive information, like API keys for Stellar Blockchain, WhatsApp integrations, and database credentials.

### AWS App Runner
For automatically deploying and scaling the backend Node.js and TypeScript application from a containerized setup or a GitHub repository, simplifying deployment without needing to manage infrastructure directly.
Automated Testing

### Jest & Supertest
Is used to host and scale the application’s infrastructure, ensuring reliability and performance.

### GitHub Actions CI/CD
Ensures a robust and automated process for continuous integration (CI) and continuous delivery (CD). It manages code quality, automated testing, and deployment to production environments efficiently.
Integrations
Stellar Blockchain & Anchors (AlfredPay and/or Cybrid)
The platform integrates with Stellar Blockchain and Anchors to process fast, low-cost remittance transactions. KYC is managed by anchors.

### WhatsApp
Serves as the primary user interaction channel for seamless money transfers.

### Respond.io

Is implemented for creating automated and customizable conversational flows through Whatsapp.


