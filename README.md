# Set up Mac OS for developers

This repository provides instructions on how to set up your Mac OS for developers. Whether you are starting a new development project or setting up your development environment, this guide will walk you through the necessary tools, applications, and plugins you need to install and how to install them.

Table of contents
=================

- 🚨 PRIORITY FOR DEV 🚨
    - [Oh My Zsh](#install-oh-my-zsh)
    - [Homebrew](#install-homebrew)
    - [MAS](#install-mas)
    - [MariaDB](#install-mariadb)
    - [NVM](#install-nvm)
    - [Yarn](#install-yarn)
    - [Php](#install-php)
    - [Composer](#install-composer)
    - [Laravel Valet](#install-laravel-valet)
    - [PhpMyAdmin](#install-phpmyadmin)
    - [Generate SSH Key Github](#generate-ssh-key-github)
- 🚨 APP’s 🚨
    - [Visual Studio Code](#install-visual-studio-code)
    - [Hyper](#install-hyper)
    - [Docker](#install-docker)
    - [Alt-Tab](#install-alt-tab)
    - [RayCast](#install-raycast)
    - [Discord](#install-discord)
    - [Sequel Ace](#install-sequel-ace)
    - [Numi](#install-numi)
    - [Loom](#install-loom)
    - [amphetamine](#install-amphetamine)
    - [Browsers](#install-browsers)
    - [Google Drive](#install-google-drive)
    - [Spotify](#install-spotify)
    - [Teams](#install-teams)
    - [Ngrok](#install-ngrok)
    - [Figma](#install-figma)
    - [Postman](#install-postman)
- 🚨 PLUGINS 🚨
    - [Auto suggestion for zsh terminal](#install-auto-suggestion-for-zsh-terminal)
    - [zsh-syntax-highlighting for terminal](#install-zsh-syntax-highlighting-for-terminal)
    - [See All hidden files in Finder](#see-all-hidden-files-in-finder)
    - [TheFuck](#install-thefuck)
    - [Gitmoji](#install-gitmoji)
- httpd-setup
    - [httpd-setup](#httpd-setup)

## 🚨 PRIORITY FOR DEV 🚨

### Install oh my zsh

**Oh My Zsh** is an open source, community-driven framework for managing your Zsh configuration.

```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

---

### Install Homebrew

The Missing Package Manager for macOS (or Linux)

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

---

### Install MAS

**mas** is a plugin for download MacOs app store apps

```
brew install mas
```

---

### Install MariaDB

**MariaDB** is a database management system

```bash
brew install mariadb

mysql.server start

brew services start mariadb
```

<aside>
💡 Set Up

```bash
sudo mysql_secure_installation
```

Follow this questions with this responses :

- Responses to do:
    - N
    - Y
    - “Your new password” = root
    - Y
    - Y
    - Y
    - Y

For finish, restart mariadb:

```bash
brew services restart mariadb
```

</aside>

---

### Install NVM

Node Version Manager

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash

export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"

[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm

nvm install node # "node" is an alias for the latest version

nvm install 8.0 # install node v8
```

---

### Install Yarn

**Yarn** is a software packaging system

```bash
brew install yarn
```

---

### Install php

Free programming language, mainly used to produce dynamic web pages via an HTTP server

```bash
brew install php
// or
brew install php@8.1
```

---

### Install Composer

A Dependency Manager for PHP

```bash
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === '55ce33d7678c5a611085589f1f3ddf8b3c52d662cd01d4ba75c0ee0459970c2200a51f492d557530c71c15d8dba01eae') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
sudo mv composer.phar /usr/local/bin/composer
```

---

### Install Laravel Valet:

**Laravel Valet** is a development environment for macOS minimalists.

```bash
brew update

brew install php

composer global require laravel/valet

export PATH=$PATH:~/.composer/vendor/bin

valet install
```

In your folder “Sites”, do :

```bash
valet park
```

For verify if valet is actually working : 

```bash
valet parked
```

---

### Install PhpMyAdmin

**phpMyAdmin** is a free software tool written in PHP, intended to handle the administration of MySQL over the Web

<aside>
💡 Go to the website [phpmyadmin](https://www.phpmyadmin.net/) & download it in your “Sites” folder. Open the zip and delete the zip.

</aside>

---

### Generate SSH Key Github

```bash
ssh-keygen -t ed25519 -C "Your github email"
```

You need to follow this [tuto](https://docs.github.com/en/authentication/connecting-to-github-with-ssh) ;)

## 🚨 APP’s 🚨

### Install Visual Studio Code

```bash
brew install --cask visual-studio-code
```

<aside>
💡 Set Up shell command

```
Launch Vs Code and do f1
Search “code” and launch this:
"Shell Command: Install 'code' command in PATH"
```

</aside>

---

### Install Hyper

A terminal ******built on web technologies.

[Hyper™](https://hyper.is/)

---

### Install Docker

**Docker** is a platform to launch certain applications in software containers.

```bash
brew install --cask docker
```

---

### Install Alt-Tab

**AltTab**brings the power of Windows *alt-tab* to macOS.

```bash
brew install --cask alt-tab
```

---

### Install RayCast

**Raycast** is a blazingly fast, totally extendable launcher. It lets you complete tasks, calculate, share common links, and much more.

[Raycast - Supercharged productivity](https://www.raycast.com/)

---

### Install Discord

**Discord** is a free proprietary software for VoIP and instant messaging.

```bash
brew install --cask discord
```

---

### Install Sequel Ace

MySQL/MariaDB database management for macOS.

```bash
brew install --cask sequel-ace
```

<aside>
💡 Test Sequel Ace

You can test your connection with your [localhost](http://localhost) !

```
host: localhost // 127.0.0.1
Username: root
Password: "your password"
Port: 80
```

</aside>

---

### Install Numi

Beautiful calculator app for Mac.

```bash
brew install --cask numi
```

---

### Install Loom

```
brew install --cask loom
```

---

### Install amphetamine

```
mas install 937984704
```

---

### Install Browsers

- brave
    
    ```
    brew install brave-browser
    ```
    
- Chrome
    
    ```
    brew install google-chrome
    ```
    
- Firefox
    
    ```
    brew install firefox
    ```
    

---

### Install Google Drive

```bash
brew install --cask google-drive
```

---

### Install Spotify

```bash
brew install --cask spotify
```

---

### Install Teams

```bash
brew install --cask microsoft-teams
```

---

### Install Ngrok

```bash
brew install --cask ngrok
```

---

### Install Figma

```bash
brew install --cask figma
```

---

### Install Postman

```bash
brew install --cask postman
```

---

## 🚨 PLUGINS 🚨

### Install Auto suggestion for zsh terminal

```bash
cd $ZSH_CUSTOM/plugins

git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

<aside>
💡 Configuration :

```bash
code ~/.zshrc
```

After that, search :

```bash
plugins=(git)
```

and add :

```bash
plugins=(
	git 
	**zsh-autosuggestions**
)
```

</aside>

---

### Install zsh-syntax-highlighting for terminal

```bash
brew install zsh-syntax-highlighting
```

<aside>
💡 Configuration :

The terminal will show you a source to add in zsh config.

So open zsh config :

```bash
code ~/.zshr
```

And add the source code at the end :)

</aside>

---

### See All hidden files in Finder

```bash
defaults write com.apple.Finder AppleShowAllFiles true

killall Finder
```

---

### Install TheFuck

Magnificent app which corrects your previous console command.

```bash
brew install thefuck
```

<aside>
💡 Configuration :

```bash
code ~/.zshrc
```

And add this alias at the end of the code :

```bash
eval $(thefuck --alias)
```

</aside>

---

### Install Gitmoji

An emoji guide for your commit messages

```bash
brew install gitmoji
```

## HTTPD Setup

If your looking for httpd setup, you can check this configuration [here](https://gist.github.com/karlhillx/b2ccb9ea1f30ff59505311e1908c3dc4)  made by [karlhillx](https://gist.github.com/karlhillx) 😃
