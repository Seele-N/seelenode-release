# seelenode-release
seele node mainnet Beta binary


Prepare your machine
To run Seele mainnet Beta nodes, you will need a machine with the following minimum requirements:

4-core, x86_64/ARM architecture processor;

16 GB RAM;

1 TB of storage space.

#Step 1. Get the Seele mainnet Beta binary


Step 2. Configure seele
#Step 2-0 (Optional) Clean up the old blockchain data

./seeled unsafe-reset-all

Step 2-1 Initialize seele

 $ ./seeled init [moniker] --chain-id=seelehub_186-1 [--home=]
 This moniker will be the displayed id of your node when connected to Seele Chain network.
 [--home=] set the path to store blockchain data.
 
./seeled init "sync-wallet" --chain-id=seelehub_186-1 --home=/data/seele

Step 2-2 Configure seele

replace files of config folder 
Download and replace the Seele Mainnet Beta genesis.json

Download and replace the Seele Mainnet Beta app.toml
Download and replace the Seele Mainnet Beta client.json
Download and replace the Seele Mainnet Beta config.json

change config.json moniker as you set before
moniker = "sync-wallet"

Step 2-2 Run seele

./seeled start --home=/data/seele


Step 3. docker (Optional)

build docker image with dockerfile
docker build -t seele:latest .

run docker with docker-compose 
docker-compose up -d
