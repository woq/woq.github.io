---
title: BACK IN GAME with HEXO
---





##  前话

之前的服务器到期之后，数据也没备份，没了

其实最早的方式是Github Pages，后来转去Wordpress，再到Typecho都用过，因为国内需要备案一直用的美国那边VPS，访问不稳定，然后续费也不太稳定~

现在转念一想，这个东西必须得拾起来，用最简单的方式就好了





## 基础

* Git
  * https://npm.taobao.org/mirrors/git-for-windows/
* Node.js
  * https://nodejs.org
* CNPM
  * https://npm.taobao.org/
* git
  * 设置proxy 具体google



## 简单命令

* hexo init
* hexo new  
* hexo generate / hexo g
* hexo server / hexo s 
* hexo deploy / hexo d



## 主题

简单熟悉命令之后，就是给你的博客找一个你喜欢的主题了~

主题使用与配置看Readme就好了



## 部署到Github pages

使用[Travis CI](https://travis-ci.com/)去部署，但前提是你的项目是开源的，不然需要付费使用



## 遇到的问题

现在构建方法变了，也或许是记忆模糊了... 你自己push源代码上去 然后Travis CI会自动帮你把源代码变成可浏览的网站



解决方法？ 配置好你的 .travis.yml 就可以了，如果自己安装了其他主题，按照主题提供的demo文件去修改