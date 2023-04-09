# Rocky Linux 8 Settings

## General

## Optional

### bash

<details>
<summary>make install</summary>

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

---

## Refs

<details>
<summary>urls</summary>

[enginearn - Qiita](https://qiita.com/enginearn/following_users)

[デフォルトのShell を変更する](http://linux.kororo.jp/cont/tips/shell_change.php)

[Install Linux kernel-devel - Qiita](https://qiita.com/metheglin/items/60261f474ccdfb467574)

[CentOS 7 Kernel を 5.4系(kernel-lt)に変更する](https://kuni92.net/2022/01/centos-7-kernel.html)

[GitHub - enginearn/rocky-lunix-settings](https://github.com/enginearn/rocky-lunix-settings)

[Docker - Install Engine - Documentation](https://docs.rockylinux.org/gemstones/docker/)

[How To Install and Use Docker on Rocky Linux 8 | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-rocky-linux-8)

[Linuxでユーザーをグループに追加するコマンド | LFI](https://linuxfan.info/add-sub-group-command)

[Fix full screen problem in VirtualBox Rockylinux - General - Rocky Linux Forum](https://forums.rockylinux.org/t/fix-full-screen-problem-in-virtualbox-rockylinux/5554/6)

[Installing ZSH · ohmyzsh/ohmyzsh Wiki · GitHub](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)

[Install Python on Rocky Linux 8 - kifarunix.com](https://kifarunix.com/install-python-on-rocky-linux-8/)

[GitHub - pyenv/pyenv: Simple Python version management](https://github.com/pyenv/pyenv#installation)

[GitHub - nodesource/distributions: NodeSource Node.js Binary Distributions](https://github.com/nodesource/distributions)

[GitHub - tmux/tmux: tmux source code](https://github.com/tmux/tmux)

[[Linux]ファイルの圧縮、解凍方法 - Qiita](https://qiita.com/supersaiakujin/items/c6b54e9add21d375161f)

[とほほのtmux入門 - とほほのWWW入門](https://www.tohoho-web.com/ex/tmux.html)

[Rocky Linux 8にOpenJDK 17をインストール（AppStream） - Qiita](https://qiita.com/witchcraze/items/cf0e046d8f116a1abce8)

[Download Java for Linux](https://www.java.com/en/download/)

[CrownCloud Wiki - How To Install PHP 8 2 In Rocky Linux 8](https://wiki.crowncloud.net/?How_to_Install_PHP_8_2_in_Rocky_Linux_8)

[Visual Studio Code ソースコードはスニペットと「Ctrl + space」で書いちゃいなよ | MSeeeeN](https://mseeeen.msen.jp/vscode-snippet/)

[Linuxコマンド辞典 tmuxコマンド（ユーティリティ管理） | すなりんブログ](https://kcfran.com/2022/11/07/linux-command-tmux/)

[Tmux sessions should be nested with care, unset $TMUX to force](https://koenwoortman.com/tmux-sessions-should-be-nested-with-care-unset-tmux-to-force/)

[tmuxのデフォルトシェルをzshにしたいのに起動時にbashなる問題 - Qiita](https://qiita.com/puriso/items/9cec04eaba47a9d563ea)

[tmuxからクリップボードにコピーする（令和版） - Qiita](https://qiita.com/purutane/items/1d1dc4818013bbbaead4)

[約2年ぶりの更新となるGNU Bash v5.2](https://newspicks.com/news/7611719?ref=user_14)

[Bash/Zshで配列のn番目を取得する、を統一する](https://rcmdnk.com/blog/2018/08/19/computer-bash-zsh/)

[BashとZshの違いでのハマりどころ](https://rcmdnk.com/blog/2013/12/26/computer-bash-zsh/)

[Bash でインクリメントとデクリメント演算を行う方法 | Delft スタック](https://www.delftstack.com/ja/howto/linux/how-to-perform-increment-and-decrement-operation-in-bash/)

[各種テスト - bash - 算術式評価](https://www.loose-info.com/main/varioustests/bash/arithmetic_evaluation.html)

[Upper- or lower-casing strings in bash and zsh – Scripting OS X](https://scriptingosx.com/2019/12/upper-or-lower-casing-strings-in-bash-and-zsh/)

[unix - First character of a variable in a shell script to uppercase? - Stack Overflow](https://stackoverflow.com/questions/12420317/first-character-of-a-variable-in-a-shell-script-to-uppercase)

[bashの変数展開によるファイル名や拡張子の取得 - Qiita](https://qiita.com/mriho/items/b30b3a33e8d2e25e94a8)

[ls の実行結果を for 文で処理するワンライナー](https://zenn.dev/ikuraikura/articles/4aac30d719f9c52e79a3)

[bashでfileの拡張子を取得するには | ゴルディアスの涙目](https://gordiustears.net/getting-file-extention-by-bash/)

[ls の実行結果を for 文で処理するワンライナー](https://zenn.dev/ikuraikura/articles/4aac30d719f9c52e79a3)

</details>
