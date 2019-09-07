---
title: GoSession
date: 2019-09-07 14:08:54
tags:
- Go
- session
comments: true
---
## session创建过程
	session 基本原理： 服务器为每个会话维护一份信息数据，客户端和服务器依靠一个全局唯一的标识符来访问这份数据，以达到交互的目的；
	这个过程可以概括为三个步骤：
	1. 生成全局唯一标识符(sessionid)
    2. 开辟数据存储空间
    3. 将全局唯一标识符发送给客户端。（cookie 和 URL 重写）
	
## session管理
	session管理涉及到一下几个因素：
	* 全局session管理器;
	* 保证sessionid的全局唯一性;
	* 为每个客户关联一个sessino;
	* session的存储；
	* session过期处理；
