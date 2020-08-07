---
title: 开源镜像站 CN
tags:
- mirrors
categories:
- tools
---

## 列表

* [清华大学开源软件镜像站| Tsinghua Open Source Mirror](https://mirrors.tuna.tsinghua.edu.cn/)
* [阿里巴巴开源镜像站-OPSX镜像站-阿里云开发者社区](http://developer.aliyun.com/mirror)
* [华为开源镜像站_软件开发服务_华为云](https://mirrors.huaweicloud.com/)



## Python - PIP

1. 临时使用
   1. ·pip install --trusted-host https://mirrors.huaweicloud.com -i https://mirrors.huaweicloud.com/repository/pypi/simple
      <some-package>·

2. 设为默认
   1. Pip的配置文件为用户根目录下的：**~/.pip/pip.conf**（Windows路径为：**C:\Users\<UserName>\pip\pip.ini**）

```
[global]
index-url = https://mirrors.huaweicloud.com/repository/pypi/simple
trusted-host = mirrors.huaweicloud.com
timeout = 120
```

## PHP - Composer

1. 修改全局配置(推荐)

   1. `composer config -g repo.packagist composer https://mirrors.huaweicloud.com/repository/php/`

2. 修改项目配置

   1. `composer config repo.packagist composer https://mirrors.huaweicloud.com/repository/php/`

   2. 手工在**composer.json**中添加如下内容

      1. ```
         "repositories": {
             "packagist": {
                 "type": "composer",
                 "url": "https://mirrors.huaweicloud.com/repository/php/"
             }
         }
         ```

         