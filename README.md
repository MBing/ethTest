# Ethereum APP

## Using Geth to run this baby
Your data directory must be empty so your genesis file must not be in there!

## Setup Tools
- [Geth](https://github.com/ethereum/go-ethereum/wiki/geth)

### Commands
```
	$ geth --datadir=./chaindata/ init genesis.json
	$ geth --datadir=./chaindata/
```
*TIP* When running the commands you will see a path being printed to the location of your `geth.ipc` file. You will need this later to connect to Mist.

## Other Tools
- [EthereumJS TestRPC](https://github.com/ethereumjs/testrpc)
- [MetaMask - Chrome Extension](https://metamask.io/)
- [Mist](https://github.com/ethereum/mist)
- [Mist Download Page - Only Installer, wallet is NOT necessary!](https://github.com/ethereum/mist/releases)

## Connect Mist to your VPN
- Skip all steps of installation wizard on startup. (Not necessary here)
- We need the Geth Node (which is running in background once the app starts)
- First we need to run our Commands (This creates the Private Network & thus the `geth.ipc` file)

**MAC OS X**

To open the Mist App you need to connect to geth through the IPC file. (See Tip above - *Commands* section) 
Run this command:
```
	$ /Applications/Mist.app/Contents/MacOS/Mist --rpc <path to chaindata>/geth.ipc
```

This makes sure you will open Mist with the right connection. If not then Mist will create its own connection.
When you are running your Private Network and try to run Mist without this connection, you will get an error.
Make sure to follow the steps and you are using the right Geth node for the connection to your Private Network.

Once connected, the Mist app will start and you can click `Launch Application`.

