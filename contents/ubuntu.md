# Ubuntu initial setup

> first update
```bash
sudo apt-get update && sudo apt-get upgrade -y
```

> virtual machine: [instructions](https://gist.github.com/fscheidt/aa7d22d0dbf2586d6fb32583c6b567b6)

> basic utilities:
```bash
sudo apt install vim curl mcedit git -y
```

> zip tools
```bash
sudo apt install rar unrar p7zip-full p7zip-rar -y;
```

> utilities
```bash
sudo apt install silversearcher-ag jq w3m pandoc fzf pigz figlet sqlite3 meld -y;
```

> utilities 2
```bash
sudo apt install neofetch htop xsel xclip tmux dconf-editor -y;
```

```
sudo apt-get install ripgrep pdfgrep -y
```

> essential
- [bat](https://github.com/sharkdp/bat/releases/latest)
- [fd](https://github.com/sharkdp/fd/releases/latest)
- tilix
- fzf:
```bash
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install
```

> network

```bash
sudo apt-get install openssh-server -y
```

```
sudo systemctl enable ssh; sudo systemctl start ssh
```

> web tools
```bash
sudo apt install httpie
sudo snap install postman
```

> LAMP
```bash
sudo apt install apache2 -y
sudo apt install php libapache2-mod-php php-mysql -y
sudo apt-get install php-mbstring php-xml php-apcu php-intl php-sqlite3 -y
```


> gh cli
```bash
curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo gpg --dearmor -o /usr/share/keyrings/githubcli-archive-keyring.gpg

echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null

sudo apt update && sudo apt install gh -y
```


> brave browser
```bash
sudo apt install apt-transport-https curl -y

sudo curl -fsSLo /usr/share/keyrings/brave-browser-archive-keyring.gpg https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg

echo "deb [signed-by=/usr/share/keyrings/brave-browser-archive-keyring.gpg arch=amd64] https://brave-browser-apt-release.s3.brave.com/ stable main" | sudo tee /etc/apt/sources.list.d/brave-browser-release.list

sudo apt update ; sudo apt install brave-browser -y
```

> docs helper
```bash
sudo npm install -g tldr
```
