
English | [简体中文](./openEuler_UKUI_offline_install_cn.md)

# How to install UKUI on openEuler(offline)

UKUI is a Linux desktop built by the KylinSoft software team over the years, primarily based on GTK and QT. Compared to other UI interfaces, UKUI is easy to use. The components of UKUI are small and low coupling, can run alone without relying on other suites. It can provide user a friendly and efficient experience.

UKUI supports both x86_64 and aarch64 architectures. Since the UKUI-owned package is not yet fully entered the official source of openEuler, the current installation method requires some additional steps.

## aarch64
1.Install openEuler system. Download address: https://repo.openeuler.org/openEuler-20.03-LTS/ISO/.
2.Configure source information

It's basically the [same method](./openEuler_UKUI_install.md) to configure the official source. You can also use Everything ISO as local source. 

**Config UKUI source**

a)Install createrepo package(`yum install createrepo`).

b)Download these files:
```
Link:https://pan.baidu.com/s/11PWuSuf_OZZFwEZtiERrLg 
Extraction code:7gti
```

c)Put reinstall.zip, install.sh in `/root`directory and create a new directory called RPMS in `/`. Then put the whole RPMS directory which you just download in directory `/RPMS`.
Modify file /etc/yum.repos.d/openEuler_aarch64.repo, Add the following at the end:

```
[ukui]
name=ukui
baseurl=file:///RPMS/
enabled=1
gpgcheck=0
priority=1
```

3.Change to root directory, run the following command as root:

```
cd /root/
createrepo ./../RPMS     
unzip reinstall.zip
chmod a+x install.sh
./install.sh
```

4.If you want to start with graphical interface after confirming the installation, please run this code and reboot.

```
systemctl set-default graphical.target
```
At present, UKUI version is still constantly updated. Please check the latest installation method: [https://gitee.com/openeuler/ukui](https://gitee.com/openeuler/ukui)


## x86_64
1.Install openEuler system. Download address: https://repo.openeuler.org/openEuler-20.03-LTS/ISO/。
2.Configure source information

It's basically the [same method](./openEuler_UKUI_install.md) to configure the official source. You can also use Everything ISO as local source. 

**Config UKUI source**

a)Install createrepo package(`yum install createrepo`).

b)Download these files:
```
Link:https://pan.baidu.com/s/1BDUyj5pRssqMOlZ7mfLh7Q 
Extraction code:b9o0
```

c)Put reinstall.zip, install.sh in `/root`directory and create a new directory called RPMS in `/`. Then put the whole RPMS directory which you just download in directory `/RPMS`.
Modify file /etc/yum.repos.d/openEuler_aarch64.repo, Add the following at the end:

```
[ukui]
name=ukui
baseurl=file:///RPMS/
enabled=1
gpgcheck=0
priority=1
```

3.Change to root directory, run the following command as root:

```
cd /root/
createrepo ./../RPMS  
unzip reinstall.zip
chmod a+x install.sh
./install.sh
```

4.If you want to start with graphical interface after confirming the installation, please run this code and reboot.

```
systemctl set-default graphical.target
```
At present, UKUI version is still constantly updated. Please check the latest installation method: [https://gitee.com/openeuler/ukui](https://gitee.com/openeuler/ukui)