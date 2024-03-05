# Kadena CLI Feedback

## Scenario

Scenario 1

## Participants

Driver: Steven

Reporter: Sam

## Expectations

stright forward cli with feedback on failure

## Outcome

[Did the driver successfully complete the scenario?] No

[Was it complex to execute] It was not complex, just not stright forward feedback or indications

[Did you have any prior knowledge about Kadena blockchain interactions] Not for either on the cli

## Challenges

Error decription not being too meaningful (decryption failed)

## Additional Feedback

-key generation, example is not clear (default is 0 and suggestion 1-5) and explanation is not either
-we tried 2 times as password "test123", we got the feedback for length and kept repeating it till it worked with a short pw
-When generating the keys it should say "enter wallet password" since we could not make it work with a different password

## Errors

when generating a key we got decryption failed, using index: 0, action: generate public key (also with public and private) | alias: steven1 | randompassword
This was because it was mentioning "a" password (last feedback point)
