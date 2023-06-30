# ether-assessment
# Project Title
Token Creation
# Description
To run this program, you can use Remix, an online Solidity IDE. 
This code provides a basic implementation of a token contract with the ability to mint and burn tokens, while keeping track of the token balances for each address.
The MyToken contract represents a basic token contract. It includes the following functionalities:
### Public variables:
tokenName: A string variable that stores the name of the token.
tokenAbb: A string variable that stores the abbreviation of the token.
totalSupply: An unsigned integer variable that represents the total supply of the token.
#### code: // public variables here
    string public tokenName = "Token";
    string public tokenAbb = "Tok";
    uint public totalSupply = 0;

### Mapping variable:
 #### code: // mapping variable here
    mapping (address => uint) public balances;
balances: A mapping that associates addresses with their token balances. It maps an address to the corresponding balance of tokens held by that address.

### Mint function:
  The mint function allows the creation of new tokens. It takes two parameters: Address (the address to mint tokens to) and Value (the number of tokens to mint).
Inside the function, it increases the total supply by the specified Value and increases the balance of the Address by that amount.
#### code:  // mint function
    function mint(address Address, uint Value) public{
      totalSupply += Value;
      balances [Address] += Value;
    }
    
### Burn function:
The burn function allows the destruction of existing tokens. It takes two parameters: Address (the address from which to burn tokens) and Value (the number of tokens to burn).
It checks if the balance of the Address is greater than or equal to the Value to be burned. If the condition is true, it reduces the total supply by the specified Value and decreases the balance of the Address by that amount.
  #### code: // burn function
function burn(address Address, uint Value) public{ 
 if (balances [Address] >= Value){
      totalSupply -= Value;
      balances [Address] -= Value;
    }
    }

# Authors
Hilina Amare Dechasa 
21CBS1058@cuchd.in


# License
This project is licensed under the MIT License License - see the LICENSE.md file for details




