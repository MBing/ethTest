# Ethereum APP

## Using Geth to run this baby
Your data directory must be empty so your genesis file must not be in there!

## Setup Tools
- [Geth](https://github.com/ethereum/go-ethereum/wiki/geth)

### Commands
Go into the folder and run these commands to start your own Private Network.
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
- [Remix IDE](http://remix.ethereum.org/)

## Connect Mist to your VPN
- Skip all steps of installation wizard on startup. (Not necessary here)
- We need the Geth Node (which is running in background once the app starts)
- First we need to run our Commands (This creates the Private Network & thus the `geth.ipc` file)

**MAC OS X**

To open the Mist App you need to connect to geth through the IPC file. (See Tip above - *Commands* section) 
Run this command:
```
	$ /Applications/Mist.app/Contents/MacOS/Mist --rpc <path/to/geth.ipc>
```

This makes sure you will open Mist with the right connection. If not then Mist will create its own connection.
When you are running your Private Network and try to run Mist without this connection, you will get an error.
Make sure to follow the steps and you are using the right Geth node for the connection to your Private Network.

**WINDOWS**

- Open Mist application
- Skip Installation Wizard (we don't need to set this up)
- Ready

Once connected, the Mist app will start and you can click `Launch Application`.
First create an account, this is a Private Network, so don't worry about the password. 
When going online, please use a very secure password!

## Run Geth
Now we have 1 terminal open that ran our Commands, another where we had to run our Mist application (Mac OS X) 
and now we need to run our Geth console in another terminal. Open a terminal window and use the following command:
```
	$ geth attach ipc:<path/to/geth.ipc>
```

## Start/Stop Mining (Geth Console)

When you are done with Commands, Mist & Geth Console is running, use the following commands for mining Ethers:
```
	$ miner.start(1);
	$ miner.stop();
	$ exit
```

Now you should see your Mist wallet getting updated with Ethers.

Enjoy!
