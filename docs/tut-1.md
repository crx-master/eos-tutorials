# Install and configure a wallet software

For a regular user to interact with EOS blockchain, it's interesting to use a wallet software. Doing
so, you can sign a transaction and publish it to the blockchain without exposing your private key.

On the other hand, you will have to trust your pk to the chosen wallet software and it's process of storing it. That's why hardware wallets do a lot of success with several other cyptocurrencies and at this point we all hope some project get a good hardware wallet compatible with EOS as soon as possible.

So, for this purpose, always use an auditable open source code software, and always check the origin of your download. 

For this tutorials, we chose to use [Scatter](https://github.com/EOSEssentials/Scatter), a browser extension that works with Google Chrome or Firefox.

# Steps

1. On a machine with Google Chrome installed, add Scatter extension from [chrome web store](https://chrome.google.com/webstore/detail/scatter/ammjpmhgckkpcamddpolhchgomcojkle)

2. Click on the new chrome toolbar icon  
![Scatter initial screen](img/tut-01-scatter-ini.png)

3. Create and confirm a very strong password to protect the Scatter local data storage. Use **at least 12** lower and uppercase letters, numbers **and** special characters. Click on "Create New Scatter" button;

4. Write down securely the **12 words** that compose your backup.  
![Scatter initial screen](img/tut-01-scatter-mnemonic.png)  
Those 12 words will give you access to the cryptographic seed that Scatter have just created. This
will be life saving in the case you loose your password or if you loose the installation data (ex.: 
a hard drive wipe with no backup or loosing your entire laptop);

5. Import the private key of your EOS account to Scatter.