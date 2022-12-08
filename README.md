# Modified Hashlips Minting-Dapp

By Fazel Pejmanfar & Web3Chick and compatible with ERC721A. I have only made some UI changes and added Web3 Modal.

This repo provides a nice and easy way for linking an existing NFT smart contract to this minting dapp. There are two ways of using this repo, you can go the simple route or the more complex one.

The simple route is so simple, all you need to do is download the build folder on the release page and change the configuration to fit your needs. (Follow the video for a walk through).

The more complex route allows you to add additional functionality if you are comfortable with coding in react.js.

## Changes by Fazel 🛠️

<b> Fixed the BigNumber Issue</b> <br>
<b> Added Social icons</b> <br>
<b> Added Story (About) </b> <br>
<b> Added FAQ</b> <br>
<b> Added Auto Network Switch</b> <br>
 Will be adding Merkle Tree whitelist soon...


 # HashLips NFT minting dapp (Edits By Web3Chick)
<b> Added Web3 Modal (Wallet Connect) </b> <br>
<b> Made optional UI changes to the minting section</b> <br>
<b> Added a new Font</b> <br>
<b> Added support for Goerli as Rinkeby is now deprecated</b> <br>

Credits to Karmelo & Flappy

## Installation 🛠️

If you are cloning the project then run this first, otherwise you can download the source code on the release page and skip this step.

```sh
git clone https://github.com/web3chick/Minting-Dapp.git

Make sure you have node.js installed so you can use npm, then run:

```sh
npm install
```
Afterwards you need to install the walletconnect dependencies via npm:

```sh
yarn add @walletconnect/web3-provider
```
```sh

npm install walletconnect --save
npm install web3-provider --save
npm install web3modal --save 
npm install walletlink --save 

```

Make sure to update the Network IDs and RPCs in blockchainActions.js to your choice network.

to run development Server

```sh
npm run start
```

to Build the File

```sh
npm run build
```

## Usage ℹ️

In order to make use of this dapp, all you need to do is change the configurations to point to your smart contract as well as update the images and theme file.

For the most part all the changes will be in the `public` folder.

To link up your existing smart contract, go to the `public/config/config.json` file and update the following fields to fit your smart contract, network and marketplace details. The cost should be in Ether.

Note: this dapp is designed to work with the intended NFT smart contract, that only takes one parameter in the mint function "tokens". But you can change that in the App.js file if you need to use a smart contract that takes 2 params.

Change your Social url in `public/config/config.json` <br>
<b> Price Should be in Ether </b> <br>
to edit about and faq q/a edit `src/App.js` <br>
to change Carousel Images for SneakPeak Replace images in `public/config/images`  <br>

```json
{
   "CONTRACT_ADDRESS": "0x38f4e5eca904e01faa7a23e8956cf9af48c6b666",
  "SCAN_LINK": "https://goerli.etherscan.io/address/0x38f4e5eca904e01faa7a23e8956cf9af48c6b666",
  "NETWORK": {
    "NAME": "Goerli",
    "SYMBOL": "ETH",
    "ID": 5
  },
  "NFT_NAME": "Web3Chick",
  "SYMBOL": "W3C",
  "MAX_SUPPLY": 200,
  "DISPLAY_COST": 0.01,
  "GAS_LIMIT": 145000,
  "MAX_PER_TX": 2,
  "MARKETPLACE": "Opeansea",
  "MARKETPLACE_LINK": "#",
  "Telegram": "#",
  "Discord": "#",
  "Twitter": "#",
  "SHOW_BACKGROUND": false
}


```

Make sure you copy the contract ABI from remix and paste it in the `public/config/abi.json` file.
(follow the youtube video if you struggle with this part).

Now you will need to create and change images in the `public/config/images` folder.

Next change the theme colors to your liking in the `public/config/theme.css` file.

```css
:root {
  --primary: #ABDBE3;
  --primary-text: rgb(56, 55, 55);
  --secondary: rgb(56, 55, 55);
  --secondary-text: rgb(56, 55, 55);
  --accent: rgb(56, 55, 55);
  --accent-text: rgb(56, 55, 55);
}
```

Now you will need to create and change the Favicons in `public/images` to your brand images.

Remember to update the title and description the `public/index.html` file

```html
<title>Web3Chick Dapp</title>
<meta name="description" content="Mint your W3C NFT" />
```

Also remember to update the short_name and name fields in the `public/manifest.json` file

```json
{
  "short_name": "Web3Chick",
  "name": "Web3Chick"
}
```

After all the changes you can run.

```sh
npm run start
```

Or create the build if you are ready to deploy.

```sh
npm run build
```

Now you can host the contents of the build folder on a server.

That's it! you're done.
#
