---
sidebar: true
contributors: true
---

# 由 Moeyy 提供的 CookieCloud 服务

CookieCloud是一个和自架服务器同步Cookie的小工具，可以将浏览器的Cookie及Local storage同步到手机和云端，它支持端对端加密，可设定同步时间间隔。

## 安全性

![](https://cdn.moeyy.cn/img/202307301634706.png/moeyy_webp)

因为 Cookie 数据非常敏感，因此 CookieCloud 采用强制端对端加密。也就是说无论加密和解密都是发生在你的电脑上，服务器端接触到的只有加密后的数据。

## 浏览器插件

1. 商店安装：[Edge商店](https://microsoftedge.microsoft.com/addons/detail/cookiecloud/bffenpfpjikaeocaihdonmgnjjdpjkeo) | [Chrome商店](https://chrome.google.com/webstore/detail/cookiecloud/ffjiejobkoibkjlhjnlgmcnnigeelbdl)（ 注意：商店版本会因审核有延迟
1. 手动下载安装：见 [Release](https://github.com/easychen/CookieCloud/releases)

## 服务器端

> 本站提供的免费服务器端供大家使用

```
https://cookiecloud.moeyy.cn
```

## 工作模式

![](https://cdn.moeyy.cn/img/202307301639539.png/moeyy_webp)

安装完后，点击浏览器插件图标会弹出设置界面。首先要选择的是工作模式，一个浏览器只能工作在上传或者下载覆盖状态。一般来讲，我们会把最常使用的浏览器设为上传模式，其他都设置为下载覆盖模式。

## 用户KEY

![](https://cdn.moeyy.cn/img/202307301639384.png/moeyy_webp)

由于一台服务器需要支持多个用户进行同步，因此需要通过用户 KEY 来进行区分。重复的用户 KEY 会导致同步数据覆盖，因此插件会自动生成一个足够长的随机 KEY 。当你配置下载覆盖模式时，需要使用同样的用户 KEY 。

## 密码

![](https://cdn.moeyy.cn/img/202307301640979.png/moeyy_webp)

密码用于端对端加密，由于服务器端完全不知道密码，因此无法找回。不过我们的场景下只是备份 Cookie ，忘记后可以设置新的密码覆盖原有云端数据就行了。同样的，当你配置下载覆盖模式时，需要使用同样的用户 KEY 。

## 同步域名关键词

![](https://cdn.moeyy.cn/img/202307301640617.png/moeyy_webp)

默认情况下，会上传所有的 Cookie ，但这会带来额外的流量消耗。因此我们提供了同步域名关键词，如果你填写了关键词，只有当 Cookie 的域名包含关键词时，才会上传对应的 Cookie 。有一个需要注意的地方是，部分网站的登入可能采用了其他二级域名，因此可能需要填写更短的顶级域名才能同步登入状态。

## Cookie保活

![](https://cdn.moeyy.cn/img/202307301640011.png/moeyy_webp)

即使是常用浏览器，某些网站我们长期不打开它的 Cookie 也会过期，这样即使同步了 Cookie 也是过期的。因此，我们添加了 Cookie 保活功能，填到这里的网址会每 60 分钟在后台打开一次。
```
https://moeyy.cn|5
```
你也可以在 URL 后加上竖线和分钟数，指定自己想要的间隔时间

## 覆盖模式的配置

![](https://cdn.moeyy.cn/img/202307301641383.png/moeyy_webp)

配置好了上传的浏览器，就可以配置下载覆盖的浏览器了。当然你需要再安装一遍插件。覆盖模式下不需要同步域名关键字和保活配置，其他项和上传浏览器的配置一样，服务器地址、用户 KEY 和密码则需要完全一致。

