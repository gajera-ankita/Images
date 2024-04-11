his is a smart contract written in Solidity, which is a programming language for implementing smart contracts on Ethereum blockchain. 

The contract contains several parts including ERC20 Token interface definition, Vesting contract definition with its various functionalities like creating vesting schedule for investors, viewing completed vesting months, view total vesting amount available for withdrawal, and withdraw tokens based on a vesting schedule. 

Here's a brief overview of what each part does:

1. **ERC20 Token interface** - This defines a set of functions required by ERC20 tokens to interact with smart contracts on Ethereum. It includes basic token operations like transfer, transferFrom and balanceOf. 

2. **Vesting contract** - This contract manages vesting schedules for investors. 

   - The constructor sets the token contract address. 
   
   - The createVesting function sets up a vesting schedule for each investor by initializing various parameters such as locked wallet amount, vesting time, cliff period, starting withdrawable amount, unlock date etc. 
   
   - The CompletedVestingMonth function allows users to view the number of completed vesting months for a specific user. 
   
   - The withdrawableAmount function allows users to view the total vesting amount available for withdrawal by a specific user. 
   
   - The withdrawTokens function allows users to withdraw tokens based on a vesting schedule. 
   
   - The contract also emits an event whenever tokens are withdrawn. 
   
This contract seems to be intended to be used for token vesting schedules on Ethereum blockchain. The token holder can create a vesting schedule for investors by adding wallet addresses, token amounts, vesting times, cliff periods, and starting withdrawable percentages of tokens for each wallet. The contract will automatically transfer tokens to this contract upon creation of vesting schedule and holders can withdraw their tokens on schedule. The contract also has features to view total vesting amount available for withdrawal by a specific user and to view completed vesting months for a specific user. 

Please note that this is a simple contract for understanding purposes only and lacks important security measures like access control (only token holder can create vesting) or input validation checks (like max wallet limit). In production level smart contracts, these checks should be more robust.our MagaNFTs, ensuring secure and seamless transactions.

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

## How to depoly contract on mainnet

## Prerequisites

- Install the MetaMask browser extension and set up your Ethereum/Avalanche-C chain account.
- Access Remix IDE in your web browser.

## Steps

1. **Compile Smart Contract:**
   - Open Remix and go to the "Solidity Compiler" tab.
   - Select the appropriate compiler version for your contract.
   - Write or import your smart contract code.
   - Click on the "Compile" button to compile the contract.

2. **Deploy Contract:**
   - Switch to the "Deploy & Run Transactions" tab in Remix.
   - Choose "Injected Provider MetaMask" as the environment to connect Remix with MetaMask.
   - Ensure MetaMask is unlocked and set to the Avalanche-C chain mainnet.
   - Select the contract to deploy from the dropdown menu.
   - Enter any constructor parameters required by your contract (if applicable).
   - Click on the "Deploy" button to initiate the deployment.

3. **Confirm Transaction in MetaMask:**
   - MetaMask will open a popup window showing the deployment transaction details.
   - Review the gas fee and other details.
   - Click "Confirm" to submit the transaction.

4. **View Contract Address:**
   - After successful deployment, Remix will display the deployed contract's address.
   - Copy this contract address for future interactions with your contract.

## Troubleshooting

- If the deployment fails, check for error messages in Remix or MetaMask for more details.
- Ensure your MetaMask account has enough ETH/AVAX to cover gas fees for the transaction.

## BSC Testnet Transaction
```
MagaNFT Contract Deployment
- Contract Address: [0x139fa7DeFB26D177474Fdccd4274fE619a22317A](https://testnet.bscscan.com/address/0x139fa7DeFB26D177474Fdccd4274fE619a22317A#code)
- Deployment Transaction: (https://testnet.bscscan.com/tx/0x79572d097400e9e8476584260eede47874a8a03eaa97b173821b5781e4281ff8)

Magacoin Contract Deployment
- Contract Address: [0xC30573f1D8b50F1Dd7e6E00E37e9dFcbf0757981](https://testnet.bscscan.com/address/0xC30573f1D8b50F1Dd7e6E00E37e9dFcbf0757981#code)
- Deployment Transaction: (https://testnet.bscscan.com/tx/0x4d3819c4202a490b71b0ed69b55be8dda5f8ae20051442987da5ab73de705a27)


Set Magacoin Address

- Transaction: (https://testnet.bscscan.com/tx/0x1949f12f735d39ffd143b91a112ada70ebc28e73d2f527f39c4645d8e9dc2896)

Other Transactions

- Update NFT Price (onlyOwner): (https://testnet.bscscan.com/tx/0x203835c6777d5688b6ef1394cf6c7ecbb7763fb42078e5bf8c05daf6c9934e33)
- Approve Transaction: (https://testnet.bscscan.com/tx/0x9449d50523a4f30d806c17304ea38471fbf22b803c9d94422a87e5c1868c335b)
- Transfer From Transaction: (https://testnet.bscscan.com/tx/0x67fdcb3fc343b4b321eae45af91371691dd694d633199111040558077fe410d6)
                             (Note: ClaimMagaCoin transaction failed due to claim time)
- Transfer Ownership (onlyOwner): (https://testnet.bscscan.com/tx/0x84630ce0a0851b7e1caab5493a3f8cf28d0f23f007dd83bb994636c037d31973)

Notes

- Ensure you are connected to the BSC Testnet network on your MetaMask to view these transactions and contracts.
- Check transaction details for gas fees and confirmations.
```
