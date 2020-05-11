# 如何用hugo搭建个人博客

## hugo的安装

1. mac安装方式


~~~
    brew install hugo
    hugo version
~~~
    
2. Windows安装方式

* [hugo下载地址](https://github.com/gohugoio/hugo/releases)
* 下载hugo_xxx_windows-64bit.zip
* 解压，将hugo放到D:\software\hugo\hugo.exe
* 把D:\software\hugo\加到PATH
* 重启终端，运行hugo version查看版本

## 用hugo写博客

1. [hugo官网](https://gohugo.io/)

2. reate a new site xxx.github.io.creater

~~~
  hugo new site quickstart
  ~~~
  
  3. Add a Theme
  
  ~~~
  cd quickstart
  git init
  git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke
  echo 'theme = "ananke"' >> config.toml
  ~~~
  
  4.Add Some Content
  
  ~~~
  hugo new posts/xxx.md
  title: "xxx xxx xxx"
date: 2019-03-26T08:47:11+01:00
draft: true
  ~~~
  
  注意：如果遇到问题，code错位所在目录，修改后重新运行
  
  
5. 撰写博客内容

6.start the hugo server

~~~
 hugo server -D
 ~~~
 
 7. custonize the theme
 
 code文件
 
 ~~~
 config.toml
 ~~~
 
 会看到如下代码
 
 ~~~
 baseURL = "https://example.org/"
languageCode = "zh-hands"
title = "My New Hugo Site"
theme = "ananke"
~~~

注意：

* 
~~~
baseURL = "https://example.org/"
~~~
中的网址应当改为Github Pages中显示的网址

7. Build static pages

~~~
hugo -D
~~~
9. 上传github

* 新建.gitignore,添加/public/

* 新建远程仓库，仓库名为xxx.github.io

* 
~~~
git remote add origion gir@xxxxxxxxxx

git push -u origion master
~~~

10. settings——————github pasge——————选择master————点击网址
