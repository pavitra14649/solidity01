MyToken: A Basic ERC-20 Token Contract (Solidity)
This Solidity contract implements a basic ERC-20 token named "META" (tName) with the symbol "MTA" (tSymbol). It allows minting and burning of tokens, but lacks some functionalities for a fully functional token.

Features:

Stores token name, symbol, and total supply.
Tracks token balances for each address using a mapping.
Allows minting new tokens for a specified address.
Allows burning tokens held by the sender address.
Requirements:

Solidity compiler version >= 0.8.18
Deployment:

Compile the contract using a Solidity compiler.
Deploy the contract to a blockchain network (e.g., test network).
Interact with the contract functions using a web3 wallet or development tools.
Limitations:

This is a simplified example and doesn't include features like:
Transferring tokens between addresses.
Access control for minting and burning functions.
Events to notify about token transfers.
Consider adding these features for a more robust token implementation.
Usage:

Call the mint function to mint new tokens for a specific address.
Call the burn function to burn tokens held by the sender address (ensure sufficient balance).
Security:

This is a basic example and might not be secure for real-world use cases.
Always thoroughly test your smart contract before deploying it to a live network.
Further Development:

Implement transfer functionality between addresses.
Add access control mechanisms for minting and burning.
Include events to track token transfers.
Explore additional ERC-20 functionalities.
License:

MIT License

Author: Pavitra Pal 
