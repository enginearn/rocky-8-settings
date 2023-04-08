# PHP

<details>
<summary></summary>

``` bash
sudo dnf info php
メタデータの期限切れの最終確認: 2:00:36 時間前の 2023年04月08日 10時20分10秒 に実施しました。
利用可能なパッケージ
名前         : php
バージョン   : 7.2.24
リリース     : 1.module+el8.4.0+413+c9202dda
Arch         : x86_64
サイズ       : 1.5 M
ソース       : php-7.2.24-1.module+el8.4.0+413+c9202dda.src.rpm
リポジトリー : appstream
概要         : PHP scripting language for creating dynamic web sites
URL          : http://www.php.net/
ライセンス   : PHP and Zend and BSD and MIT and ASL 1.0
説明         : PHP is an HTML-embedded scripting language. PHP attempts to make it
             : easy for developers to write dynamically generated web pages. PHP also
             : offers built-in database integration for several commercial and
             : non-commercial database management systems, so writing a
             : database-enabled webpage with PHP is fairly simple. The most common
             : use of PHP coding is probably as a replacement for CGI scripts.
             : 
             : The php package contains the module (often referred to as mod_php)
             : which adds support for the PHP language to Apache HTTP Server.


```

</details>

<details>
<summary>set repos</summary>

``` bash
sudo dnf install https://dl.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm 
メタデータの期限切れの最終確認: 2:04:22 時間前の 2023年04月08日 10時20分10秒 に実施しました。
epel-release-latest-8.noarch.rpm                                         24 kB/s |  24 kB     00:01    
パッケージ epel-release-8-18.el8.noarch は既にインストールされています。
依存関係が解決しました。
行うべきことはありません。
完了しました!

```

``` bash
sudo dnf install https://rpms.remirepo.net/enterprise/remi-release-8.rpm 
メタデータの期限切れの最終確認: 2:05:05 時間前の 2023年04月08日 10時20分10秒 に実施しました。
remi-release-8.rpm                                                       28 kB/s |  31 kB     00:01    
依存関係が解決しました。
========================================================================================================
 パッケージ               アーキテクチャー   バージョン                  リポジトリー             サイズ
========================================================================================================
インストール:
 remi-release             noarch             8.7-2.el8.remi              @commandline              31 k

トランザクションの概要
========================================================================================================
インストール  1 パッケージ

合計サイズ: 31 k
インストール後のサイズ: 27 k
これでよろしいですか? [y/N]: y
パッケージのダウンロード:
トランザクションの確認を実行中
トランザクションの確認に成功しました。
トランザクションのテストを実行中
トランザクションのテストに成功しました。
トランザクションを実行中
  準備             :                                                                                1/1 
  インストール中   : remi-release-8.7-2.el8.remi.noarch                                             1/1 
  検証             : remi-release-8.7-2.el8.remi.noarch                                             1/1 

インストール済み:
  remi-release-8.7-2.el8.remi.noarch                                                                    

完了しました!

```

``` bash
dnf info php
Rocky Linux 8 - AppStream                                               1.5 MB/s |  10 MB     00:06    
Rocky Linux 8 - BaseOS                                                  1.5 MB/s | 6.1 MB     00:04    
Rocky Linux 8 - Extras                                                   14 kB/s |  12 kB     00:00    
Docker CE Stable - x86_64                                               186 kB/s |  40 kB     00:00    
Extra Packages for Enterprise Linux 8 - x86_64                          1.8 MB/s |  14 MB     00:07    
Node.js Packages for Enterprise Linux 8 - x86_64                        419 kB/s | 538 kB     00:01    
Remi's Modular repository for Enterprise Linux 8 - x86_64               399  B/s | 833  B     00:02    
Remi's Modular repository for Enterprise Linux 8 - x86_64               3.0 MB/s | 3.1 kB     00:00    
GPG 鍵 0x5F11735A をインポート中:
 Userid     : "Remi's RPM repository <remi@remirepo.net>"
 Fingerprint: 6B38 FEA7 231F 87F5 2B9C A9D8 5550 9759 5F11 735A
 From       : /etc/pki/rpm-gpg/RPM-GPG-KEY-remi.el8
これでよろしいですか? [y/N]: y
Remi's Modular repository for Enterprise Linux 8 - x86_64               396 kB/s | 1.3 MB     00:03    
Safe Remi's RPM repository for Enterprise Linux 8 - x86_64              494  B/s | 833  B     00:01    
Safe Remi's RPM repository for Enterprise Linux 8 - x86_64              3.0 MB/s | 3.1 kB     00:00    
GPG 鍵 0x5F11735A をインポート中:
 Userid     : "Remi's RPM repository <remi@remirepo.net>"
 Fingerprint: 6B38 FEA7 231F 87F5 2B9C A9D8 5550 9759 5F11 735A
 From       : /etc/pki/rpm-gpg/RPM-GPG-KEY-remi.el8
これでよろしいですか? [y/N]: y
Safe Remi's RPM repository for Enterprise Linux 8 - x86_64              534 kB/s | 2.3 MB     00:04    
Visual Studio Code                                                      2.3 MB/s |  34 MB     00:14    
利用可能なパッケージ
名前         : php
バージョン   : 7.2.24
リリース     : 1.module+el8.4.0+413+c9202dda
Arch         : x86_64
サイズ       : 1.5 M
ソース       : php-7.2.24-1.module+el8.4.0+413+c9202dda.src.rpm
リポジトリー : appstream
概要         : PHP scripting language for creating dynamic web sites
URL          : http://www.php.net/
ライセンス   : PHP and Zend and BSD and MIT and ASL 1.0
説明         : PHP is an HTML-embedded scripting language. PHP attempts to make it
             : easy for developers to write dynamically generated web pages. PHP also
             : offers built-in database integration for several commercial and
             : non-commercial database management systems, so writing a
             : database-enabled webpage with PHP is fairly simple. The most common
             : use of PHP coding is probably as a replacement for CGI scripts.
             : 
             : The php package contains the module (often referred to as mod_php)
             : which adds support for the PHP language to Apache HTTP Server.
```

</details>

<details>
<summary>module reset php</summary>

``` bash
sudo dnf module reset php
Remi's Modular repository for Enterprise Linux 8 - x86_64               374  B/s | 833  B     00:02    
Remi's Modular repository for Enterprise Linux 8 - x86_64               3.0 MB/s | 3.1 kB     00:00    
GPG 鍵 0x5F11735A をインポート中:
 Userid     : "Remi's RPM repository <remi@remirepo.net>"
 Fingerprint: 6B38 FEA7 231F 87F5 2B9C A9D8 5550 9759 5F11 735A
 From       : /etc/pki/rpm-gpg/RPM-GPG-KEY-remi.el8
これでよろしいですか? [y/N]: y
Remi's Modular repository for Enterprise Linux 8 - x86_64               351 kB/s | 1.3 MB     00:03    
Safe Remi's RPM repository for Enterprise Linux 8 - x86_64              499  B/s | 833  B     00:01    
Safe Remi's RPM repository for Enterprise Linux 8 - x86_64              2.8 MB/s | 3.1 kB     00:00    
GPG 鍵 0x5F11735A をインポート中:
 Userid     : "Remi's RPM repository <remi@remirepo.net>"
 Fingerprint: 6B38 FEA7 231F 87F5 2B9C A9D8 5550 9759 5F11 735A
 From       : /etc/pki/rpm-gpg/RPM-GPG-KEY-remi.el8
これでよろしいですか? [y/N]: y
Safe Remi's RPM repository for Enterprise Linux 8 - x86_64              389 kB/s | 2.3 MB     00:06    
メタデータの期限切れの最終確認: 0:00:01 時間前の 2023年04月08日 12時28分34秒 に実施しました。
依存関係が解決しました。
行うべきことはありません。
完了しました!

```

</details>

<details>
<summary>module list php</summary>

``` bash
sudo dnf module list php
メタデータの期限切れの最終確認: 0:00:35 時間前の 2023年04月08日 12時28分34秒 に実施しました。
Rocky Linux 8 - AppStream
Name            Stream             Profiles                             Summary                         
php             7.2 [d]            common [d], devel, minimal           PHP scripting language          
php             7.3                common [d], devel, minimal           PHP scripting language          
php             7.4                common [d], devel, minimal           PHP scripting language          
php             8.0                common [d], devel, minimal           PHP scripting language          

Remi's Modular repository for Enterprise Linux 8 - x86_64
Name            Stream             Profiles                             Summary                         
php             remi-7.2           common [d], devel, minimal           PHP scripting language          
php             remi-7.3           common [d], devel, minimal           PHP scripting language          
php             remi-7.4           common [d], devel, minimal           PHP scripting language          
php             remi-8.0           common [d], devel, minimal           PHP scripting language          
php             remi-8.1           common [d], devel, minimal           PHP scripting language          
php             remi-8.2           common [d], devel, minimal           PHP scripting language          

ヒント: [d]efault, [e]nabled, [x]disabled, [i]nstalled

```

</details>

<details>
<summary>module install php:remi-8.2</summary>

``` bash
sudo dnf module install php:remi-8.2
[sudo] rocky のパスワード:
メタデータの期限切れの最終確認: 0:26:33 時間前の 2023年04月08日 12時28分34秒 に実施しました。
依存関係が解決しました。
========================================================================================================
 パッケージ           Arch       バージョン                                      リポジトリー     サイズ
========================================================================================================
group/moduleパッケージをインストール:
 php-cli              x86_64     8.2.4-1.el8.remi                                remi-modular     5.4 M
 php-common           x86_64     8.2.4-1.el8.remi                                remi-modular     1.3 M
 php-fpm              x86_64     8.2.4-1.el8.remi                                remi-modular     1.9 M
 php-mbstring         x86_64     8.2.4-1.el8.remi                                remi-modular     579 k
 php-xml              x86_64     8.2.4-1.el8.remi                                remi-modular     255 k
依存関係のインストール:
 httpd-filesystem     noarch     2.4.37-51.module+el8.7.0+1182+86a6cd60.5        appstream         42 k
 oniguruma5php        x86_64     6.9.8-1.el8.remi                                remi-safe        212 k
弱い依存関係のインストール:
 nginx-filesystem     noarch     1:1.14.1-9.module+el8.4.0+542+81547229          appstream         23 k
モジュールプロファイルのインストール中:
 php/common                                                                                            
モジュールストリームの有効化中:
 httpd                           2.4                                                                   
 nginx                           1.14                                                                  
 php                             remi-8.2                                                              

トランザクションの概要
========================================================================================================
インストール  8 パッケージ

ダウンロードサイズの合計: 9.6 M
インストール後のサイズ: 44 M
これでよろしいですか? [y/N]: y
パッケージのダウンロード:
(1/8): nginx-filesystem-1.14.1-9.module+el8.4.0+542+81547229.noarch.rpm 104 kB/s |  23 kB     00:00    
(2/8): httpd-filesystem-2.4.37-51.module+el8.7.0+1182+86a6cd60.5.noarch 144 kB/s |  42 kB     00:00    
(3/8): php-common-8.2.4-1.el8.remi.x86_64.rpm                           332 kB/s | 1.3 MB     00:03    
(4/8): php-fpm-8.2.4-1.el8.remi.x86_64.rpm                              352 kB/s | 1.9 MB     00:05    
(5/8): php-xml-8.2.4-1.el8.remi.x86_64.rpm                              340 kB/s | 255 kB     00:00    
(6/8): oniguruma5php-6.9.8-1.el8.remi.x86_64.rpm                        543 kB/s | 212 kB     00:00    
(7/8): php-mbstring-8.2.4-1.el8.remi.x86_64.rpm                         100 kB/s | 579 kB     00:05    
(8/8): php-cli-8.2.4-1.el8.remi.x86_64.rpm                              447 kB/s | 5.4 MB     00:12    
--------------------------------------------------------------------------------------------------------
合計                                                                    695 kB/s | 9.6 MB     00:14     
Remi's Modular repository for Enterprise Linux 8 - x86_64               3.0 MB/s | 3.1 kB     00:00    
GPG 鍵 0x5F11735A をインポート中:
 Userid     : "Remi's RPM repository <remi@remirepo.net>"
 Fingerprint: 6B38 FEA7 231F 87F5 2B9C A9D8 5550 9759 5F11 735A
 From       : /etc/pki/rpm-gpg/RPM-GPG-KEY-remi.el8
これでよろしいですか? [y/N]: y
鍵のインポートに成功しました
トランザクションの確認を実行中
トランザクションの確認に成功しました。
トランザクションのテストを実行中
トランザクションのテストに成功しました。
トランザクションを実行中
  準備             :                                                                                1/1 
  scriptletの実行中: php-common-8.2.4-1.el8.remi.x86_64                                             1/8 
  インストール中   : php-common-8.2.4-1.el8.remi.x86_64                                             1/8 
  インストール中   : oniguruma5php-6.9.8-1.el8.remi.x86_64                                          2/8 
  scriptletの実行中: nginx-filesystem-1:1.14.1-9.module+el8.4.0+542+81547229.noarch                 3/8 
  インストール中   : nginx-filesystem-1:1.14.1-9.module+el8.4.0+542+81547229.noarch                 3/8 
  scriptletの実行中: httpd-filesystem-2.4.37-51.module+el8.7.0+1182+86a6cd60.5.noarch               4/8 
  インストール中   : httpd-filesystem-2.4.37-51.module+el8.7.0+1182+86a6cd60.5.noarch               4/8 
  インストール中   : php-fpm-8.2.4-1.el8.remi.x86_64                                                5/8 
  scriptletの実行中: php-fpm-8.2.4-1.el8.remi.x86_64                                                5/8 
  インストール中   : php-mbstring-8.2.4-1.el8.remi.x86_64                                           6/8 
  インストール中   : php-cli-8.2.4-1.el8.remi.x86_64                                                7/8 
  インストール中   : php-xml-8.2.4-1.el8.remi.x86_64                                                8/8 
  scriptletの実行中: php-xml-8.2.4-1.el8.remi.x86_64                                                8/8 
  scriptletの実行中: php-fpm-8.2.4-1.el8.remi.x86_64                                                8/8 
  検証             : httpd-filesystem-2.4.37-51.module+el8.7.0+1182+86a6cd60.5.noarch               1/8 
  検証             : nginx-filesystem-1:1.14.1-9.module+el8.4.0+542+81547229.noarch                 2/8 
  検証             : php-cli-8.2.4-1.el8.remi.x86_64                                                3/8 
  検証             : php-common-8.2.4-1.el8.remi.x86_64                                             4/8 
  検証             : php-fpm-8.2.4-1.el8.remi.x86_64                                                5/8 
  検証             : php-mbstring-8.2.4-1.el8.remi.x86_64                                           6/8 
  検証             : php-xml-8.2.4-1.el8.remi.x86_64                                                7/8 
  検証             : oniguruma5php-6.9.8-1.el8.remi.x86_64                                          8/8 

インストール済み:
  httpd-filesystem-2.4.37-51.module+el8.7.0+1182+86a6cd60.5.noarch                                      
  nginx-filesystem-1:1.14.1-9.module+el8.4.0+542+81547229.noarch                                        
  oniguruma5php-6.9.8-1.el8.remi.x86_64                                                                 
  php-cli-8.2.4-1.el8.remi.x86_64                                                                       
  php-common-8.2.4-1.el8.remi.x86_64                                                                    
  php-fpm-8.2.4-1.el8.remi.x86_64                                                                       
  php-mbstring-8.2.4-1.el8.remi.x86_64                                                                  
  php-xml-8.2.4-1.el8.remi.x86_64                                                                       

完了しました!

```

</details>

<details>
<summary>version</summary>

``` bash
php -v
PHP 8.2.4 (cli) (built: Mar 14 2023 16:11:05) (NTS gcc x86_64)
Copyright (c) The PHP Group
Zend Engine v4.2.4, Copyright (c) Zend Technologies

```

</details>How to Install PHP 8.2 in Rocky Linux 8

---

## Refs

[How to Install PHP 8.2 in Rocky Linux 8](https://wiki.crowncloud.net/?How_to_Install_PHP_8_2_in_Rocky_Linux_8)