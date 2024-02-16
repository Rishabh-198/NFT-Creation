# Create your own NFT

## What are NFT's ??
Non-fungible tokens (NFTs) are unique digital assets verified using blockchain technology, representing ownership of digital or physical items such as art, music, videos, and virtual real estate. Each NFT possesses distinct properties, enabling verifiable ownership and facilitating trading on various online platforms, transforming digital ownership paradigms.

First, creators mint NFTs by tokenizing digital or physical assets using blockchain technology, often through specialized platforms like Ethereum's ERC-721 standard. Metadata describing the asset's uniqueness and ownership details are attached. Once minted, NFTs are distributed and traded on online marketplaces, where buyers can purchase and own them securely, facilitated by smart contracts that govern transactions and ensure authenticity.

## About the project
In this project I have deployed a Smart contract over **Sepolia** test netowrk for minitng of your own NFT. This project leverages the use of **Pinata** cloud system. You can pass the pinata gateway link of your assset in file  `nft-metadata.json`. After successful minintg you will get NFT format of your assest.

## Requirements
- Hardhat
- Node.js
- Ether.js
- Metamask
- dotenv module
- Alchemy API
## Steps to mint your own NFT

- Upload your asset to pinata cloud.
- Save the gateway link in `nft-metadata.json` in `image` key.
- Create a .env file in project directory.
- Save your public address and private address where you want to mint your NFT.
- Set the API URL from Alchemy.
- Refer to this image for synatx: ![Syntax of .env file](https://github.com/Rishabh-198/NFT-Creation/blob/main/env%20sample.jpg)
- Open terminal and execute : `npx hardhat compile`
- After successful compilation run: `npx hardhat run scripts/deploy.js --network sepolia`
- This will provide you with deployement adddress.
- Copy and paste this address in `contractAddress` variable in `mint-nft.js` file.
- Now we can mint our NFT: `node scripts/mint-nft.js`
- This will give you hashcode of your transaction.
- Search for this hashcode in [https://sepolia.etherscan.io/](https://sepolia.etherscan.io/)
- Copy interaction id and tokenID.
- In your Metamask wallet paste these ID's in `import NFT` button.

### Your NFT for that asset is imported in your wallet. You can now transfer it or lists it in any NFT marketplace.
 
> [!NOTE]
> You must have some Sepolia token before deploying the smart contract.
> 
> You can import the NFT only in the accoutn from which you minted it.
