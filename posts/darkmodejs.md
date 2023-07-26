　　Darkmodejs是一个JavaScript库，可以帮助您在网站上实现暗模式。它可以自动检测用户的操作系统和浏览器设置，并根据用户的首选项自动切换网站的颜色主题。

使用Darkmodejs非常简单。您只需要在网站中引入Darkmodejs的JavaScript文件，并在页面加载时初始化它。以下是一个基本的示例：

```html
<!DOCTYPE html>
<html>
<head>
  <title>My Website</title>
  <script src="darkmode.js"></script>
  <script>
    const options = {
      bottom: '64px', // default: '32px'
      right: 'unset', // default: '32px'
      left: '32px', // default: 'unset'
      time: '0.5s', // default: '0.3s'
      mixColor: '#fff', // default: '#fff'
      backgroundColor: '#fff',  // default: '#fff'
      buttonColorDark: '#100f2c',  // default: '#100f2c'
      buttonColorLight: '#fff', // default: '#fff'
      saveInCookies: true, // default: true,
      label: '🌓', // default: ''
      autoMatchOsTheme: true // default: true
    }

    const darkmode = new Darkmode(options);
    darkmode.showWidget();
  </script>
</head>
<body>
  <h1>Welcome to my website</h1>
  <p>This is some sample text.</p>
</body>
</html>
```

当用户单击切换按钮时，Darkmodejs会自动切换网站的颜色主题，并将用户的首选项保存在cookie中，以便在下次访问时自动应用。