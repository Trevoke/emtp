# Encrypted Mail Transfer Protocol

## Why?

People who do not respect the openness of the internet are meddling.

Or maybe you're paranoid.

Or maybe you just want encryption, just because. Whatever.

## Version 0.1, very high level, naive


1. Things like GPG allow you to create a private key and password-protect it. This makes me feel a litle better about some of the following ideas.
2. The message needs to be encrypted and stored; I'm willing to accept that we store the information in plain-text in RAM, that is, we decrypt it. If you save a draft, it should be encrypted. If you want to edit it, it would be decrypted first.
3. This goes to the next idea: in your mailbox, everything, whether sent or received, is encrypted.
4. When you create an account, it generates a public/private key for you, then the public key, tied to your email address, is stored on the mail server.
5. When you send an email to someone, through communication with the server, it automatically retrieves the person's public key, then encrypts the message and sends it, of course, with SSL.
6. When you receive the email, all you need is your private key to decrypt it, so if you have logged in and have chosen to ssh-agent the key, or whatever, you don't need to retype your password.


How does this sound from a crazy-high-level view?

