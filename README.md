# my-tmux

## Install
### 1. install tmux
  - normal
  ```bash=
  sudo apt install tmux
  ```
### 2. install powerline
  - powerline
  ```bash=
  sudo apt install powerline -y
  ```
  並在.bashrc 貼上
  ```bash=
  if [ -f `which powerline-daemon` ]; then
      powerline-daemon -q
      POWERLINE_BASH_CONTINUATION=1
      POWERLINE_BASH_SELECT=1
      . /usr/share/powerline/bindings/bash/powerline.sh
  fi
  ```
  
  - powerline-status 2.7
  ```bash=
  sudo pip install powerline-status
  ```
  
  - powerline 2.8.1
  
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
(1)
```bash=
cd 
git clone https://github.com/wimterdom/my-tmux.git
cd my-tmux
cp .tmux.conf ~/.tmux/
cp .tmux.conf.local ~/.tmux/
```
(2)或更改~/.tmux.conf.local 
- clone  gpakosz/tmux 直接修改~/.tmux.conf.local
以下僅顯示更動的地方
```bash=
source "/usr/local/lib/python3.8/dist-packages/powerline/bindings/tmux/powerline.conf"
tmux_conf_theme_24b_colour=true
tmux_conf_theme_focused_pane_bg='default'
tmux_conf_theme_pane_border_style=fat
tmux_conf_theme_left_separator_main='\uE0B0'
tmux_conf_theme_left_separator_sub='\uE0B1'
tmux_conf_theme_right_separator_main='\uE0B2'
tmux_conf_theme_right_separator_sub='\uE0B3'
#tmux_conf_battery_bar_symbol_full='◼'
#tmux_conf_battery_bar_symbol_empty='◻'
tmux_conf_battery_bar_symbol_full='♥'
tmux_conf_battery_bar_symbol_empty='·'
tmux_conf_copy_to_os_clipboard=true
set -g mouse on
```
- 修改~/.tmux/.tmux.conf
以下為增加部分
```bash=
source "/usr/local/lib/python3.8/dist-packages/powerline/bindings/tmux/powerline.conf"
set -g mouse on
```
### if path error
change `~/.tmux/.tmux.conf` & `~/.tmux/.tmux.conf.local` powerline.conf path to your own path

