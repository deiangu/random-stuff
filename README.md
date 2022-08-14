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