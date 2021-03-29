# Infura x Truffle Laboratory

This is a box that ideally gets you set up with the basic scaffolding that gives you the ability to add your own logic without having to worry about the nuts and bolts. You'll need to do a few things on your end but this should get you up and going with project that uses React + Truffle + Infura which can deploy to the rinkeby testnet ( you can of course re- configure this to deploy to another desired network).

## STACK

### TRUFFLE

link: https://www.trufflesuite.com/

### INFURA

link: https://infura.io/

Go ahead and sign up for a new account if you don't have one already

### REACT

link : https://reactjs.org/docs/getting-started.html

## Make sure you've installed

#### yarn

Firsly this requires you have yarn installed
(On the chance you don't you can find out more about it in the link below)

[https://classic.yarnpkg.com/en/docs/install/#mac-stable]

`npm install --global yarn`

Next up we will be using Wallet-enabled Web3 provider. Use it to sign transactions for addresses derived from a 12 or 24 word mnemonic.

#### HD Wallet-provider

LINK https://github.com/trufflesuite/truffle/tree/master/packages/hdwallet-provider#readme

##### We are going to use version 1.2.2 for our hdwalletprovider in this box

`npm install @truffle/hdwallet-provider@1.2.2`

#### Ganache

The GUI or CLI both work, use whichever you're more comfortable with

GUI download found here: [https://www.trufflesuite.com/ganache]

Command to install the CLI

`yarn global add ganache-cli`

#### Mnemonic Generator

if you need one here is a link
[https://iancoleman.io/bip39/]

(select 12)

# Instructions on how to use this box:

### Step 1: We will start by running the command

`yarn`

![ScreenShot](./src/assets/yarn.gif)

### Step 2: Next get Ganache up and running

navigate to the folder back-end

`cd back-end`

Now that your in the folder holding our truffle.config (along with other files) You can start Ganache

you can do this with the GUI or CLI (be sure your on port: 8545)

if using the CLI go ahaed and run the command

`ganache-cli`

you should now see in your terminal
![ScreenShot](./src/assets/CLI.png)

Open up another tab to work out of while keeping the CLI up and running

### Step 3: Define your wallet

Next we will want to define the wallet we will be using to deploy

`truffle console`

`const HDWalletProvider = require('@truffle/hdwallet-provider');`

`const mnemonic = '12 words here';`

`const wallet = new HDWalletProvider(mnemonic, "http://localhost:8545");`

`wallet`

![ScreenShot](./src/assets/wallet.png)
