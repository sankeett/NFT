# NFT

# Degen Gaming Token

Degen Gaming Token is an ERC20 token smart contract designed for the Degen Gaming platform on the Avalanche network. The smart contract provides functionalities for minting new tokens, transferring tokens, redeeming tokens, checking token balances, and burning tokens.

## Features

- Minting New Tokens: The owner of the contract can create new tokens and distribute them as rewards to players.
- Transferring Tokens: Players can transfer their tokens to others using the `transfer` function.
- Redeeming Tokens: Players can redeem their tokens for items in the in-game store.
- Checking Token Balance: Players can check their token balance at any time using the `balanceOf` function.
- Burning Tokens: Anyone who owns tokens can burn them if they are no longer needed.

- The MyToken contract is an ERC20 token contract that extends the ERC20 contract from the OpenZeppelin library. It includes additional functionality for minting and burning tokens, as well as a custom redeem function and a showStore function. Here is an overview of the contract's functionality:

Contract Details
Name: MyToken
Symbol: DRT
Constructor
The constructor initializes the contract and sets the contract owner as the deployer of the contract.

Modifiers
onlyOwner
This modifier restricts certain functions to be called only by the contract owner. It checks whether the caller is the contract owner and reverts the transaction if not.

Functions
mint
The mint function allows the contract owner to create and distribute new tokens. It takes two parameters: to (the address to which the tokens will be minted) and amount (the number of tokens to mint). Only the contract owner can call this function.

burn
The burn function allows any token holder to burn a specific amount of their own tokens. It takes the amount of tokens to be burned as a parameter.

transfer
The transfer function overrides the transfer function from the ERC20 contract. It allows token holders to transfer tokens to other addresses. It checks if the sender has sufficient balance before executing the transfer.

redeem
The redeem function is an external function that can be called by anyone. It takes an item parameter that represents the item to be redeemed. Depending on the value of item, a specific amount is determined. If the amount is greater than 0, the function burns that amount of tokens from the sender's balance.

showStore
The showStore function is an external pure function that returns a string representing the available items in the store. The returned string lists three items with their corresponding redemption amounts.

