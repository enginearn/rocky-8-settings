# Nodejs

``` bash
sudo dnf info nodejs
[sudo] rocky のパスワード:
メタデータの期限切れの最終確認: 0:44:46 時間前の 2023年04月02日 22時16分19秒 に実施しました。
利用可能なパッケージ
名前         : nodejs
エポック     : 1
バージョン   : 10.24.0
リリース     : 1.module+el8.3.0+101+f84c7154
Arch         : x86_64
サイズ       : 8.8 M
ソース       : nodejs-10.24.0-1.module+el8.3.0+101+f84c7154.src.rpm
リポジトリー : appstream
概要         : JavaScript runtime
URL          : http://nodejs.org/
ライセンス   : MIT and ASL 2.0 and ISC and BSD
説明         : Node.js is a platform built on Chrome's JavaScript runtime
             : for easily building fast, scalable network applications.
             : Node.js uses an event-driven, non-blocking I/O model that
             : makes it lightweight and efficient, perfect for data-intensive
             : real-time applications that run across distributed devices.
```

``` bash
cd ~ && \
> curl -sL https://rpm.nodesource.com/setup_18.x -o nodesource_setup.sh
```

``` bash
sudo dnf install nodejs
```

``` bash
node -v
v18.15.0
```

``` bash
npm -v
9.5.0
sudo npm install -g npm@latest
npm -v
9.6.3
```