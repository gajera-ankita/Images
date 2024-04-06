# MagaNFT Smart Contract Documentation

This README provides an overview of the functionalities and usage of the MagaNFT smart contract.

## Overview

The MagaNFT smart contract facilitates the creation, transfer, and management of MagaNFTs within the NFT ecosystem. It includes functions for minting NFTs, managing approvals, transferring ownership, and more.

## Functions

### Mint
- safeMint: Using SafeMint, you can securely mint your own MagaNFTs, ensuring a smooth and reliable process within the thriving NFT space.

### Approve
- approve: Authorize a designated address to manage the transfer of your MagaNFTs on your behalf, enhancing flexibility in trading and collaboration.
- setApprovalForAll: Conveniently authorize third-party operators to manage your MagaNFTs, streamlining transactions and collaborations.

### Transfers
- transferFrom: Securely transfer MagaNFTs to another user, facilitating smooth and trusted transactions.
- safeTransferFrom: Confidently transfer your MagaNFTs, ensuring secure and seamless transactions.

### Claiming Rewards
- claimMagaCoin: Securely claim MagaCoins associated with specific MagaNFTs, ensuring fair distribution and incentivizing NFT ownership.

### Querying Information
- balanceOf: Query the balance of MagaNFTs associated with a specific address.
- ownerOf: Retrieve the current owner of a specific MagaNFT by its unique identifier.

## OnlyOwner Functions
Certain functions are restricted to the contract owner for administrative purposes.

### Contract Settings
- setMagaCoinAddress: Set the MagaCoin contract address exclusively, ensuring validity and emitting an event for successful address assignment.
- updateNFTPrice: Update the NFT price, allowing only the contract owner to call the function and emit an event signaling the price update.

### Ownership Management
- transferOwnership: Transfer ownership of the contract to a new address.
- renounceOwnership: Renounce ownership, removing the contract owner and leaving the contract without an owner.

## Usage
To use the MagaNFT contract, follow these steps:
1. Mint your MagaNFTs using the safeMint function.
2. Authorize designated addresses for managing transfers with approve or setApprovalForAll.
3. Transfer MagaNFTs securely using transferFrom or safeTransferFrom.
4. Claim MagaCoins associated with your MagaNFTs using claimMagaCoin.
5. Query information about your NFTs using balanceOf and ownerOf.
6. Utilize administrative functions such as setMagaCoinAddress and updateNFTPrice if you are the contract owner.

## Contract Deploy steps
1. Deploy magaNFT contract first.
2. Deploy Magacoin using magaNFT contract address.(The initial supply of 5,000,000 MAGA will be minted by the entity deploying this contract.)
3. call "setMagaCoinAddress" function using Magacoin contract address.
