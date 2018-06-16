# SSH Explained
---

Secure shell protocol that encrypts a connection between client and host
i.e. Github to local laptop.

## The ssh command
The command:
```bash
$ ssh {user}@{host}
```
Linux and Mac can access ssh from the terminal
Windows requires an ssh client like putty

## ssh on Github
- ssh-add ~/.ssh/id_rsa on the folder you want to add the key to

## how ssh works
3 techniques are used in ssh:
- symmetrical encryption
  - uses a key that turns input into gibberish and as long as the receiver
    has the same key it can be decrypted.
  - anyone that has the key can decrypt the message
  - this relies on a key exchange algorithm,
- Asymmetrical encryption
  - uses two separate keys for encryption and decryption
- Hashing
  - runs through a function that spits out gibberish with no way to get back to the original.
  - hmax is used to get back to the origin
  - uses a symetric key which is known by both client and host

## ssh-keygen generate public->private keypair
- The command:
```bash
ssh-keygen -C "test@gmail.com"
```
- -C -> Comment: Provides a new Comment

## Share a Public key
