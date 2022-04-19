# Truffle-Tutorial-ERC721
### Repo for deploying and minting NFTs for opensea with truffle and ipfs
### Visit https://dev.to/yournewempire/deploy-nfts-with-truffle-ipfs-opensea-polygon-5581 for detailed tutorial
### Prerequisite programming in node.js would be beneficial.

# Getting started 
Clone this repo. 
Run `npm install` in terminal.
Place Matic RPC node key and Wallet Mnemonic in new .env file
Upload some nft metadata to an api. I used IPFS.
Place link to NFT Collection.json in contractURI method, under GameItem.sol. 
Deploy the contracts with `truffle develop` then `migrate --network mumbai` in the terminal, then copy the contract address.
Add your account address, contract address and token json link to the mint script.
Enter `node scripts/mint.js` into the console to mint.


This is inspired by opensea's tutorial: https://github.com/ProjectOpenSea/opensea-creatures and https://docs.openzeppelin.com/contracts/4.x/erc721
and is supposed to be an expanded version (with ipfs and solidity at a higher version). With that, I shall explain what is going on clearly in the future blog post. 

Once again, huge credit to opensea, ethereum infrastructure, and ipfs for making it all possible for me to build on and learn with.
```
$ truffle migrate

Compiling your contracts...
===========================
✓ Fetching solc version list from solc-bin. Attempt #1
✓ Fetching solc version list from solc-bin. Attempt #1
> Everything is up to date, there is nothing to compile.


Starting migrations...
======================
> Network name:    'development'
> Network id:      12191
> Block gas limit: 60000000 (0x3938700)


1_initial_migration.js
======================

   Deploying 'Migrations'
   ----------------------
   > transaction hash:    0x63d87d95fc34e8f42f73363bf3586221621aaa025e3d737ebaf96bed32b26589
   > Blocks: 0            Seconds: 0
   > contract address:    0x2823caf546C7d09a4832bd1da14f2C6b6E665e05
   > block number:        705738
   > block timestamp:     1650367164
   > account:             0x6Be02d1d3665660d22FF9624b7BE0551ee1Ac91b
   > balance:             7408.571490183397
   > gas used:            250154 (0x3d12a)
   > gas price:           0.0000045 gwei
   > value sent:          0 ETH
   > total cost:          0.000000001125693 ETH

   > Saving migration to chain.
   > Saving artifacts
   -------------------------------------
   > Total cost:     0.000000001125693 ETH


2_deploy_token.js
=================

   Deploying 'GameItem'
   --------------------
   > transaction hash:    0xd58b0044b7340a918129541610ab68759eb317b4f1caebb3f2cb996cc981d09c
   > Blocks: 0            Seconds: 4
   > contract address:    0x1a3fa978909d86dF1244216b02733136b438D83E
   > block number:        705740
   > block timestamp:     1650367176
   > account:             0x6Be02d1d3665660d22FF9624b7BE0551ee1Ac91b
   > balance:             7408.558682836897
   > gas used:            2800164 (0x2aba24)
   > gas price:           0.0000045 gwei
   > value sent:          0 ETH
   > total cost:          0.000000012600738 ETH

   > Saving migration to chain.
   > Saving artifacts
   -------------------------------------
   > Total cost:     0.000000012600738 ETH

Summary
=======
> Total deployments:   2
> Final cost:          0.000000013726431 ETH
```
