## archlinux源文件路径
/etc/pacman.d/mirrorlist


## 添加清华源
(教程在这里https://mirrors.tuna.tsinghua.edu.cn/help/archlinuxarm/)   
(注意termux容器里要用http，https会报错)
```
Server = http://mirrors.tuna.tsinghua.edu.cn/archlinuxarm/$arch/$repo
```

## 更新软件包缓存
`pacman -Syy`

## 安装fd
`pacman -S fd`
