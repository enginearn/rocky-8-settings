# pyenv settings

``` bash
sudo dnf install bzip2-devel gdbm-devel libffi-devel libuuid-devel ncurses-devel openssl-devel readline-devel sqlite-devel xz-devel zlib-devel tk-devel
```

``` bash
curl https://pyenv.run | bash
```

``` bash
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(pyenv init -)"' >> ~/.bashrc
```

``` bash
source ~/.bashrc
```

``` bash
pyenv --version
```

``` bash
pyenv install --list
pyenv install 3.11.2
pyenv global 3.11.2
```

``` bash
python -V
```