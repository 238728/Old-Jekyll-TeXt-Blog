---
title: 将博客网站部署到Cloudflare Pages（附Jekyll TeXt Thene特殊说明）
tags: [Web]
---

Cloudflare网站部署小记

<!--more-->

事先声明：我不是一名专业的Web工程师，本文章仅基于个人经验所写，请不要作为专业内容进行参考，谢谢您的配合！:smile::smile::smile:

# Cloudflare Pages简介

> Cloudflare Pages 是Cloudflare推出的静态网站托管服务，功能和 Github Pages 相似，可以存放静态网页，还可以直接部署前端项目。如果你的网站只是静态博客或帮助文档的话，可以完全不需要购买服务器。直接部署到 Cloudflare Pages 服务上。

> CloudFlare Pages 向免费用户提供了无限的站点数、请求数和带宽，除此之外付费用户可以获得更多的构建次数和同时构建站点数。

[具体信息请移步官网查看](https://pages.cloudflare.com/)

# 部署教程

首先，你需要一个Cloudflare账号（这是必须的）。如果有，请直接跳转到设置网站这一步。

## 注册账号

[点击这里注册Cloudflare账号](https://dash.cloudflare.com/sign-up)

~~注册账号这件事，不用我教吧……~~

## 设置网站

1. [登录Cloudflare控制台](https://dash.cloudflare.com/) ![Cloudflare控制台](/screenshots/cfdash-1.jpeg)
2. 导航到Pages 
3. 点击Create a project ![创建项目](/screenshots/cfdash-2.jpeg)
4. 点击Connect to a Git Provider ![连接仓库](/screenshots/cfdash-3.jpeg)
5. 在Github下面选择自己的账户和仓库（如果没有，则需要将Github账号连接到Cloudflare Pages） ![连接账户](/screenshots/cfdash-4.jpeg)
6. Framework Preset选择对应你的博客的框架（Hexo, Hugo, Node.js, Vue, Jekyll等等）如果框架选项中没有你博客的框架（例如Hexo），请参阅[Cloudflare Pages官方文档](https://developers.cloudflare.com/pages/framework-guides/)进行部署。在这里我以本博客为例，框架为Jekyll，直接选即可。接着点击Save and Deploy ![博客框架](/screenshots/cfdash-5.jpeg)
7. 等待部署即可（如果网速快的话，大约一分半的时间就可以完成）

# 注意事项

对于本博客使用的Jekyll TeXt Theme来说，不能直接部署，否则会出错：
```
...requires rubygems version >= 3.3.22,
which is incompatible with the current version, 3.1.2
```
遇到上述情况，不要慌，请在主题下的Gemfile文件中加入这一行：
```
gem "github-pages", "~> 215", group: :jekyll_plugins
```
我的Gemfile长这样：
```
source "https://rubygems.org"

# gem "github-pages", group: :jekyll_plugins
gem "github-pages", "~> 215", group: :jekyll_plugins
gemspec
```
这样就可以啦！:smiley::smiley::smiley:

~~苦苦费了一个月琢磨这个问题没有琢磨出来，最终发现原来是Gemfile的问题……~~
