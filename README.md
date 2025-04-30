# Soup-Base
The best ingredients start with a good base, as any good coding project starts with a proper environment setup.  This repo is here to keep a running tab of how I like to setup environments or computers to kickstart the dev process.

# Mac Setup

## Install Developer Tools

`xcode-select --install`

## Install VS Code

Here is the setup info to run VS Code on Mac: https://code.visualstudio.com/docs/setup/mac

It is important to add the ability to run VS Code from the command line.

## Setup Bash Preferences

### Install oh my zsh

https://ohmyz.sh/#install

I tend to prefer the agnoster theme with solarized dark color scheme: 
* https://ethanschoonover.com/solarized/
* https://github.com/altercation/solarized


Install powerline font: https://github.com/powerline/fonts

```
git clone https://github.com/powerline/fonts.git --depth=1
cd fonts
./install.sh
cd ..
rm -rf fonts
```
 
Current font choice: Roboto Mono for Powerline

### Install iTerm2

Download here: https://iterm2.com/

Go to settings and change: Profiles >> Colors >> Color Presets... >> Solarized Dark.

OPTIONAL: use ANSI Colors from here to update Terminal settings

#### Look into 

* Powerlevel 10k: https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#extremely-customizable

# Python Setup

Setup Python environment for contained environments

## Homebrew

https://brew.sh/


## uv - Python package & project manager

https://github.com/astral-sh/uv


_Because uv handles both python version and package management, I've migrated project usage there, but if there is a reason to use the separate tools, the install information is below_
<details>

<summary>Setup for usage of pyenv and poetry</summary>


## Pyenv

https://pypi.org/project/pyenv/

```
brew update
brew install pyenv
pyenv --version
```

Then add the following to your .zprofile & open a new shell after.  If this doesn' work, follow the instructions provided by `pyenv init`.

```
export PYENV_ROOT="$HOME/.pyenv"
[[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init -)"
```

https://realpython.com/intro-to-pyenv/


## Poetry

https://python-poetry.org/docs/

```
brew install poetry
poetry --version
```
</details>