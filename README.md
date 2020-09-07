# WSL2 Dotfiles

## Turn a windows PC into a "lean mean development machine" with WSL:

![Nice GIF](https://i.makeagif.com/media/6-01-2015/BzxHr5.gif)

---

---

### Activate WSL2 (powershell started as admin):

```
# enable WSL

dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart



# enable the 'Virtual Machine Platform' optional component

dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart



# set WSL2 as your default version

wsl --set-default-version 2
```

Linux kernel may need a update: [Check out here](https://docs.microsoft.com/en-us/windows/wsl/wsl2-kernel)

---

---

### Install Linux Distro of choice

Pick Linux distro from Windows store. I use Ubuntu 20.04 LTS

```
# linux housekeeping

sudo apt update -y && sudo apt upgrade -y



# install zsh

sudo apt install zsh

```

---

---

### Setup stuff in Linux:

```
# git setup:

git config --global user.name "John Doe"
git config --global user.email johndoe@example.com



# generate ssh-key:

ssh-keygen -t rsa -b 4096 -C "your_email@example.com"



# get ohmyzsh:

sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"



# get starship prompt:

curl -fsSL https://starship.rs/install.sh | bash



# get nvm:

curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash

```
