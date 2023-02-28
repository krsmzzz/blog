---
title: "MAC安装MINIO服务器"
date: 2023-02-26T23:45:47+08:00
draft: true
---

官网：[MINIO官网链接](https://www.minio.org.cn/download.shtml#/macos)

## homebrew安装

```java
brew install minio/stable/minio
```

## 安装完成后

```java
brew info minio
```

## 启动

```java
/usr/local/opt/minio/bin/minio server --config-dir=/usr/local/etc/minio --address=:9000 /usr/local/var/minio
```

config-dir=/usr/local/etc/minio     	配置文件目录
address=:9000   				使用的端口
/usr/local/var/minio				存储数据目录

cmd+c关闭服务器。

## 访问

API: http://192.168.31.230:9000 		 http://127.0.0.1:9000

Console: http://192.168.31.230:53563		 http://127.0.0.1:53563

RootUser: minioadmin

RootPass: minioadmin

