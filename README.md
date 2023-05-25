## Rafidul_Islam_SmartContract7
### Remix fund me

### Sending ETH through a function and reverts

We have created new solidity file which is ```rafiFundMe.sol```<br>

rafiFundme.sol is a contract designed for collecting funds in various cryptocurrencies, such as Ethereum or Polygon. Users can contribute to the contract, and its owner will have control over how those funds are utilized. The contract also allows for withdrawing funds and setting a minimum funding threshold in USD.


Figure1: open a new solidity file ```rafiFundMe.sol```


figure2: Going to this link https://eth-converter.com/ we can find relation beteen ether,GWEI and WEI.<br>


When the payable keyword is used with a function, it enables the acceptance of native blockchain currencies, making the associated button appear in red color. Similar to wallets, smart contract addresses can also hold funds. Smart contract addresses and wallet addresses are nearly identical, and both have the capability to store native blockchain tokens such as Ethereum.
```
//SPDX-License-Identifier:MIT

pragma solidity ^0.8.8;

contract rafiFundMe  {

// we have use payable keyword with the function below to make it payable with any native blockchain currency
    function fund() public payable {

        require(msg.value > 1e18 , "Insufficient transmission");// to get accees to the 'value' at deploy at run transaction tab
        //1e18 is 1 ether, here the value must be greater than 1 ether
        //require is a checker it checks whether the value is greater than 1 ether
        // if not it is going to revert with an error messsage shown above

    }// To send money. We made it public so that anybody can call it



   

}

```


Figure3: Output after we deployed


Figure4: error occured as we have no enough ether to send to this contract<br>



reverting occurs for this line  ```require(msg.value > 1e18 , "Insufficient transmission");```


figure5: we set the value to 3 and successfully occured
