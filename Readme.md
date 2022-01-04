# Proof of Authority Bloockchain

For this chain, pretending to be a new developer at a small bank called smbank you were assigned a mission to set up a private testnet blockchain. 

The testnet is setup in order to avoid risk as there is no real money involved and it allows for offline development using;
 * Puppeth, to generate your genesis block.


 * Geth, a command-line tool, to create keys, initialize nodes, and connect the nodes together.


 * The Clique Proof of Authority algorithm.

## Setting up a blockchain

1.  Creat accounts for two nodes using separate datadir using geth for the network.

2.  Generate a geneisis block
  * To generate a genesis block, run puppeth, name your network (in this scenario smbank), and select the option to configure a new genesis block.
  * Choose the clique (Proof of Authority) consensus algorithm.
  * Paste both account addresses from step 1 at a time into the lists of accounts to seal ( make sure to remove 0X infront of the account adresses).
  * Then paste thesame addresses in the list of accounts to prefund. And because they are no blowck rewards in POA, you'll need to pre-fund.
  * Complete the rest of the prompts (hitting enter). Once back at the main menu choose the " Manage existing Genesis" option.
  * To finalize generating your block genesis, export configurations. This will faill to create two of the files, but only one is needed "smbank.json".

3. After completing the genesis block creation, we will initialize the nodes with the genesis' json file (smbank).

4. Nodes can be used to begin mining blocks.
  * Nodes should be run in different terminal windows with the commands.
  
  **NOTE:** Type your password and hit enter even if you can not see it visually.

5. Your private PoA blockchain should now be running.

6. Now that both nodes are up and running , the blockchain can be added to MyCrypto for testing.
   * Open Mycrypto app, then navigate to the "change network option" at the bottom left.
   * Click "Add Custom Node", then add the custom network information that you set in the genesis.
   * Make sure that you scroll down to choose Custom in the "Network" column to reveal more options like Chain ID:
   * Type ETH in the Currency box.
   * In the Chain ID box, type the chain id you generated during genesis creation.
   * In the URL box type: http://127.0.0.1:8545.  This points to the default RPC port on your local machine.
   * Finally, click Save & Use Custom Node.

7. After connecting to the custom network in MyCrypto, it can be tested by sending money between accounts.
   * Select the View & Send option from the left menu pane, then click Keystore file.
   * On the next screen, click Select Wallet File, then navigate to the keystore directory inside your Node1 directory, select the file located there, provide your password when prompted and then click Unlock.
   * This will open your account wallet inside MyCrypto.
   * In the To Address box, type the account address from Node2, then fill in an arbitrary amount of ETH and confirm the transaction by clicking "Send Transaction", and the "send" button. 
   * Click the Check TX Status when the green message pops up, confirm the logout.
   * You should see the transaction go from Pending to Successful in around the same blocktime you set in the genesis.
   * Now  click the Check TX Status button to update the status.

## 'Felicitation' you have successfully sent a transaction on your private Blockchain






