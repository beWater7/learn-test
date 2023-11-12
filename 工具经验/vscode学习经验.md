# vscode学习
## 1、一些快捷键
> ==1.== “ctrl” + “,” -------打开设置
> ==2.== “ctr” + “+”  -------页面缩放（+放大  -缩小）
## 2、参考资料
> https://blog.csdn.net/ArthurCaoMH/article/details/89300713
> 需要安装markdown 插件有五个：
> markdown (pdf Toc math preview-enhanced all-in-one)

<p align="center">
<img alt="a test picture" src="../img/阿尔卑斯山风景4k高清壁纸3840x2160_彼岸图网.jpg" width="600">

## 3、如何远程连接到Ubuntu
>1. 首先需要确保你的ubuntu下已经安装了openssh库
>2. 修改vi /etc/ssh/sshd_config，PermitRemoteLogin yes
>3. 启动/etc/init.d/ssh restart
>4. 获取ubuntu下的ip，username
>5. vscode下需要安装remote ssh插件
>6. 插件设置需要右键将本机的ssh配置文件加进去
   extension setting     C:\Users\xxxx\.ssh\config
>7. 在search栏或左下角（两个L）可以新增远程主机，输入主机名：
ubuntu ip：虚拟机ip username：xxxx
>8.连接时需要输入主机平台类型（linux），continue后要输入密码（虚拟机密码）




