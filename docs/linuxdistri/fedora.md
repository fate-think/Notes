# fedora记录
> 日期 2023/05/21   
> 时间 下午

### 更新本地缓存   
`dnf makecache` 

### 清除索引缓存和下载包的缓存
`dnf clean all`

### 更换国内源
fedora 仓库配置文件为    
/etc/yum.repos.d/fedora.repo,

updates 仓库配置文件为     
/etc/yum.repos.d/fedora-updates.repo,      

具体步骤参考以下文档:    
[更换清华源帮助文档](https://mirrors.tuna.tsinghua.edu.cn/help/fedora/)    
[北京外国语大学镜像源帮助文档](https://mirrors.bfsu.edu.cn/help/fedora/)
