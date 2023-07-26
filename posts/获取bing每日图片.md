[必应](https://bing.com)的主页每天都会放上一张好看的壁纸，很适合当博客的背景。
今天的bing图片：
![今天的bing图片][1]


  [1]: https://api.mtxh.fun/i/bing.php

# 代码


```php
<?php

$str = file_get_contents('http://cn.bing.com/HPImageArchive.aspx?idx=0&n=1');   // 从bing获取数据

 

if(preg_match('/<url>([^<]+)<\/url>/isU', $str, $matches)) { // 正则匹配抓取图片url

    $imgurl = 'http://cn.bing.com'.$matches[1];

} else {  // 如果由于某些原因，没抓取到图片地址

    $imgurl = 'http://img.infinitynewtab.com/InfinityWallpaper/2_14.jpg'; // 使用默认的图像(默认图像链接可修改为自己的)

}

 

header("Location: {$imgurl}");    // 跳转至目标图像
```
# 原理
[http://cn.bing.com/HPImageArchive.aspx?idx=0&n=1](http://cn.bing.com/HPImageArchive.aspx?idx=0&n=1)会返回bing图片的信息（json），比如图片地址，名称。根据信息，使用正则就可得到图片地址。