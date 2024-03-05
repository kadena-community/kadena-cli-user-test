# Kadena CLI Feedback

## Scenario

Add a New Wallet and Fund an Account on Testnet
Add a Second Account (as far as we got)

## Participants

Driver: Nil

Reporter: Travis & Randy

## Expectations

I wanted to create a wallet.
I wanted to generate keys
I wanted to create account
I wanted to fund an account
I wanted to create a second account

## Outcome

- Create wallet - success
- Generate keys - success
- Create account - success
- Fund account - success
- Create second account - some confusion arised

## Challenges

Scenario 1:

- Enter a password to verify with password -> should be re-enter password to verify
- On key creation:
  - better delineations of pub key / private key?
    - seems like the space is what splits the two, but maybe make it clearer?
  - also note really clear where that test-key.key file lives -> make it easier to find / access?

Scenario 2:

- When creating the second account, would be nice to be able to generate keys as part of account creation step
  - Had to create account, asked for key to use
  - Then created new key, then link the two after
  - kadena account add-from-wallet (first time) v. kadena account create (second time)
- When creating keys, would be great to have a functionality to copy private key without exposing it in terminal
  - also may want to obfuscate more -> there's a lot of the private key exposed
- When generating a new key inside the same wallet, it created a key-pair with the same public key but a different private key
- Also unclear / unsure if the private keys are stored in the same test-key.key file, or separate files

- In this step we slowed down due to some confusion: we were trying to create an account within the same wallet

## Additional Feedback

[Any other feedback or suggestions for improvement.]

## Errors

[Did you encounter any errors, please provide the error or stacktrace if any given]

## Reflection

[Was the outcome as expected? Reflect on any differences between your expectations and the actual outcome.]
