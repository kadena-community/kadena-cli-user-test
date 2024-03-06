# Kadena CLI Feedback

## Scenario

### Scenario 1

Add a New Wallet and Fund an Account on Testnet

Create (add) new wallet using Kadena CLI, generate a key, create fund an account from this wallet using this key on the Kadena testnet (chain 0), and check the account's balance to confirm the transaction.

### Scenario 2

Transfer Funds from One Account to Another on Testnet

Use the Kadena CLI to transfer funds from one account to another by making a transaction using a transaction template (tx) within the CLI on the Kadena testnet. Verify the transaction by checking the balances of both the sender and receiver accounts.

## Participants

Driver: Eileen

Reporter: Sander

## Expectations

[What did you expect to happen before starting the scenario?]

## Outcome

[Did the driver successfully complete the scenario?]

- No, kept getting errors (see "Errors").

[Was it complex to execute]

- No, not per se. Password setting unclear; why do we need it? Missing info.

[Did you have any prior knowledge about Kadena blockchain interactions]

- Yes

## Challenges

[Describe any difficulties faced during the scenario. Please be as explicit as possible]

## Additional Feedback

- What is the purpose of previous password?
- What does indices matter (for key creation)?

Instruction not very clear, which type of key to generate

"Enter a password" -> Enter "the/your" password?

kadena account create -> create on mainnet (?!)

[Any other feedback or suggestions for improvement.]

Feedback

- Not sure what to report
- Took a while to get to the documentation
- Expected some examples in the README

## Errors

### Error - Scenario 1

[Did you encounter any errors, please provide the error or stacktrace if any given]

❯ kadena account fund
? Select an account:(alias - account name) cli-test-account      - k:e82656....115d0f3f
? Enter an amount. 100
? Select a network testnet
? Enter ChainId (0-19) 0
✖ Failed
Single-key account protocol violation

Executed:
kadena account fund --account="cli-test-account" --amount="100" --network="testnet" --chain-id="0"

## Reflection

[Was the outcome as expected? Reflect on any differences between your expectations and the actual outcome.]
