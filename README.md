# NFT

# Degen Gaming Token

Degen Gaming Token is an ERC20 token smart contract designed for the Degen Gaming platform on the Avalanche network. The smart contract provides functionalities for minting new tokens, transferring tokens, redeeming tokens, checking token balances, and burning tokens.

## Features

- Minting New Tokens: The owner of the contract can create new tokens and distribute them as rewards to players.
- Transferring Tokens: Players can transfer their tokens to others using the `transfer` function.
- Redeeming Tokens: Players can redeem their tokens for items in the in-game store.
- Checking Token Balance: Players can check their token balance at any time using the `balanceOf` function.
- Burning Tokens: Anyone who owns tokens can burn them if they are no longer needed.

## Deployment

The contract can be deployed on the Avalanche network using tools such as Remix, Truffle, or Hardhat. When deploying the contract, make sure to set the following parameters:

- `name`: The name of the token (e.g., "Degen Gaming Token").
- `symbol`: The symbol or ticker of the token (e.g., "DGT").
- `decimals`: The number of decimals for token divisibility (e.g., 18).
- `initialSupply`: The initial supply of tokens to be created.

## Getting Started

To interact with the Degen Gaming Token contract, you can use an Ethereum-compatible wallet or write custom scripts. Below are a few examples of how to interact with the contract using the `web3.js` library in JavaScript:

1. Get the token balance of an address:

   ```javascript
   const contract = new web3.eth.Contract(contractABI, contractAddress);
   const balance = await contract.methods.balanceOf(address).call();
   console.log(`Token balance of ${address}: ${balance}`);
