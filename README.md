# Configuration specifications

This are the configurations I use across my different machines. Instructions to
use the following configs after cloning the repository you can create symbolic
links for each of the files or folders to keep the latest repo changes.

```
  ln -s config/nvim ~/.config/nvim

  ln -s config/.tmux.config ~
```

## Pre-Requisites

Tools:

- fzf
- ripgrep
- tmux
- fd
- LazyGit

## TMUX

The TMUX configuration can be found on config/.tmux.config. To manage plugins
we use the tpm plugin, run the following command to download it:

`git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm`

## iTerm2

To use iTerm2 we need to configure it to use nerdfonts and oh-my-zsh.
