# SSH

Using the [SSH protocol](https://es.wikipedia.org/wiki/Secure_Shell), you can connect and authenticate to remote servers and services.

## Check for existing SSH keys

```shell
$ ls -al ~/.ssh
# Lists the files in your .ssh directory, if they exist
```

By default, the filenames of the public keys are one of the following:

* id_dsa.pub
* id_ecdsa.pub
* id_ed25519.pub
* id_rsa.pub

## Generate a new SSH key

```shell
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

This creates a new ssh key, using the provided email as a label.

```shell
> Generating public/private rsa key pair.
```

When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.

```shell
> Enter a file in which to save the key (/home/you/.ssh/id_rsa): [Press enter]
```

At the prompt, type a secure passphrase:

```shell
> Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again]
```

> If you leave passphrase empty and press Enter, you will create a new SSH key without passphrase.