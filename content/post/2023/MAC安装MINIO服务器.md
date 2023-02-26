---
title: "MAC安装MINIO服务器"
date: 2023-02-26T23:45:47+08:00
draft: true
---

官网：[MINIO官网链接](https://www.minio.org.cn/download.shtml#/macos)

## 1.[homebrew](https://so.csdn.net/so/search?q=brew&spm=1001.2101.3001.7020)安装

```java
brew install minio/stable/minio
```

![img](https://cdn.nlark.com/yuque/0/2023/png/472835/1677425442971-f88e8eb2-3397-49e7-bb8f-03390c4805f8.png)

## 2.安装完成后

```java
brew info minio
```

![img](https://cdn.nlark.com/yuque/0/2023/png/472835/1677425361458-a8f0b388-c348-47c4-b7ac-8b7b1e77f270.png)

## 3.启动

```java
/usr/local/opt/minio/bin/minio server --config-dir=/usr/local/etc/minio --address=:9000 /usr/local/var/minio
```

![img](https://cdn.nlark.com/yuque/0/2023/png/472835/1677425414408-53a0191d-a4f1-4f1e-b3ca-4732be3020c6.png)

config-dir=/usr/local/etc/minio     	配置文件目录
address=:9000   				使用的端口
/usr/local/var/minio				存储数据目录

cmd+c关闭服务器。

## 4.访问

API: http://192.168.31.230:9000 		 http://127.0.0.1:9000

Console: http://192.168.31.230:53563		 http://127.0.0.1:53563

RootUser: minioadmin

RootPass: minioadmin

![img](https://cdn.nlark.com/yuque/0/2023/png/472835/1677425663622-86af1e12-64b1-42ca-ae72-b45b8af9279b.png)

