# Kadena CLI - User Feedback (Round 2)

## Installation

### Via npm

To install the Kadena CLI using npm/pnpm, run the following command:

```bash
npm install -g @kadena/kadena-cli@1.0.0-rc.2
```

or

```bash
pnpm install -g @kadena/kadena-cli@1.0.0-rc.2
```

## Getting Started

After installation, you can access the full suite of Kadena CLI functionalities. The CLI provides a range of commands for different operations, such as managing wallets, accounts, and transactions, as well as creating dApps, (PLANNED: run your devnets / deploy / upgrade contracts).

For a complete list of commands and their descriptions, please refer to the [Kadena CLI documentation](https://github.com/kadena-community/kadena.js/blob/main/packages/tools/kadena-cli/README.md).

### Clone

Clone this repository in order to be able to push your feedback form to the feedback folder.

```bash
git clone https://github.com/kadena-community/kadena-cli-user-test.git
```

### To initialise

To initialise within your project, use the following command:

```bash
kadena config init
```

Running config init, creates a account, a wallet, and your first key, see docs for more info:

```
https://github.com/kadena-community/kadena.js/tree/main/packages/tools/kadena-cli#kadena-config
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

3.  **Write down Feedback**: The reporter will document the experience, including any challenges faced, areas for improvement, and overall feedback (Optionally you can use the [template below](#feedback-template)).

---

### **Scenarios for Testing Using Kadena CLI on Testnet**

#### **Scenario 1: Add and Fund Accounts on Testnet**

**Objective**: Utilize the Kadena CLI to create and fund **two accounts** on the Testnet. Note that the `config init` command typically creates an initial account. If `config init` has been used, only one additional account needs to be created. If `config init` has not been used, the steps should be repeated to create the second account.

**Steps**:

1. **Add an Account**: Create a new account using the Kadena CLI, if less than two accounts exist.
2. **Fund the Account**: Send funds to this account on chain 0.
3. **Check Balance**: Verify the account balance to confirm the transaction.
4. **Repeat for Second Account (if necessary)**: If only one account exists after using `config init` or if no initial account was created, repeat the above steps to ensure a total of two accounts are set up.

[More details on the `account` command](https://github.com/kadena-community/kadena.js/tree/main/packages/tools/kadena-cli#kadena-account)

---

#### **Scenario 2: Generate Keys from a Wallet**

**Objective**: Generate keys from a wallet using the Kadena CLI.

**Steps**:

1. **Generate Keys**: If no wallet exists, create one first, then generate keys.
2. **List Keys**: Display the available keys.

[More details on the `wallet` command](https://github.com/kadena-community/kadena.js/tree/main/packages/tools/kadena-cli#kadena-wallet)

---

#### **Scenario 3: Transfer Funds on Testnet**

**Objective**: Perform a fund transfer between two accounts using the Kadena CLI.

**Steps**:

1. **Add Transaction**: Select and use the transfer template.
2. **Sign Transaction**: Authenticate the transaction.
3. **Test Transaction**: Verify the transaction functionality.
4. **Send Transaction**: Execute the transfer.
5. **Check Transaction Status**: Monitor the status of the transaction and confirm the balances of both sender and receiver accounts.

[More details on the `tx` command](https://github.com/kadena-community/kadena.js/tree/main/packages/tools/kadena-cli#kadena-tx)

---

#### **Scenario 4: Change Wallet Password and Generate Keys**

**Objective**: Update the password of a wallet and generate keys using the new security credentials.

**Steps**:

1. **Change Password**: Update the password for an existing wallet.
2. **Generate Keys**: Use the new password to generate keys.

---

#### **Scenario 5: Import a Wallet from Chainweaver and Check Balance**

**Objective**: Import a wallet from Chainweaver using the Kadena CLI and check the key balance.

**Legacy Wallet Details**:

- **Mnemonic Phrase**: "script victory human funny onion ketchup tent record square custom snack lizard"

**Steps**:

1. **Import Wallet**: Use the `--legacy` flag to import the wallet.
2. **Check Balance**: Confirm the balance for the key index "5". Expected balance: 1 KDA.

---

#### **Scenario 6: Delete an Account**

**Objective**: Remove an existing account using the Kadena CLI.

**Steps**:

1. **Delete Account**: Permanently remove the selected account.
2. **List Accounts**: Display the remaining accounts to confirm deletion.

---

#### **Scenario 7: Generate Random Keys**

**Objective**: Create random keys using the Kadena CLI that are not associated with any wallet.

**Steps**:

1. **Generate Keys**: Produce random keys.
2. **List Keys**: Display all generated keys.

[More details on the `key` command](https://github.com/kadena-community/kadena.js/tree/main/packages/tools/kadena-cli#kadena-key)

---

3.  **Document Your Experience**: As you go through the scenario, the reporter should note any difficulties encountered, areas for improvement, and overall feedback.

#### Feedback Submission

- **Format**: Feedback should be structured according to the provided template (see below).

- **Where to Submit**: Feedback should be pushed to the `/round-two/feedback` folder in this repository. Please create a new file for your feedback report and follow the naming convention `feedback_<scenario_name>_<date>(_user1_user2_or when anonymous leave empty).md`.

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
