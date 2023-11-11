# vscode学习
## 1、一些快捷键
> ==1.== “ctrl” + “,” -------打开设置
> ==2.== “ctr” + “+”  -------页面缩放（+放大  -缩小）
## 2、参考资料
> https://blog.csdn.net/ArthurCaoMH/article/details/89300713
> 需要安装markdown 插件有五个：
> markdown (pdf Toc math preview-enhanced all-in-one)
##![Alt text](%E9%98%BF%E5%B0%94%E5%8D%91%E6%96%AF%E5%B1%B1%E9%A3%8E%E6%99%AF4k%E9%AB%98%E6%B8%85%E5%A3%81%E7%BA%B83840x2160_%E5%BD%BC%E5%B2%B8%E5%9B%BE%E7%BD%91.jpg)
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




