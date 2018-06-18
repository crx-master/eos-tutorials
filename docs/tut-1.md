![stability-wip](https://img.shields.io/badge/stability-work_in_progress-lightgrey.svg)

# Install and configure a wallet software

For a regular user to interact with *EOS blockchain*, it's interesting to use a *wallet software*. Doing so, you can *sign a transaction* and publish it to the blockchain without exposing your *private key*.

On the other hand, you will have to trust your private key to the chosen wallet software and in it's storage. That's why hardware wallets have great success with several other cyptocurrencies and, at this point, we all hope that soon we will have a good hardware wallet compatible with EOS.

So, for this purpose, always use an auditable open source code software, and always check the origin of your download. 

For this tutorials, we chose to use *[Scatter](https://github.com/EOSEssentials/Scatter)*, a browser extension that works with Google Chrome or Firefox.

## 1. Install Scatter

On a machine with Google Chrome installed, add Scatter extension from [chrome web store](https://chrome.google.com/webstore/detail/scatter/ammjpmhgckkpcamddpolhchgomcojkle).

## 2. Password

Click on the new chrome toolbar icon

![Scatter initial screen](img/tut-01-scatter-ini.png)

Create and confirm a very strong password to protect the Scatter local data storage. Use **at least 12** lower and uppercase letters, numbers **and** special characters. Click on "Create New Scatter" button. This example uses a really long the password `xC4Km*zAn$as8!!v$fRHqcDxumW2u#QP`;

## 3. Mnemonic phrase

Scatter now creates a cryptographic seed and shows you a mnemonic phrase. Write it down carefully, **every one of the twelve words in the very same order**. As this is not clear on the user interface, the correct order is:

```
cotton city sadness fame critic lake quality rain rich guess symptom load
```

![Scatter mnemonic 12 words](img/tut-01-scatter-mnemonic.png)

Those words give Scatter the capacity to regenerate the cryptographic seed and will cover you up if you forget your password. **But, very important**, differently from other wallets implementations from other blockchains, you **cannot** recover your entire Scatter just using the mnemonic phrase. In the case you loose Scatter data (ex.: a hard drive wipe or loosing your entire laptop), you will really need **a backup file** (wich we will cover soon) **AND one of the two: 1) your password OR 2) your mnemonic phrase**.

If you create a new Scatter from zero with the same password, it will give you the same mnemonic.

If you change your password, Scatter will change your mnemonic phrase.

Now **read Scatter disclaimer** and then click at "**Skip Basic Setup**", as our objective is to create and test a backup file!

![Scatter welcome](img/tut-01-scatter-welcome.png)

## 4. Backup

At this point you really already know how important is to keep you private key **private**, so let's create our first key pair! As a matter of fact, you create only a random private key, as the public key mathmatically generated from it.

Differently from Bitcoin and other blockchains *[deterministic wallets](https://en.bitcoin.it/wiki/Deterministic_wallet)*, Scatter will create a totally random private key that has nothing to do with your password or mnemonic phrase. So click in the "Key Pairs" link of the current screen and then, on the screen of the next image, do the following:
  - (1) Give a cool name to your new key pair;
  - (2) Click in "Generate Key Pair";
  - (3) Click in "Copy" (only if you want to save your private key elsewhere);
  - (4) Click in "Save".   

![Scatter welcome](img/tut-01-scatter-new-key-pair.png)  

In this example, Scatter created the following Private + Public Keys:

```
Private Key: 5K4PEv5RJcA7LtFaHCqZpajTQbasEXKWH8692RaQMCC1YxTBGtF
Public Key: EOS6vmtbSxZM4oDgpTxzVV62U1hHj1ZEyzhVJuvCMAzA8KZq6g3CA
```

If you clicked in the "Copy" button before saving your new key pair, you now have your private key ready to paste on a secure file. Only do this if you **really** need the private key outside of Scatter context. This copy procedure increases your exposure to malware and other kind of attacks.

Now that you have your new private key stored inside Scatter, do the following:  
  - (1) click on the cog icon on upper right corner;
  - (2) click on "Backup";
  - (3) now you can use your password **or** mnemonic phrase, but **be sure to inform your password** as a test of assertiveness.  

If you done it all correctly, Scatter exported a [JSON](https://www.json.org/) backup file with encrypted contents of your wallet, including your newly created private key: 

```
{
  "iv": "bR1YRST4XCcgRgGE4U43QA==",
  "salt": "oA5C7S5H0q8=",
  "ct": "VRlhr6Uzjdl4MjB4aq6PGgtlhxDcW8jdEQEuz7cFX2qh7A...22ioWQv7OzzQv9h2H4VuojwLQounTEAOWYk="
}
```

If Scatter rejects your password, for security reasons, you will have to wipe this installation and start it all over again from step 1.

Right after creating a new key par or identity, is highly recommended that you create a new backup file and test it again. **Do not overwrite or delete your old backup files**! You will probably need old backups if something goes wrong from now on.

Keep at least **two copies** of your backup files stored safely, **outside your current computer**. Ask yourself if that files could be somehow lost and what would be the consequences if you loose your Scatter install.

## 5. Destroy Scatter data

We have to trust the process, so now we will now destroy the Scatter data and restore it from the backup file. That way, we will rest assured to be able to operate securely with the recently generated Key Pair.

  - (1) click on the cog icon on upper right corner;
  - (2) click on "Destroy";
  - (3) now you can use your password **or** mnemonic phrase, but **be sure to inform your mnemonic phrase** as a test of assertiveness.

> You are about to destroy your entire Scatter keychain. The **only way** to get this exact Scatter back is by **importing an exported Scatter JSON**. You will not be able to claim your identities otherwise. Make sure you have exported your Scatter from the backup settings panel before hand.

  - (4) click "Destroy Scatter" if you feel ready! :) 

If Scatter rejects your mnemonic phrase, for security reasons, you will have to start it all over again from step 1.

Scatter will say it's locked even if it is not. Just unlock it and try again closing the warning window if necessary.

## 5. Test your backup file

At this point, Scatter will be asking again for a password to create a new install.

- (1) Click on "Load from Backup" this time;

> Importing your encrypted keychain file will rebuild you Scatter keychain, but it will not import your old networks or accounts.

- (2) Open your JSON backup file with a text editor and copy it's contents; 
- (3) Paste the contents on the "Paste your Backup" text box;
- (4) Now that you **already tested both**, you can use your **password or mnemonic phrase**.

![Scatter welcome](img/tut-01-scatter-load-backup.png)  

## 7. Ready to go live!

Check your key pairs. (NOT THERE... WORK IN PROGRESS)