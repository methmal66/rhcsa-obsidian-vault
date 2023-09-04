#linux 

What is the most common file encryption tool?::gpg (gnupg)
# Method1: Symmetric encryption

# Step1: Encrypting
How to encrypt a file using a passphrase
?
`gpg -c folder.tar.xz` then confirm a passphrase
![400](https://i.imgur.com/UkBj6wL.png)

# Step2: Decrypting 
How to decrypt a file using a passphrase on a different host
?
`gpg -d folder.tar.xz.gpg` then enter the passphrase
![400](https://i.imgur.com/j7SPA9l.png)

How to decrypt a file using a passphrase on the same host used to encrypt it
?
![400](https://i.imgur.com/QlTdPcX.png)

Why is it not safe to keep passphrase encrypted files in the same host used to encrypt it?::It can be decrypted without the passphrase when logged as the user who encrypted it

# Method2: Asymmetric encryption

# Step1: Generating keys
How to list the existing public keys?
?
`gpg --list-public-keys` 
![500](https://i.imgur.com/d1QtGq4.png)

How to generate a new key pair?
?
`gpg --full-gen-key` then follow the prompt to add options and parameters
