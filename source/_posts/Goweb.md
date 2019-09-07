---
title: Goweb
date: 2019-09-07 14:08:00
tags:
- Go
- Web
catetories:
- recording
---
## Web 工作方式的几个概念
	Request： 用户请求的信息，包括post,get,cookie,url 等信息
	Reponse： 服务器返回给客户端的信息
	Conn：    用户的每次请求链接
	Handler： 处理请求和生成返回信息的处理逻辑

## Go Web工作流程
	1. 创建Listen Socket，监听指定的端口，等待客户端请求到来
	2. Listen Socket接受客户端的请求，得到Client Socket，通过Client Socket 与客户端通信
	3. 处理客户端的请求，首先从Client Socket 读取HTTP 请求的协议头，根据方法转交给相应的Handler 处理，
	Handler 处理完毕后将处理结果通过Client Socket 写给客户端
