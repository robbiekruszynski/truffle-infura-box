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

![ScreenShot](./src/assets/yarn.gif)

Next up we will be using Wallet-enabled Web3 provider. Use it to sign transactions for addresses derived from a 12 or 24 word mnemonic.

#### HD Wallet-provider

LINK https://github.com/trufflesuite/truffle/tree/master/packages/hdwallet-provider#readme

## We are going to use version 1.2.2 for our hdwalletprovider in this box

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

#Instructions on how to use this box:

The first thing you'll want to do is get Ganache up and running
you can do this with the GUI or CLI (be sure your on port: 8545)

if using the CLI go ahaed and run the command

`ganache-cli`

you should now see in your terminal
(IMG)

`truffle console`

`const HDWalletProvider = require('@truffle/hdwallet-provider');`

`const mnemonic = '12 words here';`

`const wallet = new HDWalletProvider(mnemonic, "http://localhost:8545");`

`wallet`
