# Blockchain Homework

## Create Nodes

1.- Create empty directories for 2 nodes

2.- Get the new accounts numbers from nodes to use them later as signers

    ./geth account new --datadir node1
    ./geth account new --datadir node2

3.- Save the passwords and account addresses in a .txt file in you local machine (important for later steps)

4.- Create 2 password.txt files inside each node directory and store the assigned passwords

    echo 'password' > node1/password.txt
    echo 'password' > node1/password.txt
    echo '48028193fF1D8F52241073466cF766E2E9274ae6' >> accounts.txt
    echo '5A55468eef595490268eb889B6cf9B2e07e4b58C' >> accounts.txt

5.- Run puppeth

    ./puppeth

6.- Initialize nodes

    ./geth init homeworknet.json --datadir node1
    ./geth init homeworknet.json --datadir node2

7.- Start up a mining thread for node 1

    ./geth --datadir node1/ --mine --miner.threads 1 --unlock '48028193fF1D8F52241073466cF766E2E9274ae6' --password node1/password.txt --rpc --allow-insecure-unlock

8.- Open a new terminal and navigate to the Blockchain-Tools folder

    cd OneDrive
    cd Desktop
    cd Blockchain-Tools

9.- Start mining node 2

    ./geth --datadir node2 --unlock "A55468eef595490268eb889B6cf9B2e07e4b58C" --mine --port 30304 --bootnodes enode://3ab60e400193220d49731ea3264ef4f7378742049f3a48b0fbc5731bb4e7a72462cacb0fba0d5b7c4185b158eb504720d94e7c143362fa609daff7d643243b3e@127.0.0.1:30303 --ipcdisable


## MyCrypto

1.- Open MyCrypto

2.- Click on "Add Custom Node" and fill out the fields based on your network information

  3.- Go back to the main menu and import the keystore file from your folder directory into MyCrypto
  
  4.- Make a transaction (remember to specify the address and the transaction amount)
  
  5.- Confirm transaction and click 'Send'
  
  6.- Copy the hash string in a .txt file (this string will be required to cehck for the transaction status)
  
  7.- Select the TX Status from the left-side menu
  
  8.- Paste the hash string or select the most recent transaction made
  
  9.- Click 'Check TX Status'

**Please refer to the 'Screenshots' folder for command lines and for a visual guidance for each of the steps.**
