# Dotfiles

## Syncing dotfiles

Setting up synchronized dotfiles:

 ```
 $ git init --bare $HOME/.dotfiles
 $ alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME'
 $ dotfiles config status.showUntrackedFiles no
```