# Kadena CLI - User Feedback

## Installation

### Via npm

To install the Kadena CLI using npm/pnpm, run the following command:

```bash
npm  install  -g  @kadena/kadena-cli@0.0.1-alpha.5 or pnpm  install  -g  @kadena/kadena-cli@0.0.1-alpha.5
```


## Getting Started

After installation, you can access the full suite of Kadena CLI functionalities. The CLI provides a range of commands for different operations, such as managing wallets, accounts, and transactions, as well as creating dApps, (WIP: run your devnets / deploy / upgrade contracts ).

For a complete list of commands and their descriptions, please refer to the [Kadena CLI documentation](https://github.com/kadena-community/kadena.js/blob/main/packages/tools/kadena-cli/README.md).

### To initialise 

To initialise within your project, use the following command:

```bash
kadena config init
```



## User Feedback Program

### Objective

We are committed to making Kadena CLI the best tool it can be for developers. As part of this commitment, we are seeking feedback from our user community. This feedback will be invaluable in identifying areas for improvement, enhancing usability, and adding new features.

### How to Participate

Participation in the user feedback program involves completing specified scenarios using the Kadena CLI and documenting your experience. This process is structured around "Pair Programming Hour," where participants work in pairs, with one acting as the "driver" and the other as the "reporter."

#### Scenario Execution

Note: **we use chain 0 since the faucet there is not empty !!**

1.  **Pair Up**: We will form pairs consisting of a driver and a reporter and add them to a breakout room. (this session will take 30 minutes, and will automatically be ended)

2.  **Execute Scenario**: Finish all scenarios listed below.

    #### Scenarios:

    #### Scenario 1: Add a New Wallet and Fund an Account on Testnet

    **Description**: Create (add) new wallet using Kadena CLI, generate a key, create fund an account from this wallet using this key on the Kadena testnet (chain 0), and check the account's balance to confirm the transaction.


    #### Scenario 2: Transfer Funds from One Account to Another on Testnet

    **Description**: Use the Kadena CLI to transfer funds from one account to another by making a transaction using a transaction template (tx) within the CLI on the Kadena testnet. Verify the transaction by checking the balances of both the sender and receiver accounts.

    #### Scenario 3: Import a Wallet from Chainweaver and Check Balance

    ## **Legacy (Chainweaver) wallet for test usage:**

    #### Mnemonic Phrase:

    ##### script victory human funny onion ketchup tent record square custom snack lizard

    ***

    **Description**:
    Import a wallet that was previously exported from Chainweaver into the Kadena CLI.
    Once imported, check the balances of the key (5b46750a00e824891fa0a4f9cae1e31b85a19da7cfbf704224eb7649ca010e49) on index "5" to ensure successful import.
    **The balance should be 1 kda**.

    #### Scenario 4: Add an Account and Drain a Funded Account Using a Template

    **Description**: Using a wallet imported from Chainweaver, add a new account through the Kadena CLI. Then, use a predefined transaction template from [Kadena's transaction library](https://github.com/kadena-io/txlib/blob/master/drain.ktpl) (store to project folder) to drain funds from a funded account into the newly created account.

4.  **Document Your Experience**: As you go through the scenario, the reporter should note any difficulties encountered, areas for improvement, and overall feedback.

#### Feedback Submission

- **Format**: Feedback should be structured according to the provided template (see below).

- **Where to Submit**: Feedback should be submitted to the `/round-one/feedback` folder in this repository. Please create a new file for your feedback report and follow the naming convention `feedback_<scenario_name>_<date>(_user1_user2_or when anonymous leave empty).md`.

### Feedback Template

```markdown
# Kadena CLI Feedback

## Scenario

[Name of the scenario]

## Participants

Driver: [Driver's Name]

Reporter: [Reporter's Name]

## Expectations

[What did you expect to happen before starting the scenario?]

## Outcome

[Did the driver successfully complete the scenario?]

[Was it complex to execute]

[Did you have any prior knowledge about Kadena blockchain interactions]

## Challenges

[Describe any difficulties faced during the scenario. Please be as explicit as possible]

## Additional Feedback

[Any other feedback or suggestions for improvement.]

## Errors

[Did you encounter any errors, please provide the error or stacktrace if any given]

## Reflection

[Was the outcome as expected? Reflect on any differences between your expectations and the actual outcome.]
```

## Conclusion

Your contributions and feedback are crucial to the continuous improvement of the Kadena CLI. We thank you for your participation and look forward to making Kadena CLI an even more powerful tool for developers.

---

## Why did do we do this:

This template is designed to be comprehensive, guiding users from installation to participation in the feedback program. It aims to foster a collaborative environment where the community can actively contribute to the development and refinement of the Kadena CLI.
