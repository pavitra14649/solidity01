
MyToken Contract


Overview


The MyToken contract is a simple implementation of a cryptocurrency token on the Ethereum blockchain. It allows for the minting and burning of tokens, and keeps track of balances associated with addresses. The contract includes functionality to store and retrieve the token's name, abbreviation, and total supply.

Requirements


Public variables for storing token details:
Token Name
Token Abbreviation
Total Supply
A mapping to keep track of balances associated with addresses.
A mint function to create new tokens.
A burn function to destroy tokens with checks to ensure sufficient balance.

Contract Details


Public Variables
string public tName = "META";
Stores the name of the token.
string public tSymbol = "MTA";
Stores the abbreviation (symbol) of the token.
uint public totalSupply = 0;
Stores the total supply of the token, initialized to 0.

Mapping


mapping(address => uint256) public balances;
Keeps track of the balance of tokens for each address.

Functions


mint

     function mint(address _address, uint _value)public {
     totalSupply += _value;
     balances[_address] += _value;
    }

    
Parameters:


_address: The address to which the minted tokens will be credited.


_value: The amount of tokens to be minted.


Functionality:


Increases the total supply of tokens by the specified value.
Increases the balance of the specified address by the specified value.

'burn'
        
	function burn(address _address, uint _value) public {
        if(balances[_address] >= _value) {
        totalSupply -= _value;
        balances[_address] -= _value;
              }
          }

   Parameters:

   
_address: The address from which the tokens will be burned.


_value: The amount of tokens to be burned.


Functionality:



Checks if the balance of the specified address is greater than or equal to the specified value.


If the check passes, decreases the total supply of tokens by the specified value.


Decreases the balance of the specified address by the specified value.



Usage


Deploy the Contract: Deploy the MyToken contract to the Ethereum blockchain.


Mint Tokens: Call the mint function with the desired address and amount to create new tokens and credit them to the address.


Burn Tokens: Call the burn function with the desired address and amount to destroy tokens, ensuring the address has sufficient balance.


License


This contract is licensed under the MIT License.
