# Java

<details>
<summary>java -version</summary>

``` bash
java -version
openjdk version "1.8.0_362"
OpenJDK Runtime Environment (build 1.8.0_362-b09)
OpenJDK 64-Bit Server VM (build 25.362-b09, mixed mode)
```

</details>

<details>
<summary>dnf search java</summary>

``` bash
sudo dnf search java
java-1.8.0-openjdk.x86_64 : OpenJDK 8 Runtime Environment
java-1.8.0-openjdk-accessibility.x86_64 : OpenJDK 8 accessibility connector
java-1.8.0-openjdk-demo.x86_64 : OpenJDK 8 Demos
java-1.8.0-openjdk-devel.x86_64 : OpenJDK 8 Development Environment
java-1.8.0-openjdk-headless.x86_64 : OpenJDK 8 Headless Runtime Environment
java-1.8.0-openjdk-javadoc.noarch : OpenJDK 8 API documentation
java-1.8.0-openjdk-javadoc-zip.noarch : OpenJDK 8 API documentation compressed
                                      : in a single archive
java-1.8.0-openjdk-src.x86_64 : OpenJDK 8 Source Bundle
java-11-openjdk.x86_64 : OpenJDK 11 Runtime Environment
java-11-openjdk-demo.x86_64 : OpenJDK 11 Demos
java-11-openjdk-devel.x86_64 : OpenJDK 11 Development Environment
java-11-openjdk-headless.x86_64 : OpenJDK 11 Headless Runtime Environment
java-11-openjdk-javadoc.x86_64 : OpenJDK 11 API documentation
java-11-openjdk-javadoc-zip.x86_64 : OpenJDK 11 API documentation compressed in
                                   : a single archive
java-11-openjdk-jmods.x86_64 : JMods for OpenJDK 11
java-11-openjdk-src.x86_64 : OpenJDK 11 Source Bundle
java-11-openjdk-static-libs.x86_64 : OpenJDK 11 libraries for static linking
java-17-openjdk.x86_64 : OpenJDK 17 Runtime Environment
java-17-openjdk-demo.x86_64 : OpenJDK 17 Demos
java-17-openjdk-devel.x86_64 : OpenJDK 17 Development Environment
java-17-openjdk-headless.x86_64 : OpenJDK 17 Headless Runtime Environment
java-17-openjdk-javadoc.x86_64 : OpenJDK 17 API documentation
java-17-openjdk-javadoc-zip.x86_64 : OpenJDK 17 API documentation compressed in
                                   : a single archive
java-17-openjdk-jmods.x86_64 : JMods for OpenJDK 17
java-17-openjdk-src.x86_64 : OpenJDK 17 Source Bundle
java-17-openjdk-static-libs.x86_64 : OpenJDK 17 libraries for static linking
java-dirq.noarch : Directory based queue
java-latest-openjdk.x86_64 : OpenJDK 19 Runtime Environment
java-latest-openjdk-demo.x86_64 : OpenJDK 19 Demos
java-latest-openjdk-demo-fastdebug.x86_64 : OpenJDK 19 Demos optimised with full
                                          : debugging on
java-latest-openjdk-demo-slowdebug.x86_64 : OpenJDK 19 Demos unoptimised with
                                          : full debugging on
java-latest-openjdk-devel.x86_64 : OpenJDK 19 Development Environment
java-latest-openjdk-devel-fastdebug.x86_64 : OpenJDK 19 Development Environment
                                           : optimised with full debugging on
java-latest-openjdk-devel-slowdebug.x86_64 : OpenJDK 19 Development Environment
                                           : unoptimised with full debugging on
java-latest-openjdk-fastdebug.x86_64 : OpenJDK 19 Runtime Environment optimised
                                     : with full debugging on
java-latest-openjdk-headless.x86_64 : OpenJDK 19 Headless Runtime Environment
java-latest-openjdk-headless-fastdebug.x86_64 : OpenJDK 19 Runtime Environment
                                              : optimised with full debugging on
java-latest-openjdk-headless-slowdebug.x86_64 : OpenJDK 19 Runtime Environment
     ...: unoptimised with full debugging on
java-latest-openjdk-javadoc.x86_64 : OpenJDK 19 API documentation
java-latest-openjdk-javadoc-zip.x86_64 : OpenJDK 19 API documentation compressed
                                       : in a single archive
java-latest-openjdk-jmods.x86_64 : JMods for OpenJDK 19
java-latest-openjdk-jmods-fastdebug.x86_64 : JMods for OpenJDK 19 optimised with
                                           : full debugging on
java-latest-openjdk-jmods-slowdebug.x86_64 : JMods for OpenJDK 19 unoptimised
                                           : with full debugging on
java-latest-openjdk-slowdebug.x86_64 : OpenJDK 19 Runtime Environment
                                     : unoptimised with full debugging on
java-latest-openjdk-src.x86_64 : OpenJDK 19 Source Bundle
java-latest-openjdk-src-fastdebug.x86_64 : OpenJDK 19 Source Bundle for packages
                                         : with debugging on and optimisation
java-latest-openjdk-src-slowdebug.x86_64 : OpenJDK 19 Source Bundle for packages
                                         : with debugging on and no optimisation
java-latest-openjdk-static-libs.x86_64 : OpenJDK 19 libraries for static linking
java-latest-openjdk-static-libs-fastdebug.x86_64 : OpenJDK 19 libraries for
     ...: static linking optimised with full debugging on
java-latest-openjdk-static-libs-slowdebug.x86_64 : OpenJDK 19 libraries for
     ...: static linking unoptimised with full debugging on
```

</details>

<details>
<summary>wget</summary>

``` bash
wget https://download.oracle.com/java/20/latest/jdk-20_linux-x64_bin.rpm
```

</details>

<details>
<summary>install</summary>

``` bash
sudo rpm -ivh jdk-20_linux-x64_bin.rpm
[sudo] rocky のパスワード:
警告: jdk-20_linux-x64_bin.rpm: ヘッダー V3 RSA/SHA256 Signature、鍵 ID ec551f03: NOKEY
Verifying...                          ################################# [100%]
準備しています...              ################################# [100%]
更新中 / インストール中...
   1:jdk-20-2000:20-36                ################################# [100%]
```

``` bash
java -version
java version "20" 2023-03-21
Java(TM) SE Runtime Environment (build 20+36-2344)
Java HotSpot(TM) 64-Bit Server VM (build 20+36-2344, mixed mode, sharing)
which java
/usr/bin/java
```

</details>

<details>
<summary>jshell</summary>

``` bash
jshell
4月 08, 2023 12:12:49 午後 java.util.prefs.FileSystemPreferences$1 run
INFO: Created user preferences directory.
|  JShellへようこそ -- バージョン20
|  概要については、次を入力してください: /help intro

jshell> "Hello World!"
$1 ==> "Hello World!"

jshell> 'a'
$2 ==> 'a'

jshell> "Hello World!".toUpperCase()
$3 ==> "HELLO WORLD!"

# Ctrl + D
```

</details>

## Maven

``` bash
wget https://dlcdn.apache.org/maven/maven-3/3.9.1/binaries/apache-maven-3.9.1-bin.tar.gz
sudo tar xzvf apache-maven-3.9.1-bin.tar.gz -C /opt
sudo ln -s /opt/apache-maven-3.9.1 /opt/maven
sudo vim /etc/profile.d/maven.sh
```

`/etc/profile.d/maven.sh`

``` maven.sh
export JAVA_HOME=/usr/java/jdk-20
export M2_HOME=/opt/maven
export MAVEN_HOME=/opt/maven
export PATH=${M2_HOME}/bin:${PATH}
```

``` bash
chmod +x /etc/profile.d/maven.sh
source /etc/profile.d/maven.sh
```

``` bash
mvn -v
Apache Maven 3.9.1 (2e178502fcdbffc201671fb2537d0cb4b4cc58f8)
Maven home: /opt/maven
Java version: 20, vendor: Oracle Corporation, runtime: /usr/lib/jvm/jdk-20-oracle-x64
Default locale: ja_JP, platform encoding: UTF-8
OS name: "linux", version: "4.18.0-425.19.2.el8_7.x86_64", arch: "amd64", family: "unix"
```

---

## Ref

[How to Install Apache Maven on Rocky Linux / CentOS 8](https://linuxways.net/centos/how-to-install-apache-maven-on-rocky-linux-centos-8/)
