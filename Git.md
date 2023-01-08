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