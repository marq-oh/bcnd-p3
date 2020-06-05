# Project: Ethereum Dapp for tracking items

## Description
Third project for Blockchain Developer course, the intent of the project was to create a Dapp supply chain solution backed by the Ethereum platform. This involved architecting smart contracts that manage specific user permission controls as well as contracts that track and verify a product’s authenticity. (See [Original ReadMe](https://github.com/marq-oh/bcnd-p3/blob/master/README_orig.md) for complete instructions)

## Write-Up / Details
### Part 1: Plan the project with write-ups
The main workflow and backend of the application was developed using Smart Contracts (Solidity). The frontend was developed using NodeJs.

There are a total of 4 roles. The flow of how each role communicates with each other, the properties of each role and the functions that each role performs can be understood through the [UML diagrams](https://github.com/marq-oh/bcnd-p3/tree/master/UML). 

### Part 2: Write smart contracts
|Contract            |Description              																				   									   |
|:------------------:|:-------------------------------------------------------------------------------------------------------------------------------------------:|
|ConsumerRole.sol  	 |This contract is used to give an address the Consumer role to be able to purchase an item           					 					   |
|DistributionRole.sol|This contract is used to give an address the Distributor role to be able to mark an item as sold and also ship the item   				   |
|FarmerRole.sol  	 |This contract is used to give an address the Farmer role to harvest, process, pack and sell an item         								   |
|RetailerRole.sol  	 |This contract is used to give an address the Retailer role to receive an item          													   |
|Roles.sol  		 |This contract is used as a library to assign, remove and check roles           																				   |
|SupplyChain.sol  	 |This contract runs and manages the flow of items through each state (Harvested, Procesed, Packed, ForSale, Sold, Shipped, Received, Purchased|        																|
|Ownable.sol  		 |This contract is used as a library to manage the ownership of an item as it passes through the supply chain														   | 
|Migrations.sol  	 |This contract is used as part of the deployment process using truffle				     													   |  

See [contracts folder](https://github.com/marq-oh/bcnd-p3/tree/master/project-6/contracts) for solidity code

### Part 3: Test smart contract code coverage
Ten (10) unit tests were written:
1. Testing smart contract function harvestItem() that allows a farmer to harvest coffee
2. Testing smart contract function processItem() that allows a farmer to process coffee
3. Testing smart contract function packItem() that allows a farmer to pack coffee
4. Testing smart contract function sellItem() that allows a farmer to sell coffee
5. Testing smart contract function buyItem() that allows a distributor to buy coffee
6. Testing smart contract function shipItem() that allows a distributor to ship coffee
7. Testing smart contract function receiveItem() that allows a retailer to mark coffee received
8. Testing smart contract function purchaseItem() that allows a consumer to purchase coffee
9. Testing smart contract function fetchItemBufferOne() that allows anyone to fetch item details from blockchain
10. Testing smart contract function fetchItemBufferTwo() that allows anyone to fetch item details from blockchain

See [test folder](https://github.com/marq-oh/bcnd-p3/blob/master/project-6/test)

### Part 4: Deploy smart contracts on a public test network (Rinkeby)
TBD

### Part 5: Modify client code to interact with smart contracts
Only minor edits were done from the code that was provided

### Optional: Implement Infura to store product image
N/A - This option was not done

### Versions
|            Item           |               Value              |
|:-------------------------:|:--------------------------------:|
|     Node Version   		|             v12.16.1             |
|      Truffle Version      | v5.1.14-nodeLTS.0 (core: 5.1.13) |
| Solidity Compiler Version |          0.6.2 (solc-js)         |
