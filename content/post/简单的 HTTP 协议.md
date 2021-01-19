---
title: "简单的 HTTP 协议"
date: 2021-01-19T14:24:30+08:00
lastmod: 2021-01-20T20:12:35+08:00
draft: false
tags: ["HTTP"]
categories: ["技术"]

weight: 10
contentCopyright: MIT
mathjax: true
autoCollapseToc: true

---

## 1. HTTP 协议用于客户端和服务器端之间的通信

{{% admonition  info %}}
请求访问文本或图像等资源的一端称为客户端，而提供资源响应的一 端称为服务器端。
{{% /admonition %}}

### HTTP请求报文

```
POST /user HTTP/1.1      //请求行
Host: www.user.com
Content-Type: application/x-www-form-urlencoded
Connection: Keep-Alive
User-agent: Mozilla/5.0.      //以上是首部行
（此处必须有一空行）  //空行分割header和请求内容 
name=world   请求体
```

{{% admonition info POST %}}

起始行开头的**POST**表示请求访问服务器的类型，称为方法。

{{% /admonition %}}

{{% admonition info user%}}

随后的字符串 /user 指明了请求访问的资源对象， 也叫做请求 URI。

{{% /admonition %}}

{{% admonition info HTTP版本号 %}}

HTTP/1.1，即 HTTP 的版本 号，用来提示客户端使用的 HTTP 协议功能。

{{% /admonition %}}

>  请求报文是由请求方法、请求 URI、协议版本、可选的请求首部字段和内容实体构成的。



### HTTP返回报文

```
HTTP/1.1 200 OK 
Date: Tue, 10 Jul 2020 06:50:15 GMT 
Content-Length: 362
Content-Type: text/html

<html>
...
```

{{% admonition info HTTP版本号 %}}

HTTP/1.1，表示服务器对应的 HTTP 版本。

{{% /admonition %}}

{{% admonition info 状态码 %}}

200 OK 表示请求的处理结果的状态码（status code）和 原因短语（reason-phrase）。

{{% /admonition %}}

{{% admonition info 响应时间 %}}

下一行显示了创建响应的日期时间，是首部 字段（header field）内的一个属性。

{{% /admonition %}}

{{% admonition info 主体 %}}

接着以一空行分隔，之后的内容称为资源实体的主体（entity body）。

{{% /admonition %}}

> 响应报文基本上由协议版本、状态码（表示请求成功或失败的数字代 码）、用以解释状态码的原因短语、可选的响应首部字段以及实体主 体构成。

