# MyToken 

This is a Solidity Project "MyToken" program in which we have created to a specific address.

## Description

This project creates a token that may be burned and minted. We can mint new tokens to a specific address to increase the Total supply of the "Anshu" token (ans)," or burn existing tokens from that address to reduce the total supply.

## Getting Started

### Executing program

To run the program use Remix IDE, we have used an Online Platform https://remix.ethereum.org/.

Once you are on the Remix website, create a new file and save the file with a .sol extension (like MyToken.sol). Copy and paste the code into the file:
```javascript
// SPDX-License-Identifier: MIT
pragma solidity 0.8.25;

contract MyToken {

    // state variables here
    string public Name = "Anshu";
    string public symbol = "ans";
    uint public totalSupply = 100;

    // mapping variable here
    mapping( address => uint ) public balance;

    // mint function for creating token
    function mint (address _to, uint _value) public {
        totalSupply += _value;
        balance[_to] += _value;
    }

    // burn function for destroying token
    function burn (address _from, uint _val) public {
        require ( balances[_from] >= _val ) {
            totalSupply -= _value;
            balance[_from] -= _value;
        }        
    }
}
```
Compile the code and then deploy it
Add the address to mint/burn to add or burn the tokens.

## Authors

Anshu

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
