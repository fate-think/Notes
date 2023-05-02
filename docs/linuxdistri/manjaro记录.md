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
Server = https://mirrors.sonic.net/manjaro/arm-stable/$repo/$arch
Server = https://mirrors.ustc.edu.cn/manjaro/arm-stable/$repo/$arch
Server = https://mirrors.hit.edu.cn/manjaro/arm-stable/$repo/$arch
Server = http://mirrors.163.com/archlinuxarm/aarch64/$repo
```

如果pacman -Sy网络连接有问题，
改DNS来解决，
即`nano /etc/resolv.conf`
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

(3)安装中文字体
`pacman -S wqy-zenhei`
(或者pacman -S wqy-zenhei ttf-fireflysung(flash乱码))
(或者pacman -S wqy-microhei)
(或者pacman -S wqy-bitmapfont wqy-microhei-lite wqy-zenhei)
(或者pacman -S noto-fonts-cjk)
(4) 执行(也可以加到.bashrc，可以只要第一行命令)
```
export LANG=zh_CN.UTF-8
export LANGUAGE=zh_CN:en_US
```

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
> pacman -Sy: 从服务器下载新的软件包数据库(实际上就是下载远程仓库最新软件列表到本地)。
> pacman -Su: 升级所有已安装的软件包。
> pacman -Syu:同步远程软件仓库并升级系统的软件包

