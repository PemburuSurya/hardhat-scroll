# hardhat-scroll

Hardhat plugin for Arbitrum Developers.

## Features

ArbitrumScan Contract Verification

## Prerequisites

Before the installation steps you need to have your hardhat project initialized using the command

```bash
npx hardhat init
```

Make sure to have dependencies installed!

## Installation

Use the following command to install

```bash
npm i hardhat-scroll --save-dev
```

Import the plugin in your `hardhat.config.js`:

```js
require("hardhat-scroll");
```

Or if you are using TypeScript, in your `hardhat.config.ts`:

```ts
import "hardhat-scroll";
```

Remove / Comment the import for `@nomicfoundation/hardhat-toolbox`

Add the following configuration to the `config` object in `hardhat.config.js`.

```js
networks: {
        scrollGoerli: {
            // can be replaced with the RPC url of your choice.
            url: "https://scroll-testnet-public.unifra.io",
            accounts: [
                "<YOUR_PRIVATE_KEY>"
            ],
        },
        scrollOne: {
            url: "https://rpc.scroll.io	",
            accounts: [
                "<YOUR_PRIVATE_KEY>"
            ],
        }
    },
    etherscan: {
        apiKey: {
            scrollGoerli: "<OPTIMISMSCAN_API_KEY>",
            scrollOne: "<OPTIMISMSCAN_API_KEY>"
        },
    },
```

Verify your contracts using the following command (Make sure your contracts are compiled before verification)

Arbitrum Goerli Testnet

```bash
npx hardhat verify <CONTRACT_ADDRESS> <CONSTRUCTOR_ARGS> --network scrollGoerli
```

Arbitrum Mainnet

```bash
npx hardhat verify <CONTRACT_ADDRESS> <CONSTRUCTOR_ARGS> --network scrollOne
```
# hardhat-scroll
# hardhat-scroll
