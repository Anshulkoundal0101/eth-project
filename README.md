# Create a Token

The Anshulk_token contract is a simple ZNC token in the blockchain.
It lets you create (print ) and destroy (burns ) token.The contract
include the public variable to track the token name,symbol,and 
total supply.It also keep tack on the each address's token balance.

## Description
The Anshulk_token contact is a basic ZNC like token  on thr etherium
blockchain.it incldes the following features  like token details ,
balance tracking , events.

The main function includes constructor :initilize the token with a name
,symbol ,number of the decimals and initial supply.Assign the total 
supply to the contract deployer.

pragrma solidity 0.8.26:This lines speifies the version  of the solidity
compiler to use.The contract is written using solidity version 0.8.26.
Mapping:"ans" :A mapping that help to minu new token and distributr them 
to a specific address.

##Getting Started
### Installing
To download the code please follow this path:-
(https://github.com/Anshulkoundal0101/eth-project/tree/main)

###executing program


pragrma solidity 0.8.26:This lines speifies the version  of the solidity
compiler to use.The contract is written using solidity version 0.8.26.
For run this code use this website(https://remix.ethereum.org/#lang=en&optimize=false&runs=200&evmVersion=null&version=soljson-v0.8.26+commit.8a97fa7a.js)
Mapping:"ans" :A mapping that help to minu new token and distributr them 
to a specific address.The solidity code defines a basic token contract
named"Anshulk_token".
This contract faclitiates the creation ,distribution,and destruction of
the token.The contract adhere to a set of requirement outlined in command
at the beginning of the code.
```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.26;

/*
       REQUIREMENTS
    1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
    2. Your contract will have a mapping of addresses to balances (address => uint)
    3. You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the “sender” address by that amount
    4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the “sender”.
    5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
       to the amount that is supposed to be burned.
*/

contract Anshulk_token {

    // public variables here
    string public tokenName ="Zenithcoin";
    string public tokenAbb ="ZNC";
    uint public totalSupply = 0;
    // mapping variable here
    mapping (address=>uint) public ans;

    // mint function
   function mint(address _address,uint _value)public{
      totalSupply +=_value;
      ans[_address]+=_value;

   }
    // burn function
    function burn (address _address,uint _value)public{
         if( ans[_address]>=_value){
         totalSupply-=_value;
         ans [_address]-=_value;
         }
}
}
```
To compile the code, click on the "Solidity Compiler" tab in the left-hand 
sidebar.Make sure the "Compiler" option is set to "0.8.26", and then click
on the "Compile Meta.sol" button.

## Authors
Anshul koundal @Anshulkoundal0101


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
