# 简介

Umami 是一个开源、注重隐私的谷歌分析的替代品

官方网站：https://umami.is/

官方文档：https://umami.is/docs/

开源地址：https://github.com/umami-software/umami

## 优点

1.开源：Umami是一个完全开源的项目，可以在GitHub上获取其源代码。这意味着你可以自由地自定义、修改和贡献代码。

2.隐私保护：Umami非常注重用户隐私保护。与其他常见的网站统计工具相比，Umami不使用第三方跟踪脚本或Cookie，也不与广告平台共享数据。用户的访问数据完全保留在自己的服务器上，没有被共享或用于其他目的。

3.简洁而直观的界面：Umami具有简洁、直观的用户界面，易于使用和导航。它提供了各种报告和分析工具，以可视化的方式展示网站的访问数据，帮助用户快速了解其网站的表现和趋势。

4.实时数据更新：Umami能够实时收集和更新访问数据，你可以随时查看最新的数据情况，而不需要等待数据的延迟。

5.多网站管理：Umami支持多个网站的管理和统计。你可以在一个实例中运行多个Umami跟踪代码，轻松管理并比较不同网站的数据。

6.自定义事件追踪：Umami允许用户自定义追踪事件，以收集和分析特定的用户行为。你可以跟踪页面浏览量、按钮点击、表单提交等行为，获取更详细的数据。

7.支持Vercel部署。

# 数据库

打开[supabase](https://supabase.com/)并使用github登录，选择 Free 方案，按要求填写相关内容。Name 填写任意项目名，Database Password 可以使用下方工具 Generate a password 生成，初始化完成后点击Project Settings中的Database，将Connection info中的内容记录下来。

# 部署

登录Vercel，让后点击这个按钮

[![](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fumami-software%2Fumami&env=DATABASE_URL)

随便输一个项目名，点击Create，在下方的Configure Project中新建一个名称为DATABASE_URL的环境变量，值的格式为

> postgresql://username:mypassword@host:5432/mydb

把其中的username替换为刚刚记录下来的Database name，mypassword替换为给项目设置的密码，host替换为Host，mydb替换为postgres。

在新建一个名称为HASH_SALT的的环境变量，值随便输，最好长一点。

然后点击Deploy部署，等待几十秒，出现满屏的烟花就是部署成功了。

# 自定义域名

因为vercel提供的免费二级域在国内被墙，所以需要绑定自己的域名。

进入Settings-Domains，添加自定义域名，按提示给输入的域名添加dns记录。没有域名的可以去申请[eu.org](https://eu.org)免费域名，或去搜索[免费二级域名分发](https://dk.mtxhblog.top/?q=%E5%85%8D%E8%B4%B9%E4%BA%8C%E7%BA%A7%E5%9F%9F%E5%90%8D%E5%88%86%E5%8F%91_)，有一大堆。

# 使用

打开配置的域名，默认用户名和密码分别是 admin 和 umami ，进入后台可以修改密码、设置语言，然后就可以添加网站了。

# 效果

[共享连接](https://umami.mtxh.fun/share/0bMZqO9xVtrKEknm/%E6%BB%A1%E5%A4%A9%E6%98%9F%E6%B2%B3%E7%9A%84%E5%8D%9A%E5%AE%A2)