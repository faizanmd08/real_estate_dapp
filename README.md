# Real Estate DApp

A decentralized application for real estate transactions, leveraging Ethereum blockchain technology to enable secure and transparent property transactions through smart contracts.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Smart Contracts](#smart-contracts)
- [Installation](#installation)
- [Usage](#usage)

## Introduction

This Real Estate DApp allows for secure and transparent real estate transactions on the blockchain. Users can list properties, place earnest money in escrow, and proceed through an escrow process managed by smart contracts, with roles for buyer, seller, inspector, and lender.

## Features

- **Property Listings:** Sellers can list properties as NFTs.
- **Escrow Management:** Secure transactions with escrow functionality to protect both parties.
- **NFT Property Ownership:** Each property is represented as a unique NFT.
- **Role Management:** Defined roles include Buyer, Seller, Inspector, and Lender.

## Tech Stack

- **Blockchain & Smart Contracts:** Solidity, Hardhat
- **Frontend:** HTML, CSS, JavaScript, React
- **Libraries:** ethers.js, OpenZeppelin
- **IPFS:** Used for decentralized storage of property metadata

## Smart Contracts

The application includes two primary contracts:

1. **RealEstate.sol:**

   - Manages property NFTs, including minting and transferring ownership.
   - Uses ERC721 standards to represent property as unique assets on the blockchain.

2. **Escrow.sol:**
   - Facilitates the escrow process, ensuring that funds and ownership are transferred only when all approvals are met.
   - Manages buyer-seller agreements, escrow deposits, and transaction conditions.

## Installation

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/faizanmd08/real_estate_dapp.git
   cd real_estate_dapp
   ```

2. **Install Dependencies:**

   ```bash
   npm install
   ```

3. **Compile Contracts:**

   ```bash
   npx hardhat compile
   ```

4. **Deploy Contracts:**
   Deploy the contracts to a local blockchain (Hardhat Network):

   ```bash
   npx hardhat node
   npx hardhat run scripts/deploy.js --network localhost
   ```

5. **Start the Frontend:**
   ```bash
   npm start
   ```

## Usage

1. **Seller Lists Property:**

   - The seller mints a property NFT and lists it on the platform.

2. **Buyer Deposits Escrow:**

   - The buyer deposits an escrow amount for the property in the smart contract.

3. **Inspection Approval:**

   - The inspector verifies the property and approves it for sale.

4. **Final Approvals:**

   - The lender, buyer, and seller each provide final approval to complete the sale.

5. **Finalize Sale:**
   - Once all approvals are complete, ownership of the NFT transfers to the buyer, and the seller receives the funds.
