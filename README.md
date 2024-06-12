# MyToken

A simple smart contract for creating and managing a custom token on the Ethereum blockchain.

## Description
This project demonstrates a basic implementation of an Ethereum smart contract for a token named "Lucifer" with the abbreviation "Lir". The contract allows for minting and burning of tokens, keeping track of balances for different addresses.

## Getting Started

### Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

To compile using Remix IDE:

Open Remix IDE.
create a new file by clicking on the "+" icon in the left-hand sidebar and then paste the provided smart contract code.
Click on the "Solidity Compiler" tab and compile the contract.
Deploy the contract using the "Deploy & Run Transactions" tab.
use any one account address given to run the program and check with transactions.
```
pragma solidity 0.8.18;

contract MyToken {
    // public variables here
    string public tokenName = "Lucifer";
    string public tokenAbbrv = "Lir";
    uint public totalSupply = 0;

    // mapping variable here
    mapping (address => uint) public balances; 

    // mint function
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }
    // burn function
function burn(address _address, uint _value) public {
    if (balances[_address] >= _value){
        totalSupply -= _value;
        balances[_address] -= _value;
    }
    }
}
```

## Help
If you encounter any issues, ensure that:

You have a compatible version of Solidity (0.8.18).


## Authors

Manav Singh


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
