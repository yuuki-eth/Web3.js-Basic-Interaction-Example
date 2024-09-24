# Web3.js-Basic-Interaction-Example
Web3.js Basic Interaction Example
Introduction
Welcome to the Web3.js Basic Interaction Example! This repository serves as a starting point for developers looking to interact with the Ethereum blockchain using the web3.js library. Web3.js is a powerful JavaScript library that allows you to communicate with the Ethereum network, manage accounts, and interact with smart contracts.

Prerequisites
Before you begin, ensure you have the following installed:

Node.js (version 12 or higher)
npm (Node package manager)
Getting Started
1. Initialize npm
If you haven't already, initialize npm in your project directory:

npm init -y
2. Install Dependencies
Install the necessary dependencies:

npm install web3 command-line-args node-rest-client-promise
3. Set Up Infura
To connect to the Ethereum network, you will need an Infura project ID. Sign up at Infura and create a new project to get your API key.

4. Create a Script
Create a new JavaScript file, e.g., web3-contract-basic-interaction.js, and add the following code:

const Web3 = require('web3');
const fs = require('fs');

// Load Infura token from a local file
const infuraToken = fs.readFileSync('/path/to/your/infura_token').toString().trim();
const infuraHost = `https://mainnet.infura.io/v3/${infuraToken}`;

const web3 = new Web3(infuraHost);

// Example: Get the current protocol version
web3.eth.getProtocolVersion()
    .then(protocolVersion => {
        console.log(`Protocol Version: ${protocolVersion}`);
    })
    .catch(error => {
        console.error(`Error fetching protocol version: ${error}`);
    });
5. Run the Script
Execute your script using Node.js:

node web3-contract-basic-interaction.js
6. Review the Output
You should see the current Ethereum protocol version printed in the console.

Conclusion
This example demonstrates how to set up a basic interaction with the Ethereum blockchain using web3.js. From here, you can expand your project to include more complex interactions, such as sending transactions or interacting with smart contracts.
