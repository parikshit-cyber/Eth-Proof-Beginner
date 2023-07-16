# Solidity Assignment
This Solidity Assignment is a part of the ETH Proof Beginner Course that demonstrates the working and
application of web 3.0  and also gives a background on Ethereum and the Ethereum Virtual Machine (EVM).
It explains decentralization and existence of decentralized finance (deFi) and decentralized applicatios (dApps)

# Description
In this program which I have written using the IDE Remix for Solidity, which is a programming language used for
writing smart contracts on the Ethereum Blockchain. This ccontract has 3 public variables that store data about the Token Name, Token Abbreviation and the total supply. I then create a public mapping variable called balances which is mapped from the address to the value. I then create two public functions called mint and burn, where mint is supposed to credit tokens to the provided address and the burn function is supposed to debit tokens from the address after confirming the presence of the amount of tokens using an if loop.

# Getting Started
## Executing 
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

```solidity
  // SPDX-License-Identifier: MIT
  pragma solidity 0.8.18;

  contract MyToken {

    // public variables here
    string public tokenName = "APPLE";
    string public tokenAbbrv = "APP";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address _address, uint _value) public 
    {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn(address _address, uint _value) public 
    {
        if( balances[_address] >= _value)
        {
            totalSupply -= _value;
            balances[_address] -= _value;

        }
    }
}
```

Once the code is `compiled`, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.
Once the contract is deployed, you can interact with it by calling the mint and burn functions. You can add and subtract tokens using the dropdown menu along the mint and burn functions and entering the value to be operated.

# Author
PARIKSHIT SINGH BAGHEL
[Linkedin](https://www.linkedin.com/in/parikshit-siingh)
