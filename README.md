# assessment2meta
Overview
MyToken is a simple ERC20-like smart contract implemented in Solidity. It allows for basic token operations such as minting and burning tokens. The contract keeps track of token balances and the total supply of tokens.

Features
Token Name: Ansh
Token Abbreviation: ASH
Initial Total Supply: 0
Public Variables
string public tokenName = "Ansh";
string public tokenAbbrv = "ASH";
uint public totalSupply = 0;
Mapping
mapping (address => uint) public balances;
This mapping keeps track of the balance of tokens for each address.
Functions
Mint
function mint(address _address, uint _value) public

Increases the totalSupply by _value.
Adds _value tokens to the balance of _address.
Burn
function burn(address _address, uint _value) public

Decreases the totalSupply by _value.
Subtracts _value tokens from the balance of _address, provided _address has at least _value tokens.
Usage
Minting Tokens:

To mint new tokens, call the mint function with the recipient's address and the number of tokens to be minted.
Example: mint(0x1234..., 100); will mint 100 tokens to the address 0x1234....
Burning Tokens:

To burn tokens, call the burn function with the address from which tokens should be burned and the number of tokens to be burned.
Example: burn(0x1234..., 50); will burn 50 tokens from the address 0x1234... if that address has at least 50 tokens.
