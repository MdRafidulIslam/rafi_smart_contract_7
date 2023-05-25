## Rafidul_Islam_SmartContract7
### Remix fund me

### Sending ETH through a function and reverts

We have created new solidity file which is ```rafiFundMe.sol```<br>

rafiFundme.sol is a contract designed for collecting funds in various cryptocurrencies, such as Ethereum or Polygon. Users can contribute to the contract, and its owner will have control over how those funds are utilized. The contract also allows for withdrawing funds and setting a minimum funding threshold in USD.

![r1 (1)](https://github.com/MdRafidulIslam/rafi_smart_contract_7/assets/86659473/c688b1f5-c86a-49d7-b0a0-b31dc074aa19)

Figure1: open a new solidity file ```rafiFundMe.sol```

![r2 (1)](https://github.com/MdRafidulIslam/rafi_smart_contract_7/assets/86659473/4dbee080-2482-46c7-94e0-e3d5223cd80d)

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

![r3 (1)](https://github.com/MdRafidulIslam/rafi_smart_contract_7/assets/86659473/4598acac-6c82-426e-a3cf-829f72aa22c8)

Figure3: Output after we deployed

![r4](https://github.com/MdRafidulIslam/rafi_smart_contract_7/assets/86659473/775bbbcc-853f-4f70-8596-376576869b8b)

Figure4: error occured as we have no enough ether to send to this contract<br>



reverting occurs for this line  ```require(msg.value > 1e18 , "Insufficient transmission");```

![r5](https://github.com/MdRafidulIslam/rafi_smart_contract_7/assets/86659473/d8b83d71-0beb-4ad7-94b9-ece8cdac4dde)

figure5: we set the value to 3 and successfully occured
![r6](https://github.com/MdRafidulIslam/rafi_smart_contract_7/assets/86659473/02569f32-489b-4bfe-a257-c48a084efae4)
figure6:
