# Polygon-Advanced-Module-1: Deploying NFT Collection and Transferring Assets

Welcome to the first project in Polygon-Advance! In this project, your task is to deploy an NFT (Non-Fungible Token) collection on the Ethereum blockchain, establish a connection to the Polygon network, and transfer assets across using the Polygon Bridge.

## Getting Started

To begin, follow these steps:

1. Download the entire repository to access all project contents.
2. Navigate to the "Poly_Proof" project directory and execute the following command to install dependencies:

```shell
npm install
```

3. After installing dependencies, run the test file using this command:

```shell
npx hardhat test
```

## Deploying the ERC721 Contract

Before deploying, ensure to rename ".env.example" to ".env" and provide your wallet's private key where required (e.g., `PRIVATE_KEY='your wallet private key'`). Deploy the ERC721 contract to the Goerli Ethereum Testnet with this command:

```shell
npx hardhat run scripts/deploy.js --network goerli 
```

**Note**: The deployed contract will have a generated address. Copy this address into `contractAddress.js` (located in the metadata folder) and also in `batchMint.js` (located in the scripts folder).

## Batch Minting NFTs

Use the following command to batch-mint NFTs through the deployed ERC721 contract:

```shell
npx hardhat run scripts/batchMint.js --network goerli
```

This script will create the specified number of NFTs and associate them with your address.

## Approving and Depositing NFTs to Polygon Mumbai

Execute these commands to approve and deposit the minted NFTs from Ethereum to the Polygon Mumbai network using the FxPortal Bridge:

```shell
npx hardhat run scripts/approveDeposit.js --network goerli
```

## Author

[DIYA](https://github.com/diya26322632)

## License

This project is licensed under the [MIT License](LICENSE).
