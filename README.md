## Running a Full Node
This tutorial will go over the basics of spinning up a Bitcore node. Before you begin, you'll need to have around 8GB of memory and about 200GB of disk space available to store the Bitcoin blockchain plus additional database information. Both 64bit Mac OS X and GNU/Linux are currently supported. The process of downloading the blocks and indexing can take upwards of 24 hours on livenet and 2 hours for testnet, depending on Internet connection and other factors such as CPU and disk speed. It's also possible to use an existing Bitcoin data directory, which will speed up the process as reindexing can take upwards of 12 hours for livenet and 1 hour for testnet.

## Install Node.js v4 LTS

It's recommended to install the Node Version Manager, as this makes it simple to switch between different Node.js versions. We will specifically need to install and run v0.12 or v4 LTS. Please follow the directions at https://github.com/creationix/nvm#install-script and then run:

```
nvm install v4
```

## Install ZeroMQ and Tools

For GNU/Linux distribution such as Debian or Ubuntu:

```
apt-get install libzmq3-dev build-essential
```

For Mac OS X:

```
brew install zeromq
```

## Install Bitcore

Bitcore comes with a command line utility for creating and managing your full node. To get started, run these commands, and you'll then have the bitcore command in your path:

```
git clone https://github.com/tealcoin-project/tealcoin-explorer-fullnode.git && tealcoin-explorer-fullnode
npm install
npm start
```

## Configure the Network

Your node can run on "livenet" or "testnet". If you wish to configure the network, you can do so by opening the  litecore-tealcoin-node.json configuration file with your favorite text editor (vi is used here):

```
cd tealcoin-explorer-fullnode
vi litecore-tealcoin-node.json
```
Then change the network value to "testnet" or "livenet". Here is an example configuration file:

```
{
  "network": "testnet", // livenet or testnet
  "port": 3001,
  "services": [
    "bitcoind",
    "insight-tealcoin-api",
    "insight-tealcoin-ui",
    "web"
  ],
  "servicesConfig": {
    "bitcoind": {
      "spawn": {
        "datadir": "./data",
        "exec": "./node_modules/.bin/tealcoind"
      }
    }
  }
}
```

## Test to open in your browser

Go to the local URL (default):

```
http://localhost:3001/insight/
```

<img src="https://bitcore.io/images/guides/full-node/insight.d1fa5ecc.png">
