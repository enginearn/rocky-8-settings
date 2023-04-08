# Rocky Linux 8 Settings

## General

## Optional

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
