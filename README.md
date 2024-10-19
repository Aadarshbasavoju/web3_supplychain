# Web3 Supply Chain for Medicine

## Overview
This project implements a decentralized supply chain management system for the pharmaceutical industry using blockchain technology. The smart contract is built using **Solidity**, with **IPFS** and **Pinata** for decentralized file storage. The front end provides an interface for interacting with the blockchain, ensuring transparency, security, and immutability at every stage of the medicine's supply chain.

## Features
- **Decentralized and Transparent**: Tracks the journey of medicines from raw material suppliers to consumers on the blockchain.
- **Immutable Records**: Every action, from raw material supply to the sale of the medicine, is permanently stored on the blockchain.
- **Role-based Access Control**: Only authorized roles (e.g., raw material suppliers, manufacturers, distributors, retailers) can perform actions within their domain.
- **Stage-based Tracking**: The medicine's lifecycle is tracked through five key stages: `RawMaterialSupply`, `Manufacture`, `Distribution`, `Retail`, and `Sold`.
- **Front-end Integration**: Users can interact with the smart contract through a user-friendly interface.

## Technologies
- **Solidity**: Smart contracts that manage roles and medicine lifecycle.
- **IPFS/Pinata**: Decentralized storage for medicine records.
- **Truffle**: Framework for smart contract deployment and testing.
- **Web3.js**: JavaScript library for interacting with Ethereum.
- **Front-end**: User interface for interacting with the blockchain (details pending).

## Smart Contract Architecture

### Roles
- **Raw Material Supplier**: Provides the materials required for manufacturing.
- **Manufacturer**: Produces the medicines following safety guidelines.
- **Distributor**: Distributes medicines to retailers.
- **Retailer**: Sells medicines to consumers.

### Stages
The medicine passes through the following stages:

1. **Init** – Medicine order is created.
2. **RawMaterialSupply** – Raw materials supplied.
3. **Manufacture** – Medicine is manufactured.
4. **Distribution** – Medicine is sent to the distributor.
5. **Retail** – Medicine reaches the retailer.
6. **Sold** – Medicine is sold to the consumer.

## Smart Contracts

### SupplyChain.sol
This contract manages the entire supply chain of medicines, from raw material supply to final sale. It allows the owner to authorize and manage the roles of raw material suppliers, manufacturers, distributors, and retailers.

#### Functions:
- `addRMS()`, `addManufacturer()`, `addDistributor()`, `addRetailer()`: Functions for the owner to add authorized users to the supply chain.
- `addMedicine()`: Owner can add new medicines to the supply chain.
- `RMSsupply()`, `Manufacturing()`, `Distribute()`, `Retail()`, `sold()`: Functions to move the medicine through different stages.
- `showStage()`: View the current stage of a specific medicine.

### Migrations.sol
Handles the deployment process for the smart contract using the Truffle framework.

## Deployment
### Install dependencies:
npm install

### Compile the contracts:
truffle compile

### Deploy the contracts to a blockchain (local or testnet):
truffle migrate

### Interactions:
You can interact with the smart contracts using a front-end UI or directly through Truffle Console:
truffle console

### Testing:
Run unit tests for the smart contracts:
truffle test

## Future Work
- Front-end integration with Web3 for user-friendly interaction.
- Add IPFS/Pinata for decentralized storage of medicine-related documents.
- Expand the supply chain to include more granular roles and stages.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.
