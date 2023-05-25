# Shiori部署教程
docker相关   
开源项目相关   
书签管理相关   
稍后阅读相关   

> 日期 2023/05/25    
> 时间 11:48

<br/>

Shiori 书签/稍后阅读应用        
[开源地址](https://github.com/go-shiori/shiori)

<br/>

## docker部署 支持arm64
已测试 随身wifi arm64   

- 拉取镜像   
```
docker pull ghcr.io/go-shiori/shiori
```

- 创建容器并运行   
```
docker run -d --name shiori -p 8080:8080 -v ~/dockerdata/shiori:/shiori ghcr.io/go-shiori/shiori:latest
```

- 登录使用    
浏览器访问http://你的ip:8080   
输入默认用户名 密码，登录。   
设置里点 ADD NEW ACCOUNT 添加一个自己的账号，会自动变成管理员账号。   
可以点+ 开始添加书签，体验阅读模式   
安装 浏览器插件(可选)

<br/>

### 注释1
-v后面的目录是本地存储的shiori数据位置(可以自定义)，    
如果要备份或者迁移shiori，备份这个目录即可


<br/>

### 注释2
默认端口是8080，可以自定义映射端口    
默认的用户名是shiori   
默认的密码为 gopher



