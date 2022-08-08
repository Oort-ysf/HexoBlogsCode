---
title: 【Hexo】博客搭建
date: 2022-08-08 21:37:13
tags: Hexo
description: Hexo博客搭建
---

## 1、前置准备

### 1.1、依赖安装

- `Git`
- `NodeJs`
- `Hexo`

安装教程请参考[【树莓派】常用应用安装]()



## 2、博客搭建

### 2.1、Hexo初始化

使用Hexo的默认框架

~~~bash
mkdir Blogs
cd Blogs
hexo init
~~~



### 2.2、博客配置

博客配置详情参考[【Hexo】博客美化]()



## 3、本地测试

可在本地调试查看博客效果

~~~bash
# 清理缓存
hexo clean

# 博客生成
# hexo g
hexo generate 

# 在本地运行
# hexo s
hexo server
~~~



## 4、在GitHub上发布

### 4.1、创建仓库

在`GitHub`上创建个人仓库，仓库名称随意

![4-1 创建仓库](%E3%80%90Hexo%E3%80%91%E5%8D%9A%E5%AE%A2%E6%90%AD%E5%BB%BA/4-1%20%E5%88%9B%E5%BB%BA%E4%BB%93%E5%BA%93.png)

### 4.2、配置GitHub Pages

为刚刚创建的仓库配置`GitHub Pages`

![4-2 配置GitHub Pages-1](%E3%80%90Hexo%E3%80%91%E5%8D%9A%E5%AE%A2%E6%90%AD%E5%BB%BA/4-2%20%E9%85%8D%E7%BD%AEGitHub%20Pages-1.png)

![4-2 配置GitHub Pages-2](%E3%80%90Hexo%E3%80%91%E5%8D%9A%E5%AE%A2%E6%90%AD%E5%BB%BA/4-2%20%E9%85%8D%E7%BD%AEGitHub%20Pages-2.png)

![4-2 配置GitHub Pages-3](%E3%80%90Hexo%E3%80%91%E5%8D%9A%E5%AE%A2%E6%90%AD%E5%BB%BA/4-2%20%E9%85%8D%E7%BD%AEGitHub%20Pages-3.png)



### 4.3、本地配置Git信息

~~~bash
git config --global user.email "achieveordie@163.com"
git config --global user.name "Oort."
~~~



### 4.4、添加SSH密钥

1、生成密钥

~~~bash
ssh-keygen -t rsa -C "achieveordie@163.com"
~~~

2、将公钥添加到`GitHub`

![4-4 添加SSH密钥-1](%E3%80%90Hexo%E3%80%91%E5%8D%9A%E5%AE%A2%E6%90%AD%E5%BB%BA/4-4%20%E6%B7%BB%E5%8A%A0SSH%E5%AF%86%E9%92%A5-1.png)

![4-4 添加SSH密钥-2](%E3%80%90Hexo%E3%80%91%E5%8D%9A%E5%AE%A2%E6%90%AD%E5%BB%BA/4-4%20%E6%B7%BB%E5%8A%A0SSH%E5%AF%86%E9%92%A5-2.png)

公钥在`id_rsa.pub`文件中，将该文件中的所有内容复制到`Key`的填充框中

![4-4 添加SSH密钥-3](%E3%80%90Hexo%E3%80%91%E5%8D%9A%E5%AE%A2%E6%90%AD%E5%BB%BA/4-4%20%E6%B7%BB%E5%8A%A0SSH%E5%AF%86%E9%92%A5-3.png)

添加成功后如下所示

![4-4 添加SSH密钥-4](%E3%80%90Hexo%E3%80%91%E5%8D%9A%E5%AE%A2%E6%90%AD%E5%BB%BA/4-4%20%E6%B7%BB%E5%8A%A0SSH%E5%AF%86%E9%92%A5-4.png)



### 4.5、博客添加发布地址

修改`Blogs/_config.yml`文件，修改内容如下

~~~yaml
# Site
title: Oort. - PersonalBlogs
subtitle: 'Personal Blogs'
description: 'This is personal blogs for Oort.'
keywords:
author: Oort
language: cn
timezone: 'Asia/Shanghai'

# URL
## Set your site url here. For example, if you use GitHub Page, set url as 'https://username.github.io/project'
url: https://Oort-ysf.github.io/Blogs/
root: /Blogs/
permalink: :title/
permalink_defaults:
pretty_urls:
  trailing_index: true # Set to false to remove trailing 'index.html' from permalinks
  trailing_html: true # Set to false to remove trailing '.html' from permalinks

# Deployment
## Docs: https://hexo.io/docs/one-command-deployment
deploy:
  type: git
  repo: git@github.com:Oort-ysf/Blogs.git
  branch: master

~~~



### 4.6、博客发布

安装Git发布工具

~~~bash\
npm install --save hexo-deployer-git
~~~

发布

~~~bash
hexo clean
hexo g
hexo d

~~~

出现类似内容表示发布成功

![4-6 博客发布到git仓库](%E3%80%90Hexo%E3%80%91%E5%8D%9A%E5%AE%A2%E6%90%AD%E5%BB%BA/4-6%20%E5%8D%9A%E5%AE%A2%E5%8F%91%E5%B8%83%E5%88%B0git%E4%BB%93%E5%BA%93.png)



## 5、在Gitee上发布

### 5.1、创建仓库

![5-1 创建仓库](%E3%80%90Hexo%E3%80%91%E5%8D%9A%E5%AE%A2%E6%90%AD%E5%BB%BA/5-1%20%E5%88%9B%E5%BB%BA%E4%BB%93%E5%BA%93.png)

### 5.2、配置Gitee Pages

![5-2 配置Gitee Pages-1](%E3%80%90Hexo%E3%80%91%E5%8D%9A%E5%AE%A2%E6%90%AD%E5%BB%BA/5-2%20%E9%85%8D%E7%BD%AEGitee%20Pages-1.png)

![5-2 配置Gitee Pages-2](%E3%80%90Hexo%E3%80%91%E5%8D%9A%E5%AE%A2%E6%90%AD%E5%BB%BA/5-2%20%E9%85%8D%E7%BD%AEGitee%20Pages-2.png)

### 5.3、本地配置Git信息

参考4.4章节，若4.4章节已配置则无需重复配置

### 5.4、添加SSH密钥

![5-4 添加SSH密钥](%E3%80%90Hexo%E3%80%91%E5%8D%9A%E5%AE%A2%E6%90%AD%E5%BB%BA/5-4%20%E6%B7%BB%E5%8A%A0SSH%E5%AF%86%E9%92%A5.png)



### 5.5、博客添加发布地址

修改`Blogs/_config.yml`文件，修改内容如下(注：可同时在Github和Gitee上发布)

~~~yaml
# Deployment
## Docs: https://hexo.io/docs/one-command-deployment
deploy:
  type: git
  repo: 
    github: git@github.com:Oort-ysf/Blogs.git
    gitee: git@gitee.com:Oort-ysf/Blogs.git
  branch: master

~~~



### 5.6、博客发布

参考4.6章节

