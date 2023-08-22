
# MyToken Solidity Contract

This is a simple Solidity smart contract named MyToken that implements a basic token functionality. It allows for minting and burning tokens, and also keeps track of token balances for different addresses.

## Table of Contents

- [Introduction](#introduction)
- [Contract Details](#contract-details)
- [Usage](#usage)
  - [Minting Tokens](#minting-tokens)
  - [Burning Tokens](#burning-tokens)


## Introduction

MyToken is a basic Solidity contract that demonstrates a simple token implementation. It includes features like token minting and burning, as well as tracking balances for different addresses.

## Contract Details

- **Solidity Version:** 0.8.18
- **License:** MIT

### Public Variables

- `tokenName`: The name of the token. In this contract, it's set to "Ratheesh".
- `tokenAbbrv`: The abbreviation or symbol of the token. Here, it's "RTH".
- `totalSupply`: The total supply of tokens. Currently set to 0.

### Mapping Variable

- `balances`: A mapping that associates addresses with their token balances.

## Usage

This section provides details on how to use the contract's minting and burning functions.

### Minting Tokens

The `mint` function allows you to create new tokens and assign them to a specific address.

```solidity
function mint(address _address, uint _value) public {
    totalSupply += _value;
    balances[_address] += _value;
}
```

To mint new tokens, call the `mint` function with the target address and the amount of tokens you want to mint.

### Burning Tokens

The `burn` function lets you destroy tokens held by a specific address.

```solidity
function burn(address _address, uint _value) public {
    totalSupply -= _value;
    balances[_address] -= _value;
}
```

To burn tokens, call the `burn` function with the target address and the amount of tokens you want to burn.

