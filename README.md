# my-tmux

## Install
### 1. install tmux
  - normal
  ```bash=
  sudo apt install tmux
  ```
  
  - powerline-status 2.7
  ```bash=
  sudo pip install powerline-status
  ```
  
  or 2.8.1
  
  ```bash=
  sudo pip install git+https://github.com/powerline/powerline.git@develop
  ```
  
### 2. 安裝字體
```bash=
sudo apt install fonts-powerline
```

### 3. install gpakosz/tmux

```bash=
cd ~
mkdir ~/tmp
mv ~/.tmux.conf ~/tmp/
git clone https://github.com/gpakosz/.tmux.git
ln -s ~/.tmux/.tmux.conf ./
cp ~/.tmux/.tmux.conf.local ./
```

### 4. install my-tmux
```bash=
cd 
git clone https://github.com/wimterdom/my-tmux.git
cd my-tmux
cp .tmux.conf ~/.tmux/
cp .tmux.conf.local ~/.tmux/
```

### if path error
change `~/.tmux/.tmux.conf` & `~/.tmux/.tmux.conf.local` powerline.conf path to your own path

