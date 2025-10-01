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

## MacOS

### iTerm2

To use iTerm2 we need to configure it to use nerdfonts and oh-my-zsh. If you
want to use a specific color theme you need to download it and import it (ex. Dracula)

```
# Step 1: Install iTerm2
brew install --cask iterm2

# Step 2: Install oh-my-zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# Step 3: Install PowerLevel10k for oh-my-zsh
git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k

# Step 4: Create a symbolic link for .zshrc
ln -s ~/config/.zshrc ~/

# Step 5: If the p10k configuration does not start (optional)
p10k configure

# Step 6: Install ZSH plugins
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

# Step 7: Source the file
source ~/.zshrc

```

\*Note: Lines 144 - 124 are dependant on other software like Docker Desktop,
Angular CLI and k8s if you are not using any of those you may remove them.
