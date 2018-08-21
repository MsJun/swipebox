# swipebox
swipebox灯箱(仿微博九宫格图片展示效果)


将下载的压缩包解压，咱么主要会用到以下文件

src
├── css
│   ├── swipebox.css  #css样式文件，二选一，推荐swipebox.min.css，文件更小
│   └── swipebox.min.css
├── img #这个目录的东需全部需要，放到你项目静态目录的根目录下
│   ├── icons.png
│   ├── icons.svg
│   └── loader.gif
└── js #实现动态效果的js代码，二选一，推荐第二个
    ├── jquery.swipebox.js
    └── jquery.swipebox.min.js
    
和

lib
└── jquery-2.1.0.min.js # 重要，必须是这个版本的jq，最新版无效

    1
    2

开始你的代码

<!DOCTYPE html>
<html lang="en">
<head>
    <!-- 脚本及样式文件（根据你文件的具体地址）-->
    <script src="/static/js/jquery-2.1.0.min.js"></script>
    <script src="/static/js/jquery.swipebox.min.js"></script>
    <link rel="stylesheet" href="/static/css/swipebox.min.css">
    <meta charset="UTF-8">
    <title>测试效果</title>
</head>
<body>
<div class="swipeboxEx"> <!--每个 div class="swipeboxEx" 代表一组图片-->
    <a  href="/media/big1.png" class="swipebox">  <!-- 点击图片后全屏放大的图片-->
        <img src="/media/small1.png" alt="image">  <!-- 直接显示的图片-->
    </a> <!-- 每对a标签代表一张大小图-->
</div>
<!--多组图片写多个 div class="swipeboxEx" -->

<!-- 直接复制-->
<script type="text/javascript">
    ;( function( $ ) {
        $( '.swipebox' ).swipebox();
    } )( jQuery );
</script>
</body>
</html>

最后说一点，先引用jq的js文件，后引用swipebox的，而且jq的文件必须是作者自带的！！
