# Hardhat ERC-721/ERC-1155 Repo

* Clone this and run `npm i` in terminal.
* Add .env file with:
```
MNEMONIC=privatekey. not the seedphrase
MATIC_APP_ID=appid_from_maticvigil
POLYGONSCAN=apikey_from_polygonscan
```
* Edit the deploy script to pass in your name and ticker/uri depending on standard
* Edit the contractUri method in the contract and add your OpenSea collection URI 
* Edit the mint script and add your token uri, contract address and account address of the account you want to mint to.
* Deploy with `npx hardhat run --network matic scripts/deploy721.js` for ERC-721
* Mint with `npx hardhat run --network matic scripts/mint.js`

Contract code inspired from Opensea: https://github.com/ProjectOpenSea/meta-transactions/blob/main/contracts/ERC721MetaTransactionMaticSample.sol
This is for gas-less transactions when transferring assets. Users dont have to pay that extra gas, and get a better experience.

I added the mintItem method, from the old [truffle repo contract](https://github.com/YourNewEmpire/Truffle-Tutorial-ERC721).

I will make a blog post with detail soon.
