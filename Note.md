## Mailcatcher 原理分析

启动两个服务
smtp server: 1025
smtp用于接受发送给它的mail message

http server: 1080
http则作为mail的client， 供用户读取邮件

在mailcatcher内部使用memory 类型的sqlite3 db存储收到的邮件

web使用sinatra
邮件推送则使用eventmachine + thin + websocket

不错的邮件收发器

console访问存储的数据

MailCatcher::Mail.messages

## 挖掘试验

编译静态资源
bundle exec rake assets

运行测试
bundle exec rake test   


## 类似产品

MailGun
MailHog
