markdown-preview.nvim插件  
[开源地址](https://github.com/iamcco/markdown-preview.nvim)

测试环境  
<u>安卓13 arm64 termux nvim-nightly
</u>

## 安装依赖  
```
pkg install nodejs-lts
npm install -g yarn
```

## 编辑plugins.lua  
(文件一般位于~/.config/nvim/lua/目录)  
plugins.lua里加入以下代码  
```
use({ "iamcco/markdown-preview.nvim", run = "cd app && npm install", setup = function() vim.g.mkdp_filetypes = { "markdown" } end, ft = { "markdown" }, })
```
## 安装插件  
打开nvim，运行  
`:PackerInstall`

## 具体使用方法  
开启Mardown预览  
`:MarkdownPreview`   
关闭Mardown预览  
`:MarkdownPreviewStop`

> 注意!
> github上提供了几种方法，
> 不要使用以下这种方法，会造成无法预览的结果
```
use({  
    "iamcco/markdown-preview.nvim",  
    run = function() vim.fn["mkdp#util#install"]() end,  
})  
```
