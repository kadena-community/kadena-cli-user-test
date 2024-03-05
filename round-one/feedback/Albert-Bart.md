# Kadena CLI Feedback

## Scenario

Add a New Wallet and Fund an Account on Testnet

## Participants

Driver: Albert

Reporter: Bart

## Outcome

Yes mostly

## Challenges

Got the error when adding an account from-wallet that the wallet had no keys yet.

Trouble finding where templates are, and adding a new one or modifying an existing one.

## Additional Feedback

- "enter a password" should be "enter the password for the wallet" (missing context)
- searching "balance" in readme has no results
- fund should give explorer link and request-key
- should have a "kadena tx status" command for a request-key
- details only works for one network/chain
- send should do local calls first to find errors
- should be easier to add custom templates
- sign can still scan for which wallet to sign with and ask that wallet's password
- order of some prompts is off. "sign" should ask transaction first.
- when using "account import" add some discovery to find existing keys
- don't show mnemonic in "executed:" like password.
- import should be the full flow including making keys and accounts
