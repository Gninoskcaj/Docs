---
description: Play hangman from your terminal
---

# Hangman CLI

## Installation

Make sure you have python 3 installed.

```bash
# macOS
brew --version
# -> Homebrew 2.1.16

# if brew is not installed install it.
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
 
# then install python3
brew install python3

# Linux
sudo apt-get install python3.8


# Windows
# follow the instructions here:
# https://phoenixnap.com/kb/how-to-install-python-3-windows


# All versions
# When that finishes check if the install was successful:
python3 --version
```

Then install hangman:

```bash
git clone https://github.com/Gninoskcaj/hangman-cli
chmod +x ./hangman-cli/hangman
mkdir ~/bin
sudo mv ./hangman-cli/ ~/bin/
'export PATH=$PATH":$HOME/bin/hangman-cli"' >> .profile
source .profile
```

Thats it for installation, to start playing type `hangman`

## Usage

To play type `hangman`. See if you can win!

