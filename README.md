# DaiVinity **MeetYourMaker** NFT Contract

The DaiVinity NFT contract is based on the ERC721A contract specs. The contract us a whitelist mint only contract. Minting costs are zero.

**Rinkeby Contract Address**: ***0x96F1a12c14155F5732009CE3dc5a49b687A1C436***

## Prerequisites
The best way to test and deploy this contract is by using the remix ide. The imports are optimized for this. The easiest way to use this repository is by using Remixd. 
You can clone this repo locally

## Installation using remixd
run:
npm i @remix-project/remixd
remixd -s ~/YOUR_PROJECT_FOLDER --remix-ide https://remix.ethereum.org/

Visit: https://remix.ethereum.org/
Select localhost as workspace

## Manual installation using the Remix-IDE

Visit: https://remix.ethereum.org/
Create a file named ERC721A.sol
Copy the contents of the ERC721A.sol file from the contracts folder

Create a file named Daivinity.sol
Copy the contents of the Daivinity.sol file from the contracts folder

## Compiling the contract
Open the Daivinity.sol file
Click on solidity compiler
Click on the compiler selector and select "0.8.0+commit..."
Click on "Advanced configuration" and select "Enable opimization" (200)
Click on "Compile Daivinity.sol"


## Deploying the contract
Click on  "Deploy and run transactions"
In the Contract section select "Daivinity"
In the expand the Deploy section and fill in the max batch size and collectionsize
The batchsize is the number of mints that can be done in one go
The collectionsize is the size of the collection

batchsize: 20
collectionsize: 2500

Click on "transact" and the contract will be deployed to the javascript vm

## Interacting with the contract
If the contract is deployed, it will show in the "Deployed contracts" section

Expand the contract.
You will see a function called allowlistMint. This is the mint function
Before adding the whitelist, the tokenURI needs to be set. This is something I can take care of if you want

The whitelist is called allowList. This can only be seeded by the owner of the contract eg you.

## Create the whitelist
The allowlist consists of a struct that holdds the addresses and number of nfts the address can mint. This number is usually 1 but can be more
Expand "seedAllowList"

Add the addresses as an array 
["0x5B38Da6a701c568545dCfcB03FcB875f56beddC4", "0x5B38Da6a701c568545dCfcB03FcB875f56beddC4", "0x5B38Da6a701c568545dCfcB03FcB875f56beddC4"]
Add the numslots as an array
[1, 1, 1]

## TODO
The video and metadata need to be pinned using pinata. I can take care of that if you want.
For 2500 nfts there will be 2500 metadata files 

Then the baseUri can be set

There is batch mint function yet that mints all nfts in one go
