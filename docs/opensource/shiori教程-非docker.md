# Shiori部署教程 非docker部署
已测试 随身wifi arm64   
书签管理相关   
稍后阅读相关   
开源项目相关

> 日期 2023/05/25
> 时间 12:36

<br/>

Shiori 书签/稍后阅读应用
[开源地址](https://github.com/go-shiori/shiori)

<br/>

## 教程开始
- 从 release 页面下载最新的包，     
解压，chmod +x 给执行权限，把路径加到环境变量里

- 开启网站服务   
`shiori serve`   
或者   
`shiori serve -p 自定义端口`   
(默认8080端口)   
( 后台运行命令   
`shiori serve -p 端口 &>/dev/null & `  )

- 浏览器访问http://你的ip:8080 ,   
输入默认用户名 密码，登录。   
设置里点 ADD NEW ACCOUNT 添加一个自己的账号，会自动变成管理员账号。   
可以点+ 开始添加书签，体验阅读模式          
安装 浏览器插件(可选)   

<br/>

### 注释
默认的用户名是shiori    
默认的密码为 gopher    
数据目录是 ~/.local/share/shiori ，       
如果要备份或者迁移shiori，备份这个目录即可

