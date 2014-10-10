BitIodine
=========

With [BitIodine](https://bitiodine.net) you can find connecting paths between two Bitcoin addresses, visualize clusters controlled by the same user or entity, and get insights about activity on the network.

![BitIodine building blocks](http://miki.it/images/bitiodine_design.png)

More info at: http://miki.it/articles/papers/#bitiodine.

Dependencies
-------------

On Ubuntu:

```bash
sudo apt-get install -y libssl-dev cmake build-essential g++-4.4 libdb++-dev libboost-all-dev libsparsehash-dev git-core perl sqlite3 python3-numpy python3-simplejson python3-networkx libhiredis-dev libsqlite3-dev
```

bitcoind
--------
```
sudo aptitude install python-software-properties
sudo add-apt-repository ppa:bitcoin/bitcoin
sudo aptitude update
sudo aptitude install bitcoind
mkdir ~/.bitcoin/

# Edit an empty ~/.bitcoin/bitcoin.conf file in the .bitcoin folder:
nano ~/.bitcoin/bitcoin.conf

# Insert the following code in the new bitcoin.conf file:
server=1
daemon=1
rpcuser=INVENT_A_UNIQUE_USERNAME
rpcpassword=INVENT_A_UNIQUE_PASSWORD
txindex=1

# start bitcoind
bitcoind

# The blockchain is now loading

# To view the status of the download:
bitcoind getinfo

# For more information
bitcoind help
