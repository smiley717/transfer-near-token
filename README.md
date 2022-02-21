Constructing transactions on NEAR
===

This repository serves to demonstrate how transactions are created, signed, and sent to the NEAR blockchain.
Users are able to send `NEAR` token to any users with private key.

## Prerequisites:

- Current version of [Node.js](https://nodejs.org/). >=v14.0.0

### Install NEAR-CLI
```bash
npm i -g near-cli
```

### How to get private key from the seed phrase
```bash
near generate-key --seedPhrase 'special style height timber defense leave vote behave elbow scare gallery side'
```

## Setup:

1) Setup an environment variable `SENDER_PRIVATE_KEY` with the private key of the sender's account.

Either create a `.env` file in the root of this project, or export a bash variable by running the following in your terminal (replacing the example key).

```bash
export SENDER_PRIVATE_KEY=
```

2) Install dependencies by running:
```bash
yarn
```

## Examples:

### Send Tokens (High Level)
>[`send-tokens-easy.js`](./send-tokens-easy.js) will show you the easiest (JavaScript) way to send NEAR tokens (Ⓝ) using a [`near-api-js`](https://github.com/near/near-api-js) method; `account.sendMoney()`

1) In `send-tokens-easy.js`, update:
  - account IDs for `sender` and `receiver`.
  - network ID (`default` is `testnet`)

2) Run the file and send those tokens!

```bash
node send-tokens-easy.js
```

### Send Tokens (Low Level)
>[`send-tokens-deconstructed.js`](./send-tokens-deconstructed.js) completely dissects the transaction construction process and shows the lowest level way to send NEAR tokens (Ⓝ).

1) In `send-tokens-deconstructed.js`, update:
  - account IDs for `sender` and `receiver`.
  - network ID (`testnet` is default)
2) Enter the amount of Ⓝ you would like to send.
3) Run the file and send those tokens!
  
```bash
node send-tokens-deconstructed.js
```

For a detailed walk-through, see the [create-transactions](https://docs.near.org/docs/tutorials/create-transactions) doc.

Happy coding! 🚀 
