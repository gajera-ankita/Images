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
- updateNFTPr
