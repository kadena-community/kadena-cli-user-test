# Kadena CLI Feedback

Driver: Jermaine Jong

Reporter: Jermaine Jong

## **Config init:

**Challenges**
I was a bit unsure what the following means, how can I provide a password file?

```
You can use the --password-file flag to provide a password.
```

## **Scenario 1: Add and Fund Accounts on Testnet**

**Expectations**
My first expectation was to go to "kadena account create" to create a new account. But that prompted me for a public key which I didn't have.

Then I Aborted and went to "kadena account add-from-wallet" since I already had a wallet from the config init.
This then allowed me to create a new account (a new account was added in .kadena/accounts) but I could only select the public key that was already there. So now I ended up with two accounts with the same public key.

**Outcome**
With some help I learned that I had to go to "kadena wallet generate-keys" to generate a new keypair and then use that public key to create a new account. After that I was able to fund both account and check the balance on testnet

**Challenges**
It was challenging to understand the relationship between the wallet and the account, especially from a user's perspective that starts to develop on Kadena. Once you relate it to concepts you already know from experience by building on Kadena it's easier to understand what is meant here.


## **Scenario 2: Generate Keys from a Wallet**

**Expectations**
Since this had to be done in step 1 I was already familiar with this step.

**Outcome**
I was able to list and generate keys from a wallet without any problems.

**Additional Feedback**
When generating the keys I was prompted for the amount of keys, I entered 2. In the next step I was asked for an alias, I wasn't able to enter an alias for the second key so both keys now have the same alias.


## **Scenario 3: Transfer Funds on Testnet**

**Expectations**
Couldn't find the built in template. I was looking for it in the repo and then I went into the docs and started copying the transfer example from there.  After some help I found out that the template was contained in the CLI already by doing "kadena tx add" and that you could select it after.

**Outcome**
I managed to do all steps easily. The tx menu is pretty clear. It was nice that after checking status there was a suggestion to use the "--poll" flag

**Additional Feedback**
When using "kadena tx status" a prompt is made for chain-id, which isn't necessary imo. Don't know why that is needed but it saves an extra step if you can omit it.

**Errors**
I was trying to transfer 2 KDA but I got the following error:
```
Decimal value must be in the format "123.456"
```
I would have expected to enter 2 and then the CLI would automatically convert it to 2.00


## **Scenario 4: Change Wallet Password and Generate Keys**

**Outcome**
No remarks, everything went as expected. I managed to change the password and generate new keys using the new password.


## **Scenario 5: Import a Wallet from Chainweaver and Check Balance**

**Outcome**
Importing the wallet went without issues.
Because of the previous steps I was already familiar with generating keys and adding accounts.

**Challenges**
When adding accounts you have to manually count to get to the 5th key in the list. It would be nice if the keys were numbered so you could just go the number of the key you want to use.


## **Scenario 6: Delete an Account**

**Outcome**
No feedback, everything went as expected.


## **Scenario 7: Generate Random Keys**

**Outcome**
Generation and listing of random keys went without issues.

**Additional Feedback**
The keys are stored in the working directory, which means they live outside of the context of the cli. If i travel to another directory I can't access the keys anymore. This might be confusing for users, especially because the rest of the cli is all based on the .kadena directory.
