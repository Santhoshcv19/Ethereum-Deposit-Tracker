# Ethereum Deposit Monitoring Application

## Introduction

The Ethereum Deposit Monitoring Application is a TypeScript-based solution that monitors ETH deposits on the Beacon Chain Deposit Contract in real-time. The application interfaces with Ethereum nodes via RPC, logs deposit transactions, sends alerts via Telegram, and visualizes data through a Grafana dashboard.

## Key Features

- **Live Deposit Tracking**: Continuously monitors the Beacon Chain Deposit Contract for new deposits.
- **Comprehensive Logging**: Captures essential details of deposits such as sender, amount, and transaction time.
- **Notifications**: Real-time alerts via Telegram for every new deposit.
- **Visual Data Insights**: Integrates with Grafana to display deposit metrics and trends.
- **Resilient Error Handling**: Ensures logging and error management for robust operations.
- **Containerization**: Supports Docker deployment (under development, may need further improvements).

## Contents

- [Introduction](#introduction)
- [Key Features](#key-features)
- [Contents](#contents)
- [Installation Instructions](#installation-instructions)
- [Configuration Setup](#configuration-setup)
- [How to Run](#how-to-run)
- [Application Usage](#application-usage)
- [Data Structure](#data-structure)
- [Project Scope and Deliverables](#project-scope-and-deliverables)
- [Contributions and Support](#contributions-and-support)

## Installation Instructions

Follow these steps to set up the Ethereum Deposit Monitoring Application:

1. **Clone the Repository**
   ```bash
   git clone [repository-url]
   cd [project-directory]
   ```

2. **Install Node.js and TypeScript**
   - Make sure Node.js is installed, and install TypeScript globally:
     ```bash
     npm install -g typescript
     ```

3. **Install Project Dependencies**
   ```bash
   npm install
   ```

## Configuration Setup

1. **Configure Environment Variables**
   - Create a `.env` file in the project’s root directory with the necessary values:
     ```bash
     ALCHEMY_API_KEY=YOUR_ALCHEMY_API_KEY
     MONGO_URI=YOUR_MONGO_URI
     ETH_BLOCK_FROM=20714004
     TELEGRAM_NOTIFICATIONS_BOT_TOKEN=YOUR_TELEGRAM_BOT_TOKEN
     TELEGRAM_NOTIFICATIONS_CHAT_ID=YOUR_TELEGRAM_CHAT_ID
     ```

## How to Run

1. **Launch the Application**
   ```bash
   npm start
   ```

2. **Run Monitoring and Alerts**
   - Start Prometheus and Grafana services:
     ```bash
     npm run dev-api
     npm run dev
     ```

3. **Access Grafana Dashboard**
   - View real-time deposit data on Grafana by navigating to `http://localhost:3000`.

## Application Usage

1. **Deposit Monitoring**
   - The application automatically tracks deposits from the Beacon Chain Deposit Contract, logging transaction data and displaying metrics in Grafana.

2. **Deposit Alerts**
   - Receive notifications about new deposits in your configured Telegram chat.

## Data Structure

The deposit data model is structured as follows:

```typescript
interface Deposit {
    blockNumber: number;
    timestamp: number;
    fee?: number;
    transactionHash?: string;
    publicKey: string;
}
```

## Project Scope and Deliverables

- A fully functional TypeScript-based application for monitoring ETH deposits.
- Complete source code repository with detailed setup instructions.
- Integrated error logging and notification handling.
- Grafana dashboard for real-time data visualization.
- Telegram notifications for deposit alerts.

## Contributions and Support

If you encounter issues or wish to contribute:

- **Report Issues**: Use the [GitHub Issues page](#) to report bugs or request features.
- **Contribute**: Feel free to submit pull requests or suggest improvements on [GitHub](#).
