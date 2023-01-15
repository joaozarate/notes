## Installing Git

Link: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

```shell
sudo apt install git
git config --global user.name "Joao Zarate"
git config --global user.email joaozarate@gmail.com
```

##### Git config path: ~/.gitconfig
https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup


## Connecting to GitHub with SSH

Link: https://docs.github.com/en/authentication/connecting-to-github-with-ssh
Link: https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/github-clone-with-ssh-keys

```shell
ssh-keygen -t ed25519 -C "your_email@example.com"
```


## Commands

```shell
git clone git@github.com:joaozarate/studies.git
```


## Signed Commits

https://docs.github.com/en/enterprise-server@3.3/authentication/managing-commit-signature-verification

Command to list the long form of the GPG keys for which you have both a public and private key.
```shell
gpg --list-secret-keys --keyid-format=long
```

If you are on version 2.1.17 or greater, paste the text below to generate a GPG key pair.
```shell
gpg --full-generate-key
```

Your key must be at least `4096` bits.

When asked to enter your email address, ensure that you enter the verified email address for your GitHub account.

Use the `gpg --list-secret-keys --keyid-format=long` command to list the long form of the GPG keys for which you have both a public and private key.

From the list of GPG keys, copy the long form of the GPG key ID you'd like to use. In this example, the GPG key ID is `3AA5C34371567BD2`:

```shell
$ gpg --list-secret-keys --keyid-format=long
/Users/hubot/.gnupg/secring.gpg
------------------------------------
sec   4096R/3AA5C34371567BD2 2016-03-10 [expires: 2017-03-10]
uid                          Hubot <hubot@example.com>
ssb   4096R/4BB6D45482678BE3 2016-03-10
```


```shell
gpg --armor --export 3AA5C34371567BD2
```

Copy your GPG key, beginning with `-----BEGIN PGP PUBLIC KEY BLOCK-----` and ending with `-----END PGP PUBLIC KEY BLOCK-----`