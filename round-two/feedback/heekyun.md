# Kadena CLI Feedback

Driver: Hee Kyun

Reporter: Hee Kyun

## **Scenario 1: Add and Fund Accounts on Testnet**

**Expectations**

[What did you expect to happen before starting the scenario?]
Get to know how `kadena` command works, and how it interacts with the blockchain

**Outcome**


[Did the driver successfully complete the scenario?]
At first try, no. I have created 0 testnet account, and 1 mainnet account instead of 2 testnet accounts.

I assumed `kadena config init` would create an account on testnet, and then I created a second account using `kadena account create`.
The result was `kadena config init` did not create an account on testnet. (I don't think it was created on mainnet either. It was only added to account list in the cli tool)
`kadena account create` created a new account on mainnet. The command asked for an account name, and because it was similar to the process that `kadena config init` asked when asking for a wallet name, I assumed that it would be used within the tool, and I put a name, `user-test-1`, but this was the name that was added as the `coin` account. Also, `kadena account create` asked for a public key, and so I used `pact -g` locally to create a new public key to be used for my second account.

At second try, I tried to create the account with the wallet created from `kadena config init`, with the command,
`kadena account add-from-wallet` and failed with the error message,

```
The account configuration "/Users/heekyun/Kadena/kadena-cli-user-test/.kadena/accounts/user-test.yaml" already exists.
```
At third try, I set default network to `testnet` with

```
kadena network set-default --network="testnet"
```
and then ran

```
kadena account create
```

but it also created the account on mainnet. The docs indicated that `create` is for mainnet, but I assumed that changing config would let me run it on testnet. Also, `create` command did not have any information about the networks, so I wasn't sure which network the command would execute on.

[Was it complex to execute]

Yes, I think the mix of account names and wallet names could be confusing to people. It could be better to unify them into `k:` accounts, and have advanced configs to create `non-k:` accounts. Only supporting principal accounts can be nicer.

[Did you have any prior knowledge about Kadena blockchain interactions]
Yes

**Challenges**

[Describe any difficulties faced during the scenario. Please be as explicit as
possible]

**Additional Feedback**

[Any other feedback or suggestions for improvement.]
I’d like a bigger warning text for the necessity to backup the mnemonic phrase.
Other improvements I would ask are more consistencies in the command questions. For example, `kadena account fund` asks for the network I'd like to run them on. `kadena wallet add`, which I assume is built to create account on the blockchain, did not ask for network, as well as `kadena account create`

**Errors**

[Did you encounter any errors, please provide the error or stacktrace if any
given]

`kadena wallet add` does not create an account on blockchain even though I selected "yes" on `Create an account using the first wallet key?`.
Same behavior with `kadena config init`, which also creates a new wallet.
Because of missing this step, the next command, `kadena account fund` fails. And `kadena account create` only works with mainnet

**Reflection**

[Was the outcome as expected? Reflect on any differences between your
expectations and the actual outcome.]
No, some behaviors blocked me from getting the outcomes I expected. I have described on the `Errors` section.

## **Scenario 2: Generate Keys from a Wallet**

**Expectations**
Generate and list keys from mneumonic phrases.
**Outcome**
Generated and listed keys from mneumonic phrases.
**Challenges**
N/A
**Additional Feedback**
Worked well, and displayed nicely!
**Errors**
N/A
**Reflection**
If alias was not asked, I wouldn't want to decide any more thing that I wouldn't remember. It could default to `wallet-name-{index}`. I would recommend not asking alias as default, and have optional flag for alias.

## **Scenario 3: Transfer Funds on Testnet**

**Expectations**
Have simple ways to transfer funds
**Outcome**
I did not find the template from `./.kadena` directory. Instead, I found `./accounts`, `./defaults`, `./networks`, `./wallets`
**Challenges**
The question ` Template key "key:from" matches account "account:from". Use public account's
key?`
this wasn't clear to me. Instead of `use`, it could ask with `sign`? or, if it finds an `k:` account, it could default to the key in the account.
The options I had to choose from:
```
❯ Enter public key manually
  Pick a public key from another account
  Pick a public key from keys
```
also didn't provide an easy `default` option. I have to remember where in my wallets, the account key is stored, and pick the key to sign with, when transferring a `k:` account, which I think can be simplified.
**Additional Feedback**
I'd rather want to find `transfer` as a command instead of a template, because these are basic functions that everyone would need to interact with at some point.
**Errors**
I failed to create/fund accounts from scenario 1, so I only succeeded up to `tx test`.
`tx test` seems to ask `chainId` and `network`, but they are already in the transaction file, and doesn't seem to be applied. I think this step can be removed.

**Reflection**
I would have hoped one stop command to do `tx add`-`tx sign`-`tx test`-`tx send`.

## **Scenario 4: Change Wallet Password and Generate Keys**

**Expectations**
Change wallet password and generate keys
**Outcome**
Changed wallet password and generated keys
**Challenges**
N/A
**Additional Feedback**
Worked well!
**Errors**
N/A
**Reflection**

## **Scenario 5: Import a Wallet from Chainweaver and Check Balance**

**Expectations**
Import chainweaver wallet and recover its keys
**Outcome**
I was able to recover chainweaver wallet.
I was able to generate keys with chainweaver wallets.
I was able to run add-from-wallet and add account
I was able to check balance through `kadena account details`

**Challenges**
- The process was not so simple.
- When selecting the public key in `add-from-wallet` command, the ui showed the list of keys without indexes. With more than 10 keys, it's hard to find which key I'm searching for without indexes, so showing index along with the key would be nice.

**Additional Feedback**
On `kadena wallet add` command, the sequence is
```
wallet name?
wallet password?
```
but on `import`, the sequence was
```
wallet password?
wallet name?
```
I'd prefer to type in wallet name before password when importing, as well.
**Errors**
The example command was `kadena wallet import-wallet`, but the actual command was `kadena wallet import`.
**Reflection**

## **Scenario 6: Delete an Account**

**Expectations**
Delete the accounts that are stored in the wallet.
**Outcome**
I was able to delete the accounts that are stored in account lists.
**Challenges**
N/A
**Additional Feedback**
N/A
**Errors**
N/A
**Reflection**
N/A

## **Scenario 7: Generate Random Keys**

**Expectations**
Have easy ways to generate random keys
**Outcome**
I was able to generate random keys with simple command
**Challenges**
How to interact with the keys in the wallet? I can add
**Additional Feedback**
I've tried running `kadena key generate` several times with the same alias's. When executed in the same amount, the key generation is blocked. But for example when 2 keys were already generated, then the command with `amount=3` generates 1 key, with message that `{alias}-1`, `{alias}-2` already exists. Instead, it would be better to block using the same alias, for minimal confusion
**Errors**
N/A
**Reflection**
Having both `kadena key generate`, and `kadena wallet generate-key` was a bit confusing. One suggestion would be, merge `key` and `wallet` with `wallet`, and distinguish the `mnemonic-based` wallets, and `keyPair-based` wallets?
