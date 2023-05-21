# manjaro记录
# majaro教程

## 更换国内源
[更换国内源参考教程](https://cloud.tencent.com/developer/article/1948468)

pacman一键更换国内源   
`sudo pacman-mirrors -c China`   
或者直接修改源文件`/etc/pacman.d/mirrorlist`   
(几个国内源都加上，前后顺序有优先级区别)
```
#manjaro国内源
Server = https://mirrors.ustc.edu.cn/manjaro/arm-stable/$repo/$arch
Server = https://mirrors.hit.edu.cn/manjaro/arm-stable/$repo/$arch
Server = http://mirrors.163.com/archlinuxarm/aarch64/$repo
```

如果pacman -Sy网络连接有问题，   
改DNS来解决，   
`nano /etc/resolv.conf`   
把内容改成
```
nameserver 223.5.5.5
nameserver 8.8.8.8
```

源文件路径   
`/etc/pacman.d/mirrorlist`   
配置文件   
`/etc/pacman.conf`   

## 中文乱码解决
(1) `nano /etc/locale.gen`
```
en_US.UTF-8 UTF-8
zh_CN.UTF-8 UTF-8
```

(2)执行
`sudo locale-gen`
执行下面命令看看是否配置好了中文编码
`locale`
`locale -a`

(3) 执行以下命令 立即生效
```
export LANG=zh_CN.UTF-8
```
把命令加到.bashrc里，   
作用是，   
bash每次启动将会自动执行命令，   
就不用每次手动执行了   
<br/>
## 常用命令
安装软件   
`pacman -S 软件名`

删除软件和它的依赖   
`pacman -Rs 软件名`

更新源 更新软件   
`pacman -Syu`   
(更新软件   
`pacman -Su`   
同步软件包数据库   
`pacman -Sy`   

搜索软件   
`pacman -Ss 关键字`

> 详细说明   
> pacman -Sy: 从服务器下载新的软件包数据库(实际上就是下载远程仓库最新软件列表到本地)   
> pacman -Su: 升级所有已安装的软件包   
> pacman -Syu:同步远程软件仓库并升级系统的软件包    

