# My Setup

## MAC OS Setup
### General
Appearance: Dark
### Users & Groups
* Login Options -> Show fast user switching menu as "Icon"

### Trackpad
Tap to click: Checked

### Keyboard
Key Repeat: Fast
Delay Until Repeat: Short

## Terminal setup
### zsh
Switch default shell to Zsh
```
chsh -s /bin/zsh
```
### Oh My ZSH!
https://ohmyz.sh/
```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
### zsh-autosuggestions
https://github.com/zsh-users/zsh-autosuggestions
```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions\n
```
### zsh-syntax-highlighting
https://github.com/zsh-users/zsh-syntax-highlighting
```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```
### zsh-z
https://github.com/agkozak/zsh-z
```
git clone https://github.com/agkozak/zsh-z $ZSH_CUSTOM/plugins/zsh-z
```
### .zshrc
See [.zhrc](.zshrc)

## brew
https://brew.sh/
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```
## Source Code Pro Font
https://github.com/adobe-fonts/source-code-pro
```
brew cask install font-source-code-pro
```
## iTerm2
https://www.iterm2.com/
```
brew cask install iterm2
```
* Preferences -> Profiles -> Window -> Columns: 125 & Rows: 45
* Preferences -> Profiles -> Text -> Font "Source Code Prod" : Size 13
## SublimeText
Text Editor
https://www.sublimetext.com/
```
brew cask install sublime-text
```
* Install Package (cmd+shift+p) -> "Install Package" -> ayu-mirage theme
* Preferences (cmd+,) -> 
```
{
	"color_scheme": "Packages/ayu/ayu-mirage.sublime-color-scheme",
	"theme": "ayu-mirage.sublime-theme",
	"ignored_packages":
	[
		"Vintage",
		"Markdown"
	],
	"font_face": "Source Code Pro",
	"font_size": 13,
	"margin": 2,
	"tab_size": 2,	
	"rulers":
    [
        120
    ],
  "translate_tabs_to_spaces": true,
  "word_wrap": true,
  "open_files_in_new_window": false
}
```
## Kdiff3
Diff Tool
http://kdiff3.sourceforge.net/
```
brew cask install https://raw.githubusercontent.com/Homebrew/homebrew-cask/6a96e5ea44803e52a43c0c89242390f75d1581ab/Casks/kdiff3.rb
```
Set Kdiff3 as default diff and merge tool in git
```
git config --global --edit
```
```
[diff]
        tool = kdiff3
[difftool "kdiff3"]
        path = /usr/local/bin/kdiff3
[difftool]
        prompt = false
        keepBackup = false
        trustExitCode = false
[merge]
        tool = kdiff3
[mergetool]
        prompt = false
        keepBackup = false
        keepTemporaries = false
[mergetool "kdiff3"]
        path = /usr/local/bin/kdiff3
```
## JDK
Add cask tap
```
brew tap homebrew/cask-versions
```
Install JDK
```
brew cask install java11
```
## VS Code
```
brew cask install visual-studio-code
```
