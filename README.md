# Ethereum Dapp for Tracking Items through Supply Chain
This repository containts an Ethereum DApp that demonstrates a Supply Chain flow between a Seller and Buyer. The user story is similar to any commonly used supply chain process. A Seller can add items to the inventory system stored in the blockchain. A Buyer can purchase such items from the inventory system. Additionally a Seller can mark an item as Shipped, and similarly a Buyer can mark an item as Received.

Original project details repo is available at https://github.com/udacity/nd1309-Project-6b-Example-Template

## Solution Submission Details

### Project Write-up - UML
Below are the UML diagrams for this project.

#### Activity Diagram
![image](https://user-images.githubusercontent.com/65207094/147897073-a66ff03e-4db2-48a7-afe8-b14aff0ad6ea.png)

#### Sequence Diagram
![image](https://user-images.githubusercontent.com/65207094/147897191-61ab0cbd-6a48-455b-8971-5742eaab9850.png)

#### State Diagram
![image](https://user-images.githubusercontent.com/65207094/147898833-46c477f1-67c6-4da1-8b1f-3c63ebe0d5dd.png)

#### Classes (Data Model)
![image](https://user-images.githubusercontent.com/65207094/147899622-63598e87-79d4-4349-9abf-d3e09a17981f.png)

### Project write-up - Libraries
Below are the libraries used in this project.
```
Truffle v5.4.22 (core: 5.4.22) - Used for compiling, migrating and testing contracts
Solidity - 0.8.4 (solc-js) - Language compiler
Node v16.13.0 - Node runtime
Web3.js v1.5.3 - Javascript library to interact with metamask
truffle-hdwallet-provider: ^1.0.17 - Used to deploy contract to Raspen network.
Ganache GUI: 2.5.4 - Local block chain for development and testing purpose.
```

### Project write-up - IPFS
No IPFS is used in this project.

### Project write-up - General
- Download the project from the github repo.
- Set up the Ganache GUI to create a local workspace with truffle-config.js. Use the MNEMNIC "canyon decide cause palace clever model stadium tragic syrup knee such squirrel" to create 10 local accounts.
```
The first 5 accounts are used in this project.
Contract Owner: accounts[0]  0x7De58d745a65dA98aD0d6517a8BA0e6D605A142F
Farmer: accounts[1]  0xb0806462eED82e639F599457d824DfB77206F7f7
Distributor: accounts[2]  0x08D10A13e235942c6c63037354A64605f4536eE0
Retailer: accounts[3]  0x5C1db1b86dB5636EdEb42372FE49D5274E331fd1
Consumer: accounts[4]  0xbC99B61483279709e6932F33041702F692FD8584
```
- Run the below commands
```
cd BC_UDA_PROD3
truffle compile
truffle migrate
npm install
```

## Testing the Contracts

```
truffle test
```

```
Contract Owner: accounts[0]  0x7De58d745a65dA98aD0d6517a8BA0e6D605A142F
Farmer: accounts[1]  0xb0806462eED82e639F599457d824DfB77206F7f7
Distributor: accounts[2]  0x08D10A13e235942c6c63037354A64605f4536eE0
Retailer: accounts[3]  0x5C1db1b86dB5636EdEb42372FE49D5274E331fd1
Consumer: accounts[4]  0xbC99B61483279709e6932F33041702F692FD8584


  Contract: SupplyChain
    ✓ Testing smart contract function harvestItem() that allows a farmer to harvest coffee (429ms)
    ✓ Testing smart contract function processItem() that allows a farmer to process coffee (203ms)
    ✓ Testing smart contract function packItem() that allows a farmer to pack coffee (132ms)
    ✓ Testing smart contract function sellItem() that allows a farmer to sell coffee (139ms)
    ✓ Testing smart contract function buyItem() that allows a distributor to buy coffee (169ms)
    ✓ Testing smart contract function shipItem() that allows a distributor to ship coffee (135ms)
    ✓ Testing smart contract function receiveItem() that allows a retailer to mark coffee received (157ms)
    ✓ Testing smart contract function purchaseItem() that allows a consumer to purchase coffee (235ms)
    ✓ Testing smart contract function fetchItemBufferOne() that allows anyone to fetch item details from blockchain (52ms)
    ✓ Testing smart contract function fetchItemBufferTwo() that allows anyone to fetch item details from blockchain
```

## Running the dApp UI
Make sure to add the local accounts to metamask plugin
- Contract Owner: 0x7De58d745a65dA98aD0d6517a8BA0e6D605A142F
- Farmer: 0xb0806462eED82e639F599457d824DfB77206F7f7
- Distributor: 0x08D10A13e235942c6c63037354A64605f4536eE0
- Retailer: 0x5C1db1b86dB5636EdEb42372FE49D5274E331fd1
- Consumer: 0xbC99B61483279709e6932F33041702F692FD8584

```
npm run dev
```

- Select Owner account in metamask and click Set Actors in the DApp UI. This will set account roles. 
- Select Farmer account in metamast and perform Harvest, Process, Pack and Forsale actions. 
- Select Distributer account in metamask and perform Buy and Ship actions. 
- Select Retailer account in metamast and perform Receive actions. 
- Select Consumer account in metamask and perform Purchase actions. 

```
Transaction History
Harvested - 0x8be61f5123011dab63040bd1d84d9bead40b053ff6a3e193bd00b9883d98aa83
Processed - 0x8d52ff7b52c70f9d0e28f2f6ae6333848f36867654e3fe860c0360081bd2e266
Packed - 0x6712e911c3f80be5189b4c2d3a91aaa283735df3114825e3505160cbbfac7efe
ForSale - 0xf65c4d48db4b5fc605ebff906a5e92826bfb7453122392c2a2e6fd9c1a7621ad
Sold - 0x682e01dc198065a0e781a7981aaf532e9be6de4d4bc212a4466097b3db7cece1
Shipped - 0x39f9117385f9a4278616be5b44dfc3c0b46ae176edf5bf9f3859c7151ff88c26
Received - 0x7fbad2784ac19b34703d0694563e708d21d9a19f3893dbd323712944838a4d46
Purchased - 0xfa27ca752e1c7690c9b5e2e22f7028c39f8594a9d53787c0ba1c0204cdcb25dc
```

## Contract Deployment and Transaction details
Rapsten contract address

```
   Deploying 'SupplyChain'
   -----------------------
   > transaction hash:    0x829be607d19784434603d1b909cdd876b69c5db58dd9416b73ff78063e6631d6
   > Blocks: 0            Seconds: 16
   > contract address:    0xF9Bbd3AAa7B95ec98a2c006d77618e04C6770093
   > block number:        11736805
   > block timestamp:     1641117410
   > account:             0xcccc1d966393E28A6589cd4bE9a8D6cE4a0d55B9
   > balance:             0.188398085075295969
   > gas used:            2809271 (0x2addb7)
   > gas price:           1.500000007 gwei
   > value sent:          0 ETH
   > total cost:          0.004213906519664897 ETH
```
