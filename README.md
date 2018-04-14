Running a Full Node
This tutorial will go over the basics of spinning up a Bitcore node. Before you begin, you'll need to have around 8GB of memory and about 200GB of disk space available to store the Bitcoin blockchain plus additional database information. Both 64bit Mac OS X and GNU/Linux are currently supported. The process of downloading the blocks and indexing can take upwards of 24 hours on livenet and 2 hours for testnet, depending on Internet connection and other factors such as CPU and disk speed. It's also possible to use an existing Bitcoin data directory, which will speed up the process as reindexing can take upwards of 12 hours for livenet and 1 hour for testnet.

Install Node.js v4 LTS

It's recommended to install the Node Version Manager, as this makes it simple to switch between different Node.js versions. We will specifically need to install and run v0.12 or v4 LTS. Please follow the directions at https://github.com/creationix/nvm#install-script and then run:

```
nvm install v4
```

Install ZeroMQ and Tools

For GNU/Linux distribution such as Debian or Ubuntu:

```
apt-get install libzmq3-dev build-essential
```

For Mac OS X:

```
brew install zeromq
```

Install Bitcore

Bitcore comes with a command line utility for creating and managing your full node. To get started, run these commands, and you'll then have the bitcore command in your path:

```
git clone 
```

