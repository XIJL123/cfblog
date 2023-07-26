# 简介
Valine -是一款基于LeanCloud的快速、简洁且高效的无后端评论系统。他快速、简洁且高效，使用起来非常简单。
# 开始
请先登录或注册 LeanCloud, 进入控制台后点击左下角创建应用。
应用创建好以后，进入刚刚创建的应用，选择左下角的设置>应用Key，然后就能看到你的APP ID和APP Key了。
修改下面代码中的appId和appKey的值为上面刚刚获取到的值即可(其他可以默认)。
```html
<head>

    ..

    <script src='//unpkg.com/valine/dist/Valine.min.js'></script>

    ...

</head>

<body>

    ...

    <div id="vcomments"></div>

    <script>

        new Valine({

            el: '#vcomments',

            appId: 'Your appId',

            appKey: 'Your appKey'

        })

    </script>

</body>
```
# 评论数据管理
由于Valine 是无后端评论系统，所以也就没有开发评论数据管理功能。请自行登录Leancloud应用管理。
具体步骤：登录>选择你创建的应用>存储>选择Class Comment，然后就可以尽情的发挥你的权利。
# 效果
![效果][1]
# 更多
[官方文档](https://valine.js.org/)


  [1]: https://img2022.cnblogs.com/blog/2974308/202211/2974308-20221116235528455-1331731776.jpg