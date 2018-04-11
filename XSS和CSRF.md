# XSS(cross site scripting)
## 原理
注入攻击，将html，js代码注入网页，其他用户使用时会执行注入的恶意代码

## 解决方法
1. 过滤特殊字符
2. 转义
3. 使用http头指定内容类型->content-type

# CSRF(cross-site request forgery)
## 原理
> 攻击者通过一些技术手段欺骗用户的浏览器去访问一个自己曾经认证过的网站，被访问的网站会认为是真正的用户操作而去执行。   
> 简单的身份验证只能保证请求发自某个用户的浏览器，却不能保证请求本身是用户自愿发出的。

## 解决方法
1. 检查Referer字段-> HTTP头中Referer应和请求的url位于同一域名
2. 添加校验token
