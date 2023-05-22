# typecho换主题 教程
## 以抹茶主题为例

> 日期 2023/04/30   
> 时间 21:45

1. [matcha](https://github.com/BigCoke233/matcha)
以这个抹茶主题为例，release页面下载主题模板文件`Matcha.Ver.1.2.0.zip` ,把zip文件上传到阿里云服务器目录。

2. ssh连接服务器，解压文件
`unzip Matcha.Ver.1.2.0.zip`
,解压后得到`matcha`文件夹

3. 把主题文件夹移动到
`/www/wwwroot/typecho/usr/themes/`下
```
mv matcha /www/wwwroot/typecho/usr/themes
```

4. 进入网站后台,点更换外观，启用该主题即可。

