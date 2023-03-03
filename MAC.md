# Mac Setup

## Install software
```
xcode-select --install
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
echo 'source ~/powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc
# restart terminal
git config --global user.email "deiangu@gmail.com"
git config --global user.name "Deyan Gunchev"
git config --global pull.rebase true
ssh-keygen -t ed25519 -C "deiangu@gmail.com"

cat <<EOT >> ~/.ssh/config
Host github.com
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_ed25519
EOT

ssh-add --apple-use-keychain ~/.ssh/id_ed25519

pbcopy < ~/.ssh/id_ed25519.pub
# Paste in github ssh

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
(echo; echo 'eval "$(/usr/local/bin/brew shellenv)"') >> /Users/deyangunchev/.zprofile
eval "$(/usr/local/bin/brew shellenv)"
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | sh
curl -fsSL https://get.pnpm.io/install.sh | sh -
```

## .zshrc aliases
```
alias cd..='cd ..'

```