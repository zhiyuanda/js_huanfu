# HTML+CSS+JS作品展示（换肤效果）
## 效果展示：

![img](https://img-blog.csdnimg.cn/e72e73b98b654f76a2470940789bedd5.gif)

## 网页GitHub地址如下：（若加载较慢建议刷新后耐心等待一会~）
https://zhiyuanda.github.io/js_huanfu/

## 主要功能：

点击缩略图，更换背景图效果

### 网页代码如下：

### HTML+CSS+JS：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>js_huanfu</title>
    <style>
        * {
            margin: 0;
            padding: 0;
        }
        body {
            background: url(images/1.jpg) no-repeat center top;
        }
        ul,
        li {
            list-style: none;
            margin: 0;
            padding: 0;
        }
        ul {
            width: 1000px;
            height: 110px;
            margin: 50px auto;
        }
        li {
            float: left;
            padding-right: 10px;
            width: 18%;
            height: 100%;
            cursor: pointer;
            box-sizing: border-box;
        }
        li img:hover {
            box-shadow: 4px 9px 14px -4px skyblue;
            transform: scale(1.5,1.5);
        }
        li img {
            width: 100%;
            height: 100%;
            transition: all .2s;
        }
    </style>
</head>

<body>
    <ul>
        <li><img src="images/1.jpg" alt=""></li>
        <li><img src="images/2.jpg" alt=""></li>
        <li><img src="images/3.jpg" alt=""></li>
        <li><img src="images/4.jpg" alt=""></li>
        <li><img src="images/5.jpg" alt=""></li>
    </ul>
    <script>
        var imgs = document.querySelector('ul').querySelectorAll('img');
        for (var i = 0;i < imgs.length;i++) {
            imgs[i].onclick=function() {
                document.body.style.backgroundImage = 'url(' + this.src + ')';
            };
        }
    </script>
</body>

</html>
```

