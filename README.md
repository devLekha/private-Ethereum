# private-Ethereum
How to create private Ethereum blockchain

Create Private Ethereum Blockchain:

C:>cd E:

Create a new folder and name it. Eg. "PB".

E:> geth --datadir "E:\PB\private" account new

Give the passphrase.
Then repeat the passphrase.
You will get the address {address}.

Inside this(Here PB) folder write the genesis.json file.

Now initialize the genesis block using the following command:

E:>geth --datadir "E:\PB\private" init "E:\PB\genesis.json"

The above command needs to be run only ones.Now to open the geth console use the following command:

E:> geth --networkid  123456 --datadir "E:\PB\private" --rpc --rpcaddr "0.0.0.0" --rpcport "8545" --rpcapi "web3,net,eth,admin,personal" --rpccorsdomain "*" console

So here, private ethereum  blockchain is created. We can connect this private blockchain to Remix IDE as well and deploy our Smart contract to test it. To exit the private network simply type: 

>exit

