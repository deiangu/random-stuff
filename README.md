# Manjaro tweaks

- The vs code packge in the bg mirror is broken.
- For the google drive to show in file explorer install gvfs-google:
```
sudo pacman -S gvfs-google
```
- Vscode needs font settings to handle special glyphs:
```
"terminal.integrated.fontFamily": "'NotoSansMono Nerd Font', 'monospace', monospace",
```
- pnpm ignores node installed from nvm. Use .npmrc setting for node:
```
use-node-version=16.16.0
```
# Bash tweaks

```
# Install bash liquidprompt with powerline theme.
git clone --branch stable https://github.com/liquidprompt/liquidprompt.git ~/liquidprompt
echo  "[[ $- = *i* ]] && source ~/liquidprompt/liquidprompt && source liquidprompt/themes/powerline/powerline.theme && lp_theme powerline" >> ~/.bashrc

# Install custom fonts for powerline theme
wget https://github.com/powerline/powerline/raw/develop/font/PowerlineSymbols.otf
wget https://github.com/powerline/powerline/raw/develop/font/10-powerline-symbols.conf

mkdir -p ~/.local/share/fonts/
mv PowerlineSymbols.otf ~/.local/share/fonts/
fc-cache -vf ~/.local/share/fonts/

mkdir -p ~/.config/fontconfig/conf.d/
mv 10-powerline-symbols.conf ~/.config/fontconfig/conf.d/
```
