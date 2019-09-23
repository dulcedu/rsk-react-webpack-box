# RSK React Webpack Box

## Description

In this box you'll find a basic starter pack. It includes Truffle, React and Webpack.
The the app was created with create-react-app and it can be customized with customize-cra.

This starter contains two main elements
- Truffle framework 
- React App (located at app/ folder)

## Unboxing

Run the unbox command

```bash
truffle unbox rsk-react-webpack-box
```

## Environment setup

### Description

This box comes with two environments
- Truffle environment (located at root folder)
- React environment (located at /app)

Each environment comes with a specific `package.json`, if you want to manage truffle `package.json` you simply run npm commands at root folder. For `app/package.json` you'll need to install and manage it with `yarn` package manager (because it's a create-react-app)

If you don't have `yarn` installed you can install it running 

```bash
npm install -g yarn
```

### Truffle Envirnoment setup

First ensure you are at the root folder and have truffle installed. 

If you don't have truffle installed you'll need to run this in order to install it.

```bash
npm install -g truffle
```

To install truffle dependencies 

```bash
# At project root folder (I.E '../resk-react-webpack-box/')
npm install
```

Now, the only thing you'll need to do it's to copy your mnemonic to truffle-config.js

```js
// truffle-config.json

const HDWalletProvider = require('truffle-hdwallet-provider');

//Put your mnemonic here, take care of this and don't deploy your mnemonic into production!
const mnemonic = 'A_MNEMONIC';
```

#### Using the truffle console

You can start a truffle console for any RSK network

```bash
# Console for Mainnet
truffle console --network mainnet

# Console forn Testnet
truffle console --network testnet
```

#### Migrating contracts

In order to migrate contracts to a specific network

```bash
# Migrate for Mainnet
truffle migrate --network mainnet

# Migrate for Testnet
truffle migrate --network testnet
```

### App environment setup

First install it's dependenices. Remember that you'll need to manage it with `yarn` package manager.

```bash
# At app folder (I.E '../resk-react-webpack-box/app')
yarn
```

Then you can run the app with

```bash
# At app folder (I.E '../resk-react-webpack-box/app')
yarn start
```

#### Comunicating with RSK network

[Web3 JS](https://web3js.readthedocs.io) and [ethereumjs-tx](https://github.com/ethereumjs/ethereumjs-tx) have been bundled for comunicating with RSK network.

#### Customizing create-react-app default options

This app uses [customize-cra](https://github.com/arackaf/customize-cra) in order to customize webpack, babel and all default `create-react-app` options. 

You can customize it at `app/config-overrides.js`.