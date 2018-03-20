# EthereumBlockchainConnection

## ETHEREUM ##

In this guide, we will go through the following steps:

* Download and install latest version of Ethereum GO implementation. This will provide us the geth CLI.
* Connect to an Ethereum net, namely Homestead.

Next section explodes these steps. The expected result is to get the Homested blockchain locally. 

### Setting up geth and Homestead ###

[This guide](https://gist.github.com/cryptogoth/10a98e8078cfd69f7ca892ddbdcf26bc "connect to rinkeby") (for linux and mac) include steps which show how to install Go and geth, connect to a ethereum network, and use a client to open a (local) intercative connection to inspect blockchain, wallets, and accounts. 

To make things work for Homestead (guide shows how to connect to an unofficial testnetwork) we had to make some fix to the guide:

* Follow step 1 entirely
* In step 2, change:
~~~~
    geth --rinkeby
~~~~
to
~~~~
    geth --datadir=$HOME/.homestead 
~~~~
* In step 3, change:
~~~~
    geth --datadir=$HOME/.rinkeby attach ipc:$HOME/.rinkeby/geth.ipc console
~~~~
to
~~~~
    geth attach ipc:$HOME/.homestead/geth.ipc
~~~~

### Getting formatted information from the nodes ###

TODO
