# Docker进阶篇

# Docker Compose

## 概述

前面我们使用 Docker 的时候，定义 Dockerfile 文件，然后使用 docker build、docker run 等命令操作容器。然而微服务架构的应用系统一般包含若干个微服务，每个微服务一般都会部署多个实例，如果每个微服务都要手动启停，那么效率之低，维护量之大可想而知。

**使用 Docker Compose 可以轻松、高效的管理容器，它是一个用于定义和运行多容器 Docker 的应用程序工具**

## 基本使用

1. 安装：

   1. 安装 Docker Compose 可以通过下面命令自动下载适应版本的 Compose，并为安装脚本添加执行权限

   2. ```ruby
      要安装不同版本，请替换您要使用的版本。1.29.2
      sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
      # 国内
      curl -L https://hub.fastgit.org/docker/compose/releases/download/1.25.1/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
      向二进制文件应用可执行权限：
      sudo chmod +x /usr/local/bin/docker-compose
      ```

   3. 查看是否安装成功：docker-compose -v

   ![image-20211112152539089](https://mynotepicbed.oss-cn-beijing.aliyuncs.com/img/image-20211112152539089.png)

2. 运行docker-compose文件
   1. 在docker-compose文件所在目录下，执行命令：docker-compose up

