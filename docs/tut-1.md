# Install and configure a wallet software

For a regular user to interact with EOS blockchain, it's interesting to use a wallet software. Doing
so, you can sign a transaction and publish it to the blockchain without exposing your private key.

On the other hand, you will have to trust your pk to the chosen wallet software and it's process of storing it. That's why hardware wallets do a lot of success with several other cyptocurrencies and at this point we all hope some project get a good hardware wallet compatible with EOS as soon as possible.

So, for this purpose, always use an auditable open source code software, and always check the origin of your download. 

For this tutorials, we chose to use [Scatter](https://github.com/EOSEssentials/Scatter), a browser extension that works with Google Chrome or Firefox.

## 1. Install Scatter
On a machine with Google Chrome installed, add Scatter extension from [chrome web store](https://chrome.google.com/webstore/detail/scatter/ammjpmhgckkpcamddpolhchgomcojkle)

## 2. Password
Click on the new chrome toolbar icon  
![Scatter initial screen](img/tut-01-scatter-ini.png)

Create and confirm a very strong password to protect the Scatter local data storage. Use **at least 12** lower and uppercase letters, numbers **and** special characters. Click on "Create New Scatter" button. This example uses a really long the password `xC4Km*zAn$as8!!v$fRHqcDxumW2u#QP`;

## 3. Mnemonic phrase
Scatter now creates a cryptographic seed and shows you a mnemonic phrase. Write it down carefully, **every one of the twelve words in the very same order** (line by line).

![Scatter mnemonic 12 words](img/tut-01-scatter-mnemonic.png)

Those words give Scatter the capacity to regenerate the cryptographic seed and will cover you up if you forget your password. **But, very important**, differently from other wallets implementations from other blockchains, you **cannot** recover your entire Scatter just using the mnemonic phrase. In the case you loose Scatter data (ex.: a hard drive wipe or loosing your entire laptop), you will really need **a backup file** (wich we will cover soon) **AND one of the two: 1) your password OR 2) your mnemonic phrase**.

If you create a new Scatter from zero with the same password, it will give you the same mnemonic.

If you change your password, Scatter will change your mnemonic phrase.

## 4. Backup and test

Now read Scatter disclaimer and then click in "**Skip Basic Setup**", as our objective is to create and test a backup file!  
![Scatter welcome](img/tut-01-scatter-welcome.png)

At this point you really already know how important is to keep you private key **private**, so let's create our first key pair! As a matter of fact, you create only a random private key, as the public key mathmatically generated from it.

Differently from Bitcoin and other blockchains *[deterministic wallets](https://en.bitcoin.it/wiki/Deterministic_wallet)* Scatter will create a totally random private key that has nothing to do with your password or mnemonic phrase. So click in the "Key Pairs" link of the current screen and then, on the screen of the next image, do the following:
  - Give a cool name to your new key pair;
  - Click in "Generate";
  - Click in "Copy" (if you want to save your private key elsewhere);
  - Click in "Save".   

![Scatter welcome](img/tut-01-scatter-new-key-pair.png)  

In this example, scatter created:

```
Private Key: 5K4PEv5RJcA7LtFaHCqZpajTQbasEXKWH8692RaQMCC1YxTBGtF
Public Key: EOS6vmtbSxZM4oDgpTxzVV62U1hHj1ZEyzhVJuvCMAzA8KZq6g3CA
```

If you clicked in the copy button before saving, paste the information on a secure file.

Now that you have your new private key stored in Scatter, do the following:  
  - click on the cog icon on upper right corner;
  - click on "Backup";
  - now you can use your password or mnemonic phrase, but be sure to inform your password as a test of assertiveness.  

If you done it all correctly, Scatter will export a [JSON](https://www.json.org/) backup file with encrypted contents of your    wallet, including the newly created private key. If you cannot input your password, you will have to wipe this installation and start all over again for security reasons.

```
{
  "iv": "bR1YRST4XCcgRgGE4U43QA==",
  "salt": "oA5C7S5H0q8=",
  "ct": "VRlhr6Uzjdl4MjB4aq6PGgtlhxDcW8jdEQEuz7cFX2qh7A...22ioWQv7OzzQv9h2H4VuojwLQounTEAOWYk="
}
```