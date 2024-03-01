# dotfiles
Managing my configuration files in a github repo helps me to version-control my configurations.<br>
Also I can easily reuse them on different machines for work or private use.<br>
As suggested in this Arch Wiki [article](https://wiki.archlinux.org/title/Dotfiles) I am will be using an alias instead of symlinks.<br>
The dotfiles can be replicated on a new system like so:
```bash
$ git clone --bare <git-repo-url> $HOME/.dotfiles
$ alias dotfiles='/usr/bin/git --git-dir="$HOME/.dotfiles/" --work-tree="$HOME"'
$ dotfiles checkout
$ dotfiles config --local status.showUntrackedFiles no
```
