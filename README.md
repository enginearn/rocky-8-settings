# Rocky Linux 8 Settings

## General

## Optional

### bash

<details>
<summary>make install<summary>

``` bash
wget https://ftp.jaist.ac.jp/pub/GNU/bash/bash-5.2.15.tar.gz
cd bash-5.2.15
./configure
make
sudo make install
# reopen terminal
bash --version
GNU bash, バージョン 5.2.15(1)-release (x86_64-pc-linux-gnu)
Copyright (C) 2022 Free Software Foundation, Inc.
ライセンス GPLv3+: GNU GPL バージョン 3 またはそれ以降 <http://gnu.org/licenses/gpl.html>

This is free software; you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
```

</details>

### tmux

<details>
<summary>installations</summary>

``` bash
wget https://github.com/tmux/tmux/releases/download/3.3a/tmux-3.3a.tar.gz
tar -zvxf tmux-3.3a.tar.gz
cd tmux-3.3a

./configure
sudo dnf search libevent | grep devel
sudo dnf install libevent-devel
./configure
make
sudo make install
cd ~
tmux -V
tmux 3.3a
```

</details>

### basic usage

``` zsh
tmux
```

``` zsh
tmux ls

```

|command|description|
|--|--|
|`Ctrl+g` -> `-`|sepalate horizontal|
|`Ctrl+g` -> `\|`|sepalate vertical|
|`Ctrl+g` -> `,`|rename pane name|
|`Ctrl+g` -> `c`|new session|
|`Ctrl+g` -> `n`|move to next session|
|`Ctrl+g` -> `p`|move to previous session|
|`Ctrl+g` -> `x`|kill pane|
|`Ctrl+g` -> `d`|detouch pane|

### configration

<details>
<summary>.tmux.conf</summary>

``` .tmux.conf
# tmux起動時のshellをデフォルト設定してるshellにする
set -g default-shell "${SHELL}"
set -g default-command "${SHELL}"

# prefixをCtrl + gに変更
unbind C-b
set -g prefix C-g
bind C-g send-prefix

# 水平分割と垂直分割
bind \\ split-window -h
bind - split-window -v

# pane Noを表示
set -g display-panes-time 1000

# paneの開始を1からに変更
set -g base-index 1

# マウスでpineの切り替えやリサイズを有効にする
set -g mouse on

# マウスホイールでヒストリではなくスクロールできるようにする
# set -g mouse on
set -g terminal-override 'xterm*:smcup@:rmcup@'

# コピーモードのキー操作をviライクにする
set-window-option -g mode-keys vi
bind-key -T copy-mode-vi 'v' send -X begin-selection
bind-key -T copy-mode-vi 'C-v' send -X rectangle-toggle
bind-key -T copy-mode-vi 'y' send -X copy-selection

# コピーした際にwindowのクリップボードにも転送する
# Linux (dnf isntalll xsel)
bind-key -T copy-mode-vi Enter send-keys -X copy-pipe-and-cancel "xsel -bi"
# WSL
# bind-key -T copy-mode-vi Enter send-keys -X copy-pipe-and-cancel clip.exe

set -s escape-time 0

```

</details>
