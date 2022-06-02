
[English](./openEuler_UKUI_offline_install.md) | 简体中文

# openEuler上UKUI的安装方法(离线)
UKUI是麒麟软件团队历经多年打造的一款Linux 桌面，主要基于 GTK 和 QT开发。与其它UI界面相比，UKUI易用性和敏捷度，各元件相依性小，可以不倚赖其它套件而独自运行，给用户带来亲切和高效的使用体验。

UKUI支持x86_64和aarch64两种架构。由于目前UKUI所属包还未能完全进入openEuler所属的官方源，所以目前的安装需要一些额外的步骤。

## aarch64安装方法
1.安装openEuler。下载地址：https://repo.openeuler.org/openEuler-20.03-LTS/ISO/。

2.配置源信息并安装

配置官方源的方法和[以前](./openEuler_UKUI_install_cn.md)相同，也可挂载everything版的ISO作为本地镜像。
和在线安装最大的不同就是要手工配置UKUI的离线源。

**配置UKUI的离线源**

a)安装createrepo(`yum install createrepo`).

b)下载必须文件:
```
链接：https://pan.baidu.com/s/11PWuSuf_OZZFwEZtiERrLg 
提取码：7gti
```

c)将下载的reinstall.zip、install.sh放入`/root`目录下，在`/`目录下新建文件夹RPMS，并将下载的整个RPMS文件夹放入`/RPMS`目录下。
修改/etc/yum.repos.d/openEuler_aarch64.repo文件，在末尾添加如下内容：

```
[ukui]
name=ukui
baseurl=file:///RPMS/
enabled=1
gpgcheck=0
priority=1
```

3.切换到root目录，以root用户运行以下命令：

```
cd /root/
createrepo ./../RPMS
unzip reinstall.zip
chmod a+x install.sh
./install.sh
```

4.在确认正常安装后，如果希望以图形界面的方式启动，请在命令行运行以下代码，并重启（`reboot`）。
```
systemctl set-default graphical.target
```
目前UKUI版本还在不断的更新，最新的安装方法请查阅[https://gitee.com/openeuler/ukui](https://gitee.com/openeuler/ukui)


## x86_64安装方法
1.安装openEuler。下载地址：https://repo.openeuler.org/openEuler-20.03-LTS/ISO/。

2.配置源信息并安装

配置官方源的方法和[以前](./openEuler_UKUI_install_cn.md)相同，也可挂载everything版的ISO作为本地镜像。
和在线安装最大的不同就是要手工配置UKUI的离线源。

**配置UKUI的离线源**

a)安装createrepo(`yum install createrepo`).

b)下载必须文件:
```
链接：https://pan.baidu.com/s/1BDUyj5pRssqMOlZ7mfLh7Q 
提取码：b9o0
```

c)将下载的reinstall.zip、install.sh放入/root目录下。在`/`目录下新建文件夹RPMS，并将下载的整个RPMS文件夹放入`/RPMS`目录下。
修改/etc/yum.repos.d/openEuler_x86_64.repo文件，在末尾添加如下内容：

```
[ukui]
name=ukui
baseurl=file:///RPMS/
enabled=1
gpgcheck=0
priority=1
```

3.切换到root目录，以root用户运行以下命令：

```
cd /root/
createrepo ./../RPMS
unzip reinstall.zip
chmod a+x install.sh
./install.sh
```

4.在确认正常安装后，如果希望以图形界面的方式启动，请在命令行运行以下代码，并重启（`reboot`）。
```
systemctl set-default graphical.target
```
目前UKUI版本还在不断的更新，最新的安装方法请查阅[https://gitee.com/openeuler/ukui](https://gitee.com/openeuler/ukui)

